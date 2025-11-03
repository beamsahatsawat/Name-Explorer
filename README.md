# Name Explorer

A small PHP web app to explore and display names. This repository contains PHP views, includes, styles, and a SQL dump of names used by the app.

## Overview

- Entry points: `index.php`, `name.php`, `char.php`.
- Views are under `views/` with layout and page templates.
- PHP include files live in `inc/` (database connect, helper functions, name handling).
- Database SQL dump: `data/names.sql` (tracked in repo).
- Static assets: `images/`, `styles/`.

## Files of note

- `index.php` — main homepage entry.
- `name.php` — page for individual name details.
- `char.php` — character lookup page.
- `inc/db-connect.inc.php` — update DB credentials here (or use environment variables if configured).
- `data/names.sql` — SQL dump containing names; this file is intentionally tracked in the repo.

## Requirements

- PHP 7.4+ (or later)
- MySQL / MariaDB for importing `data/names.sql`
- A web server (Apache, Nginx) or PHP built-in server for local testing

## Quick setup (local development)

1. Import the database dump into a local MySQL database:

```bash
# Create a database first (example name: name_explorer)
mysql -u root -p -e "CREATE DATABASE IF NOT EXISTS name_explorer CHARACTER SET utf8mb4 COLLATE utf8mb4_unicode_ci;"
# Import the SQL dump
mysql -u root -p name_explorer < "data/names.sql"
```

2. Update database credentials in `inc/db-connect.inc.php` (or set up environment variables if your project reads them).

3. Start the built-in PHP server for quick testing (from the repo root):

```bash
php -S localhost:8000
```

Then open http://localhost:8000 in your browser.

If you use a different document root or `index.php` routing, adjust the `-t` option accordingly.

## Notes

- `data/names.sql` is tracked intentionally so the repository contains the dataset needed for development and testing.
- `.gitignore` excludes `vendor/`, logs, caches, and common IDE files but does not ignore `data/*.sql`.
- If you plan to add user uploads or large generated assets, consider adding those paths to `.gitignore`.

## Tests

There are no automated tests included. If you add tests, include instructions here.

## Contributing

Open an issue or create a pull request with proposed changes. Keep changes small and focused.

## License

Add your license here (e.g., MIT). If you don't have one yet, consider adding an appropriate open-source license.

## Contact

Mention contact or maintainer info here if desired.
