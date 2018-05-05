# Readable Project

The objective of the project is to build a content and comment web app, where users will be able to post content to predefined categries, comment on their post and other user's posts, and vote on posts and comments. Morover the users will be able to edit and delete posts and comments.


## TL;DR

To get started developing right away:

* install all project dependencies with `npm install`
* start the development server with `npm start`


The following page will under-construction ...... 

## What You're Getting
```bash
├── README.md - This file.
├── SEARCH_TERMS.md # The whitelisted short collection of available search terms for user to use with the app.
├── package.json # npm package manager file.
├── public
│   ├── favicon.ico # React Icon.
│   └── index.html # DO NOT MODIFY
└── src
    ├── App.css # Styles for your app. Feel free to customize this as you desire.
    ├── App.js # This is the root of your app. Contains static HTML right now.
    ├── App.test.js # Used for testing. Provided with Create React App. Testing is encouraged, but not required.
    ├── BooksAPI.js # A JavaScript API for the provided Udacity backend. Instructions for the methods are below.
    ├── icons # Helpful images for your app. Use at your discretion.
    │   ├── add.svg
    │   ├── arrow-back.svg
    │   └── arrow-drop-down.svg
    ├── App.css # Global styles for MyRead App.
    └── App.js # This is react component that attached to 'root' HTML element that is used to render either MainPage react component or SearchPage react component.
    └── Book.js # This is the react component that render 'Book' information onto UI.
    └── BookShelf.js # This is the react component that render 'BookShelf' information onto UI. It in turn call Book.js to render individual 'Book' information.
    └── BookAPI.js # This is the javascript library that implement the RESTful API for react component to call backend server to push or pull 'Book' information.
    └── MainPage.js # This is react component that render the 'Main Page' html. It will call Bookshelf components to render individual 'BookShelf' onto UI.
    └── PageNotFound.js # This is react component that render the 404 error 'Page Not Found' html. 
    └── SearchPage.js # This is the react component that render 'Search Book' html. This page allow user to search for books and also added to 'BookShelf' in 'Main Page' html.
    ├── index.css # styles sheet for index.js. 
    └── index.js # You should not need to modify this file. It is used for DOM rendering only.
```

Remember that good React design practice is to create new JS files for each component and use import/require statements to include them where they are needed.

## Backend Server

To simplify your development process, we've provided a backend server for you to develop against. The provided file [`BooksAPI.js`](src/BooksAPI.js) contains the methods you will need to perform necessary operations on the backend:

* [`getAll`](#getall)
* [`update`](#update)
* [`search`](#search)

### `getAll`

Method Signature:

```js
getAll()
```

* Returns a Promise which resolves to a JSON object containing a collection of book objects.
* This collection represents the books currently in the bookshelves in your app.

### `update`

Method Signature:

```js
update(book, shelf)
```

* book: `<Object>` containing at minimum an `id` attribute
* shelf: `<String>` contains one of ["wantToRead", "currentlyReading", "read"]  
* Returns a Promise which resolves to a JSON object containing the response data of the POST request

### `search`

Method Signature:

```js
search(query, maxResults)
```

* query: `<String>`
* maxResults: `<Integer>` Due to the nature of the backend server, search results are capped at 20, even if this is set higher.
* Returns a Promise which resolves to a JSON object containing a collection of book objects.
* These books do not know which shelf they are on. They are raw results only. You'll need to make sure that books have the correct state while on the search page.

## Important
The backend API uses a fixed set of cached search results and is limited to a particular set of search terms, which can be found in [SEARCH_TERMS.md](SEARCH_TERMS.md). That list of terms are the _only_ terms that will work with the backend, so don't be surprised if your searches for Basket Weaving or Bubble Wrap don't come back with any results.

## Create React App

This project was bootstrapped with [Create React App](https://github.com/facebookincubator/create-react-app). You can find more information on how to perform common tasks [here](https://github.com/facebookincubator/create-react-app/blob/master/packages/react-scripts/template/README.md).
