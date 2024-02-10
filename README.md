# LibraryDB
This database manages information about authors, books, borrowers, genres, and book reviews. It supports queries for retrieving details such as book and author names, borrower information, counting books by authors, updating borrower email addresses, calculating average ratings for each book, and finding books with the highest average ratings. The inclusion of genres, borrowers, and reviews enhances the database's complexity and functionality, making it suitable for applications related to libraries or book management.

Authors:

Stores information about authors.
Columns: author_id (primary key), author_name.
Books:

Represents details about books.
Columns: book_id (primary key), title, author_id (foreign key referencing Authors), genre, publication_year, isbn.
Includes a foreign key constraint linking author_id to Authors(author_id).
Borrowers:

Contains information about individuals borrowing books.
Columns: borrower_id (primary key), name, email, book_id (foreign key referencing Books).
Initially includes a column for borrowed books (borrowed_books), later replaced with a book_id column.
Genres:

Represents different genres.
Columns: genre_id (primary key), genre_name.
BookGenres:

Establishes a many-to-many relationship between books and genres.
Columns: book_id (foreign key referencing Books), genre_id (foreign key referencing Genres).
Reviews:

Captures book reviews and ratings.
Columns: review_id (primary key), book_id (foreign key referencing Books), review_name, rating, review_text.
Queries:
Retrieving Book and Author Names:

Retrieves the names of books along with their respective authors.
Retrieving Borrower Information:

Retrieves borrower names, emails, and the books they borrowed.
Counting Books by Authors:

Calculates the total number of books written by each author.
Updating Borrower Email:

Updates the email address for a specific borrower.
Calculating Average Rating for Each Book:

Calculates the average rating for each book based on reviews.
Finding Books with Highest Average Rating:

Identifies books with the highest average ratings and includes details of reviews contributing to that average.
