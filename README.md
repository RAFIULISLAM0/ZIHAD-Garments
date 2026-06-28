# Zihad Garments - Garments Management System

A full-featured garments management system built with Laravel 12, Tailwind CSS, and SQLite/MySQL. Designed for small to medium garment factories and retail shops.

## Features

- **Dashboard** - Real-time overview of sales, expenses, stock, and dues
- **Factory Portal** - Fabric in, cutting, production, fabric value, stock value tracking
- **Shop Portal** - Customer management, product catalog, orders/sales, payments
- **Stock Management** - Stock dashboard, movements log, stock-in, adjustments
- **Reports** - Summary, factory, and shop reports with charts
- **AI Features** - AI voice support (simulated), SMS sender with due reminders
- **Invoice Printing** - A4 invoice and thermal memo printing
- **Settings** - Company info, invoice config, shop/factory settings

## Requirements

- PHP 8.2 or higher
- Composer
- SQLite (default) or MySQL/MariaDB
- Node.js & NPM (for frontend assets)

## Installation

### 1. Clone & Install Dependencies

```bash
cd C:\xampp\htdocs\ZIHAIDGARMENTS
composer install
npm install
```

### 2. Environment Setup

```bash
copy .env.example .env
```

Edit `.env` and configure your database. The default uses SQLite:

```
DB_CONNECTION=sqlite
```

For MySQL, uncomment and update:

```
DB_CONNECTION=mysql
DB_HOST=127.0.0.1
DB_PORT=3306
DB_DATABASE=zihad_garments
DB_USERNAME=root
DB_PASSWORD=
```

### 3. Application Key

```bash
php artisan key:generate
```

### 4. Create Database

**For SQLite:** Create an empty file:
```bash
type nul > database\database.sqlite
```

**For MySQL:** Create a database named `zihad_garments` in phpMyAdmin or MySQL CLI.

### 5. Run Migrations & Seeders

```bash
php artisan migrate --seed
```

This will:

- Create all database tables
- Create an admin user
- Add 10 customers
- Add 20 products
- Add 10 orders with items
- Add 10 payments
- Add 10 expenses
- Add 5 fabric in records
- Add 5 cutting records
- Add SMS demo history
- Add voice demo history
- Configure default settings

### 6. Build Frontend Assets

```bash
npm run build
```

### 7. Storage Link

```bash
php artisan storage:link
```

### 8. Start Development Server

```bash
php artisan serve
```

Visit `http://localhost:8000` in your browser.

## Demo Login

| Field    | Value                       |
|----------|-----------------------------|
| Email    | admin@zihadgarments.com     |
| Password | admin123456                 |

## Clean Database (Reset Demo Data)

To reset the database and start fresh:

```bash
php artisan migrate:fresh --seed
```

This drops all tables, re-runs migrations, and re-seeds demo data.

To reset WITHOUT seeders (empty database with only tables):

```bash
php artisan migrate:fresh
```

## Project Structure

```
app/
├── Http/
│   ├── Controllers/       # Application controllers
│   └── Auth/              # Custom authentication
├── Models/                # Eloquent models
├── Providers/             # Service providers
database/
├── migrations/            # Database migrations
├── seeders/               # Database seeders
resources/
├── views/                 # Blade templates
├── css/                   # Tailwind CSS
├── js/                    # JavaScript
routes/
├── web.php                # Web routes
```

## Tech Stack

- **Backend:** Laravel 12
- **Frontend:** Tailwind CSS 4, Alpine.js (via Lucide icons)
- **Charts:** ApexCharts
- **Database:** SQLite / MySQL
