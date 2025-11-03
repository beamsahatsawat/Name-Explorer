# Name Explorer

A PHP web application for exploring and discovering names. Features include name search, meaning lookup, and character-based name browsing with a clean, simple interface.

## Features

- Name search functionality
- Detailed name information and meanings
- Character/letter-based name browsing
- Clean and responsive design
- Simple and intuitive user interface

## Technologies Used

- PHP
- MySQL/MariaDB
- HTML5
- CSS3 (with Simple.css framework)
- SVG Graphics

## Project Structure

```
├── data/
│   └── names.sql         # Database schema and data
├── images/              # Image assets
├── inc/
│   ├── all.inc.php      # Global includes
│   ├── db-connect.inc.php # Database connection
│   ├── functions.inc.php  # Helper functions
│   └── names.inc.php     # Name-related functions
├── styles/
│   ├── custom.css       # Custom styling
│   └── simple.css       # Base CSS framework
├── views/
│   ├── layouts/
│   │   └── main.view.php # Main layout template
│   └── pages/
│       ├── char.view.php  # Character browse view
│       ├── index.view.php # Homepage view
│       └── name.view.php  # Name details view
├── char.php             # Character browse controller
├── index.php           # Main entry point
└── name.php            # Name details controller
```

## Setup

1. Clone the repository
2. Import the database schema from `data/names.sql`
3. Configure database connection in `inc/db-connect.inc.php`
4. Point your web server to the project directory
5. Access the application through your web browser

## Requirements

- PHP 7.4 or higher
- MySQL/MariaDB
- Web server (Apache/Nginx)

## License

MIT License

## Author

beamsahatsawat
