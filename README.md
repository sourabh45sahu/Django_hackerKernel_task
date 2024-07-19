# Django_hackerKernel_task
# Library Management System

This is a Django web application to manage an online library system where admins can manage books, authors, and their borrow records. The application allows admins to add books, authors, and assign books to authors. Additionally, admins can export the library data to an Excel sheet.

## Features

- Add, edit, and delete authors
- Add, edit, and delete books
- Add, edit, and delete borrow records
- Paginated list views for authors, books, and borrow records
- Export data to Excel file with separate sheets for authors, books, and borrow records
- Form validation for email field
- Error handling and user notifications
- Responsive design using custom CSS

## Models

### Author
- `name`: CharField
- `email`: EmailField
- `bio`: TextField

### Book
- `title`: CharField
- `genre`: CharField
- `published_date`: DateField
- `author`: ForeignKey to Author

### BorrowRecord
- `user_name`: CharField
- `book`: ForeignKey to Book
- `borrow_date`: DateField
- `return_date`: DateField

## Installation

1. Clone the repository:
    ```sh
    git clone https://github.com/yourusername/library-management-system.git
    cd library-management-system
    ```

2. Create and activate a virtual environment:
    ```sh
    python -m venv venv
    source venv/bin/activate  # On Windows use `venv\Scripts\activate`
    ```

3. Install the dependencies:
    ```sh
    pip install -r requirements.txt
    ```

4. Apply the migrations:
    ```sh
    python manage.py makemigrations
    python manage.py migrate
    ```

5. Create a superuser:
    ```sh
    python manage.py createsuperuser
    ```

6. Run the development server:
    ```sh
    python manage.py runserver
    ```



