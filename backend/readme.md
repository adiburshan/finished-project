## Library Management System

This is a Flask-based web application for managing a library system, allowing users to register, login, borrow and return books.
manage customers, books and loans data in DB. 
It includes features for both administrators and regular users.
Uses RestAPI for communication
DB- Sqlalchemy

Before you will start:
1. create virtual environment 
2. activate the virtual environment
3. install all the requirements ('pip install -r requirements.txt')


# Content of the app.py:
 create tables (library.db):
 1. Customers table
 2. Books table
 3. Loans table


 create endpoints for register, login and logout:
 Register
Endpoint: /register
Method: POST
Description: Allows a user to register with the system by providing necessary details.

Login
Endpoint: /login
Method: POST
Description: Allows a registered user to login and obtain an access token for authentication.

Logout
Endpoint: /logout
Method: POST
Description: Logs out the currently logged-in user by blacklisting their JWT token.

Account Information
Endpoint: /account
Method: GET
Description: Shows the details of the currently logged-in user.


for admin only:

-Book Operations-
Add Book
Endpoint: /add_book
Method: POST
Description: Allows an admin user to add a new book to the library database.

Show All Books
Endpoint: /admin_show_books
Method: GET
Description: Shows a list of all books (available and not available) in the library.

Delete Book
Endpoint: /delete_book/<book_id>
Method: DELETE
Description: Marks a book as inactive (soft delete) in the database.

Update Book
Endpoint: /update_book/<book_id>
Method: PUT
Description: Allows an admin user to update the details of a book in the library.

-Customer Operations-
Show All Customers
Endpoint: /show_customers
Method: GET
Description: Shows a list of all customers registered in the system.

Delete Customer
Endpoint: /delete_customer/<customer_id>
Method: DELETE
Description: Marks a customer as not active (soft delete) in the database.

Update Customer
Endpoint: /update_customer/<customer_id>
Method: PUT
Description: Allows an admin user to update the details of a customer.

-Loan Operations-
Show All Loans
Endpoint: /all_loans
Method: GET
Description: Shows a list of all loans in the library.

Show Late Loans
Endpoint: /all_late_loans
Method: GET
Description: Shows a list of all loans that are overdue.


for all customers:
Show All Books
Endpoint: /show_books
Method: GET
Description: Shows a list of all books (available and not available) in the library.

Loan Book
Endpoint: /loan_book/<book_title>
Method: POST
Description: Allows a user to borrow a book from the library.

Return Book
Endpoint: /return_book/<loan_id>
Method: PUT
Description: Allows a user to return a borrowed book to the library.

Show My Loans
Endpoint: /my_loans
Method: GET
Description: Shows a list of all books currently loaned by the logged-in user.

Update Customer Information
Endpoint: /update_customer_info
Method: PUT
Description: Updates the information of the currently logged-in customer.
Authentication: Requires JWT token.

Show My Late Loans
Endpoint: /my_late_loans
Method: GET
Description: Shows late loans for the currently logged-in customer.


# media library
saves the images of the books 

