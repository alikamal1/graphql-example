# graphql-example
a simple example of GraphQL

All books
```
{
  books {
  	id
  	name
  } 
}
```
All books
```
{
  authors {
  	id
  	name
  } 
}
```
Books with author
```
{
  books{
  	id
  	name
    author {
      name
    }
  } 
}
```
Book name from id
```
{
	book(id:1) {
    name
  }
}
```
Author from id with books
```
{
	author(id:1) {
    name,
    books{
      name
    }
  }
}
```
Add new book
```
mutation {
  addBook(name: "New Book", authorId: 1) {
  	id
  	name
  } 
}
```
Add author
```
mutation {
  addAuthor(name: "new author") {
  	id
  	name
  } 
}
```
