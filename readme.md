# Project Overview

Develop a link-shortening application implemented in Laravel.

## Installation

```bash
git clone 
cd url-shortener
composer install
npm install
npm run dev
cp .env.example .env
php artisan key:generate
```

Update database credentials in the `.env` file as needed.

```bash
php artisan migrate
php artisan serve
```

Then you can visit the URL shortener at `http://127.0.0.1:8000`.

## Usage

This application is accessible in both logged-in and logged-out states. For full functionality, including private URL creation and statistics, logging in is recommended.

### Features

- Full registration and login system (Used Laravel's built in functionality)
- Comprehensive form validation
- Basic URL analytics
- Basic admin panel for user and URL management

## Admin User

There is no option to create an admin user via the UI. To gain admin access, you need to update the `is_admin` field directly in the users table in the database.

Alternatively, you can create an admin user by running `php artisan db:seed`, which creates a default admin account with the following credentials:

| Field    | Value           |
|----------|-----------------|
| Name     | Admin User      |
| Email    | admin@url.com   |
| Password | password        |

## Libraries Used

- **jenssegers/agent**: Used to detect and retrieve information about the user's device, which can be useful for analytics and security.


