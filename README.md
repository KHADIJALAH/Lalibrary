# LaLibrary - Online Bookstore

An online bookstore web application built with PHP, MySQL, and Bootstrap. Users can browse, search, and purchase books from a catalog of 21+ books across 13 categories. Includes an admin panel for full inventory management.

## Features

### For Users
- **Book Browsing** - Browse books in a grid layout with cover images, prices, and details
- **Category Filtering** - Filter books by 13 categories (Romans, Science Fiction, Fantasy, History, etc.)
- **Full-Text Search** - Search books by title, author, or description
- **Book Details** - View complete book information (title, author, price, year, ISBN, quantity, description)
- **Shopping Cart** - Add books to cart and place orders
- **Order History** - View past orders with dates and totals, cancel orders if needed
- **User Authentication** - Register and login with secure bcrypt password hashing

### For Admins
- **Book Management** - Add, modify, and delete books from the catalog (full CRUD)
- **Order Management** - View all customer orders and manage order statuses
- **Inventory Control** - Track book quantities and manage stock

## Tech Stack

- **Backend**: PHP (vanilla, no framework)
- **Database**: MySQL with PDO (prepared statements for SQL injection prevention)
- **Frontend**: Bootstrap 4.5.2, HTML5, CSS3
- **Authentication**: Session-based with bcrypt password hashing
- **Server**: Apache (XAMPP)

## Database Structure

- **users** - User accounts with roles (admin/customer)
- **books** - Book catalog with details and cover images
- **categories** - 13 book categories
- **orders** - Order records with user, book, price, and date

## Getting Started

### Prerequisites

- XAMPP (or any Apache + MySQL + PHP environment)
- PHP 7.0+
- MySQL 5.7+

### Installation

1. **Clone the repository**
   ```bash
   git clone https://github.com/KHADIJALAH/Lalibrary.git
   ```

2. **Create the database**
   - Open phpMyAdmin
   - Create a new database named `webmarket`
   - Import the `lalibrary.sql` file into the database

3. **Configure the database connection**
   - Open `Source code/config.php`
   - Update `$username` and `$password` to match your MySQL server credentials

4. **Deploy the application**
   - Copy the `Source code` folder contents to your XAMPP `htdocs` directory
   - Or use PHP's built-in server:
     ```bash
     cd "Source code"
     php -S localhost:8000
     ```

5. **Start Apache and MySQL** in XAMPP Control Panel

6. **Open in browser**
   - Navigate to `http://localhost/Source code/main.php`
   - Or `http://localhost:8000/main.php` if using PHP's built-in server

### Default Admin Access

Register with an email ending in `@admin.com` to get admin privileges.

## Project Structure

```
Lalibrary/
├── Source code/
│   ├── config.php            # Database connection (PDO)
│   ├── main.php              # Home page - book catalog with search & filters
│   ├── login.php             # User login
│   ├── register.php          # User registration
│   ├── logout.php            # Logout handler
│   ├── details.php           # Book details page
│   ├── panier.php            # Shopping cart & order history
│   ├── addtocart.php         # Add to cart handler
│   ├── ajoutlivre.php        # Admin: Add new book
│   ├── listelivre.php        # Admin: List all books
│   ├── modlivre.php          # Admin: Modify book
│   ├── supplivre.php         # Admin: Delete book
│   ├── listecommande.php     # Admin: View all orders
│   ├── annulercommande.php   # Cancel order
│   ├── aide.php              # Help / About page
│   ├── headers/
│   │   ├── header1.php       # Auth pages header
│   │   ├── header2.php       # Main navigation header
│   │   └── footer.php        # Footer
│   └── images/               # Book cover images
├── lalibrary.sql             # Database schema & seed data
├── LaLibrary.pdf             # Project documentation
├── MLD webmarket.jpg         # Database diagram
└── README.md
```

## Screenshots

### Home Page
- Book grid with cover images, prices, and ratings
- Category sidebar for filtering
- Search bar for finding books

### Book Details
- Full book information with cover image
- Add to cart button for users
- Edit/Delete buttons for admins

### Admin Panel
- Book inventory management
- Order management dashboard

## Author

**Khadija Lahlou** - [GitHub](https://github.com/KHADIJALAH)
