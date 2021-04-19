# Day 2 - USING AN ORM TO INTERACT WITH A DATABASE
## Daily Journal
Read Servers with Node/Express > MongoDb Relationships and answer the following questions
## What are the three types of relationships?
One-to-One, One-to-Many, Many-to-Many
## What are the benefits of the traditional linking of relationships instead of Embedding
    Traditional linking is useful for one-to-many relationship because if you simply tried to embed then the document would become extremely long and become very hard to read. By linking you simply create a reference to the object which is easier to read, understand and search for.

## What are some of the challenges faced when deciding how to manage a many-to-many relationship that ultimately drive your decision on how to create it?
    The first challenge is desiding which side will be referenced over the other, the example makes a lot of sense.One book will have differnt genres but one genre will have tons of books, it makes sense to put the "foreign key" on the side of the books.
## Afternoon Challenge
    https://kpohiostyle.github.io/gregslist/