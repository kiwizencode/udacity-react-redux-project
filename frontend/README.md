# Readable Project

The objective of the project is to build a content and comment web app, where users will be able to post content to predefined categries, comment on their post and other user's posts, and vote on posts and comments. Morover the users will be able to edit and delete posts and comments.


## How to run this project

Firstly, we need to install and then start API server, run the following commands in `api-server` directory:

* `npm install`
* `npm start`

Secondly, we need to install all project dependencies and then start the development server, run the following commands in `frontend` directory:

* `npm install`
* `npm start`

## Here is the project structure
```bash
├── README.md - This file.
├── package.json # npm package manager file.
├── public
│   ├── favicon.ico # React Icon.
│   └── index.html # DO NOT MODIFY
└── src
    ├── actions
    │   ├── categories.js # Actions & Action creators for categories.
    │   ├── comments.js # Actions & Action creators for (post) comment.
    │   ├── index.js # main file that exports all Action & Action creators.
    │   ├── posts.js # Actions & Action creators for posts.
    │   └── sort_post # Actions & Action creators for sorting of posts.
    ├── components
    │   └── main_section # components related to main section.
    │   │   └── main_nav # components realted to main navigation section.
    │   │   │   ├── Category.css # Styles for category component.
    │   │   │   ├── Category.js # react component that render a Link component for a category.
    │   │   │   ├── CategorySelector.css # Styles for category selector component.
    │   │   │   ├── CategorySelector.js # react component that render a list of Category components for user to select. This is done by using a container component FilterCategory for the Category component.
    │   │   │   ├── MainNav.css # Styles for main navigation section component.
    │   │   │   ├── MainNav.js # this is the main navigation section componen which, in turn, render both CategorySelector component and SortPostSelector component. 
    │   │   │   ├── SortPostSelector.css # Styles for sorting of post component.
    │   │   │   ├── SortPostSelector.js # react component that render a list of post attributes for user to select to sort post by. 
    │   │   ├── comment.svg # background image for no of comments. 
    │   │   ├── CommentCards.css # Styles for comment 'card' component.
    │   │   ├── CommentCards.js # react component that render comment information.
    │   │   ├── CommentModalDialog.css # Styles for comment dialog box component.
    │   │   ├── CommentModalDialog.js # react component that render a modal dialog box to display comment's information. (for creating/editing/deleting comment operation)
    │   │   ├── CommentSection.js # This is the (main) comment section component which will display a list of comment 'card' for a particular post. It also contain separate CommentModalDialog components for editing and deleting of comment.
    │   │   ├── heart.svg # background image for no of voteScore for both post and comment component. 
    │   │   ├── MainSection.js # This is the Main Section component. It will display the main navigation component as well as the post section. It will contain separate PostModalDialog components for creating, editing and deleting of post. In addition, it will also contain a CommentModalDialog components to create new comment.
    │   │   ├── PostCard.css # Styles for post 'card' component. 
    │   │   ├── PostCard.js # react component that render render either post summary (POST_SUMMARY) or post detail (POST_DETAIL) information.
    │   │   ├── PostModalDialog.css # Styles for post dialog box component.
    │   │   ├── PostModalDialog.js # react component that render a modal dialog box to display post's information. (for creating/editing/deleting post operation)
    │   │   ├── thumbs-down.svg # background image for 'down' voteScore for both post and comment component. 
    │   │   ├── thumbs-up.svg # background image for 'up' voteScore for both post and comment component. 
    │   ├── App.js # This is the root of the app. It will render Header component as well as Footer component. It also setup the routing for MainSection component for the app.
    │   ├── Footer.css # Styles for footer section component.
    │   ├── Footer.js # react component that render the footer section of the main page.
    │   ├── Header.css # Styles for header section component.
    │   ├── Header.js # react component that render the header section of the main page.
    │   ├── NoMatch.css # Styles for No Match component.
    │   └── NoMatch.js # react component that render a page when encounter 404 page in the app.   
    ├── containers # components that incorporate redux store data state and dispatch function with some of the react components.
    │   ├── FilterCategory.js # This add redux data state or dispatch function to Category component. This perform some action when user select a categoryb (in CategorySelector.js)
    │   ├── Main.js # This add redux store data or dispatch function to MainSection component. It's basically perform sort operation on the list of post based on user selection (in SortPostSelector.js) and store the result ina varianble called sorted_posts.
    │   └── Readable.js # This add redux store data or dispatch function to App (root) component. It define most of the redux store state as well as functions required in the whole application.  
    ├── reducers # components that specify how the application's state changes in response to actions sent to the store.
    │   ├── categories.js # reducers for categories.
    │   ├── category.js # reducers for action when user select a category (in CategorySelector.js). It also change for any change in url and update the state of the category based on the change in url.
    │   ├── comments.js # reducers for (post) comment.
    │   ├── index.js # main file that exports all reducers ( including redux router reducer).
    │   ├── posts.js # reducers for posts.
    │   └── sort_post # reducers for sorting of posts.
    ├── utils # java script that perform general function in the application.
    │   ├── constant_helper.js # define constant used in the application.
    │   ├── db_api_helper.js # define functions to perform web api to the backend server.
    │   └── sort_post_helper.js # define constants related to sorting of post.
    ├── index.css # styles sheet for index.js. I have added some common elements style sheet, which is standard throughout the whole project.   
    └── index.js # It has the follwoing tasks : create the store, middleware, as well as synchronize router history with store. And finally it is render the main component to DOM.
```

## Following are rescources that I used in preparing for this project

* [React Redux Todo List example](https://redux.js.org/basics/example-todo-list) 
* [Usage with React Router](https://redux.js.org/advanced/usage-with-react-router)
* [Managing the URL in a Redux app](https://blog.marvelapp.com/managing-the-url-in-a-redux-app/)
* Create a react modal dialog with [react-modal](https://github.com/reactjs/react-modal)

## Create React App

This project was bootstrapped with [Create React App](https://github.com/facebookincubator/create-react-app). You can find more information on how to perform common tasks [here](https://github.com/facebookincubator/create-react-app/blob/master/packages/react-scripts/template/README.md).
