# GraphQL.

GraphQL allow us to get data using just a single end-point.
When we try to request data using REST routes, we create several end-points to each objects, and besides, it give us information that we don't need.
GraphQL deliver only the data that we request.

## Software requirments.

* NodeJS.
* React.
* Git.
* Mongo DB.
* Atom.
* Emulate console CMDER.

## Project.

In this project you will be able to create authors and books, and retrieve this
data using GraphQL.

### Step 01. NodeJS installation.

1. Create a folder "server".
2. Type `npm init`.
3. Type `npm install express`.
4. Create a file app.js in **server** folder and add the code.
5. Type the command: `npm install nodemon -g`
6. Type the command: `nodemon app`

## Step 02. Setting GraphQL.

1. Type the command: `npm install graphql express-graphql` in project root.
2. Type the command: `npm install -g lodash`.
3. Add the code to app.js file.
4. Create an schema folder and schema.js and add the code.
5. Run the server and find books by typing:

```
{
  book(id: "1"){
    id,
    name
  }
}
```

## Step 03. GraphQL Type ID and Authors.

1. We can look up for objects by using its ID: `GraphQLID`.
2. Repeat the same process creating an Author Objcet.
3. To declare an integer in GraphQL, we define: `GraphQLInt`.

```
{
  book(id: "1"){
    id,
    name
  }
}
```

## Step 04. Associtations belongs-to author.

This section applies for the Book object.

1. Add a new column to each book and asign them the author id.
2. Add the code in BookType function.

```
{
  book(id: 1){
    id,
    name
    author{
      name
    }
  }
}
```

## Step 05. Associtations has-many books.

This section applies to Author object.

1. We define a list object for the author: `GraphQLList`.
2. We add the method within author function.

```
{
  author(id: 2){
    name,
    books{
      id,
      name
    }
  }
}
```

## Step 06. Get all books and authors.

1. Add the methods into the RootQuery function.

```
{
  authors{
    name
  }
}
```
## Step 07. Adding Mongo DB.

1. Sign in for a free account in Mongo DB.
2. Create a database and a cluster by free.
3. Wait until the database is ready and copy the link connection.
4. Within app.js file, add the constant and the code in order to connect to the database.

## Step 08. Mongoose models.

1. Create a folder called: **models**.
2. Create a file for books: **book.js**
3. Create a file for authors: **author.js**
4. Add the code in each file (book.js and author.js);
5. The changes were to comment the returns lines because we don't need the arrays objects anymore and we import the files at the top of the file.

## Step 09. Mutations.

Mutations allow us to insert, update or delete our data sin our database. We configure the Schema with Mongo DB, so we need to insert some data.

1. Adding the method Mutation at the bottom of the file and add a new module.exports

```
mutation{
  add_book(name: "The Outliers", genre: "Entreprenurship", author_id: "6264498e48c1f7be7df96f9d"){
    name,
    genre,
    author{
      name
    }
  }
}
```

## Step 10. Mutations (part 2).

We added mutations to books as well.

## Step 11. Get all books and authors.

In this section we add few lines in order to get all books and authors by the query command.
Also, we added the list and collection to get the associations between these two models.

```
query{
  books{
    name
    author {
      id,
      name
    }
  }
}
```

## Step 12. Validations.

We can add validations to each field in order to store all the data needed.

1. Add GraphQLNonNull and place it in the add or create method

## Step 13. Installing React.

1. Open a new tab with server running, and type: `npm install create-react-app -g`.
2. Create the React app in the server folder: `create-react-app client`.
3. Go to client folder by cmd ant type: `npm start` and it'll open the browser.

Some files were deleted in order to make the web application simpler.

## Step 14. Listing books.

1. Create a file in client/src/components/BookList.js
2. Render files among them.

## Step 15. Implementing a GraphQL Client - Apollo.

1. Inside of the folder client, install Apollo by typing: `npm install apollo-boost react-apollo graphql --save`.
2. In App.js file, import ApolloClient.
