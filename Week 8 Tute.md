* Reminder: Don't include node modules in ass 4 (run npm -i on pull)
## Activity 0

What is wrong with this code?
* Shallow copy vs deep copy

```js
let board = [
	["", "", ""],
	["", "", ""],
	["", "", ""]
]
let newBoard = board;

// deep copy
let newBoardDeep = board.map(row => {
	let newRow = [];
	row.forEach(item => newRow.push(item));
});

// or spread operator
let newBoardDeep = board.map(row => [...row]);

newBoard[0][1] = "0";
console.log(board);
console.log(newBoard);
```

## React

* We’ve done everything by manipulating the DOM tree (pure HTML nodes, document is a graph of elements linked together)
* React creates a copy of the original DOM (called the virtual DOM), and stores it in its own memory
* After creating a new virtual node, react does a diff between the original and virtual node, then inserts it into the real DOM
* Using virtual DOM is more efficient (can batch updates)
* Important to set IDs so not everything refreshes
* Local variables do not persist on react unmount/remount -> use react state

```js
useEffect(() => {
	console.log("Hi");
	return () => {
		console.log("Bye");
	}
}, [] ) // empty dependency array only runs FIRST TIME component mounts, 

// without dependency array code "Hi" logs every time component mounts
// and "Bye" every time it unmounts
```


## Tic-tac-toe

