MyReads is an application that allows you to search, select and categorize books you have read, are currently reading, or want to read. It is built to demonstrate React fundamentals like UI rendering, state management, React Router, etc.

## Getting Started

```
git clone https://github.com/sreeramsama/MyReads.git
cd MyReads
npm install
npm start
```

## Backend Server

The provided file [`BooksAPI.js`](src/BooksAPI.js) contains the methods used to perform necessary operations on the backend:

### `getAll()`
* Returns a Promise which resolves to a JSON object containing a collection of book objects.
* This collection represents the books currently in the bookshelves in your app.

### `update(book, shelf)`
* book: `<Object>` containing at minimum an `id` attribute
* shelf: `<String>` contains one of ["wantToRead", "currentlyReading", "read"]  
* Returns a Promise which resolves to a JSON object containing the response data of the POST request

### `search(query, maxResults)`
* query: `<String>`
* maxResults: `<Integer>` Due to the nature of the backend server, search results are capped at 20, even if this is set higher.
* Returns a Promise which resolves to a JSON object containing a collection of book objects.

## Important
The backend API uses a fixed set of cached search results and is limited to a particular set of search terms, which can be found in [SEARCH_TERMS.md](SEARCH_TERMS.md). That list of terms are the _only_ terms that will work with the backend.

## create-react-app
This project was bootstrapped with [Create React App](https://github.com/facebookincubator/create-react-app), and forked from [Udacity Starter Code](https://github.com/udacity/reactnd-project-myreads-starter)