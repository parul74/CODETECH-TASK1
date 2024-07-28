Name - PARUL SHARMA

Company - CODTECH IT SOLUTION

Domain - PYTHON PROGRAMMING

Duration - JULY 1st,2024 to AUGUST 1st, 2024

OVER-VIEW OF THE PROJECT :-

This Python code implements a Library Management System with different functionalities for managing library items and user interactions. Here's a detailed explanation:

1.  Classes:
      LibraryItem: This is a base class representing a general library item. It defines attributes like item_id, title, author, category, is_checked_out (boolean flag), due_date, and borrower. The __init__ method 
      initializes these attributes for each item.
      Book, Magazine, DVD: These are subclasses of LibraryItem that represent specific types of library items. They inherit attributes and functionalities from LibraryItem. You can add more subclasses (e.g., 
      Audiobook) if needed.

2.  Library Class:
      This class manages the library's collection and user interactions. It has attributes like items (list to store all library items) and fines (dictionary to track overdue fines for borrowers).

   Methods:
      add_item(item): Adds a new library item (item) to the items list and prints a confirmation message.
      checkout_item(item_id, borrower): Attempts to checkout an item based on its ID. It performs the following checks:
      Finds the item by its ID using find_item_by_id.
      If the item exists and is not already checked out, it sets is_checked_out to True, assigns the current date + 14 days (2 weeks) as the due date using datetime.timedelta, and sets the borrower name.
      If the item is unavailable, it prints a message.
      return_item(item_id): Handles returning an item based on its ID. It performs the following:
      Finds the item using find_item_by_id.
      If the item exists and is checked out, it calculates the overdue days (difference between current date and due date) using datetime.datetime.now().
      If the item is overdue, it calculates a fine of $1 per overdue day and adds it to the borrower's fines in the fines dictionary.
      It then updates the item's checkout status (is_checked_out), due date (due_date), and borrower (borrower) to None.
      If the item is not checked out, it prints a message indicating it wasn't borrowed.
      find_item_by_id(item_id): Iterates through the items list and returns the item with the matching ID. If not found, it returns None.
      search_items(query, category=None): Allows searching for library items based on a search query (title or author). It performs a case-insensitive search using lower(). It also accepts an optional category 
      argument to filter results. It returns a list of matching items.
      get_fines(borrower): Retrieves the total overdue fines associated with a borrower's name from the fines dictionary. It returns 0 if there are no fines.

3. Main Program (main function):
      This function creates a Library instance and presents a menu to users for interacting with the system.
      It uses a loop to keep the program running until the user chooses to exit.
      
      The menu offers options to:
      Add a new item (book, magazine, or DVD) by specifying details like ID, title, author, and category.
      Checkout an item by entering its ID and borrower's name.
      Return an item by entering its ID.
      Search for items by title or author (optionally filtered by category).
      View overdue fines for a borrower.
      Exit the program.
      Based on the user's choice, the corresponding method from the Library class is called to perform the desired action.

Overall, this code provides a basic structure for managing a library with different item types, user checkouts, and overdue fine calculations. You can extend this code by adding functionalities like:
User accounts and login system.
Saving library data to a database for persistence.
Implementing more advanced search features.
Generating reports on item usage and fines.









