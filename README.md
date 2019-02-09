# GoogleBooks

This app is a React-based Google Books Search app, which uses create React components, works with helper/util functions, and utilizes React lifecycle methods to query and display books based on user searches. This app also use Node, Express and MongoDB so that users can save books to review or purchase later.

### LINKS to this app

* Github Repository: https://github.com/emadamczyk/GoogleBooks
* Heroku: 

### How it Works

* This application has 2 pages -- Search and Saved:

  * **Search** - User can search for books via the Google Books API and render them here. User has the option to "View" a book, bringing them to the book on Google Books, or "Save" a book, saving it to the Mongo database.

  * **Saved** - Renders all books saved to the Mongo database. User has an option to "View" the book, bringing them to the book on Google Books, or "Delete" a book, removing it from the Mongo database.

This is a full stack application that is connected to a MongoDB database named `googlebooks` using the mongoose npm package.

Within mongoose there is a Book schema -- books -- with the following fields:

* `title` - Title of the book from the Google Books API

* `authors` - The books's author(s) as returned from the Google Books API

* `description` - The book's description as returned from the Google Books API

* `image` - The Book's thumbnail image as returned from the Google Books API

* `link` - The Book's information link as returned from the Google Books API



This app uses the following Express routes:

* `/api/books` (get) - Returns  all saved books as JSON.

* `/api/books` (post) - Used to save a new book to the database.

* `/api/books/:id` (delete) - Used to delete a book from the database by Mongo `_id`.

* `*` (get) - Loads a single HTML page in `client/build/index.html`. 

This app is deployed using Heroku. It uses **Create React App** and current versions of React and React-Router-Dom.