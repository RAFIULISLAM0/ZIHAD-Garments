# Clean Database - Reset Instructions

## Option 1: Full Reset with Demo Data (Recommended)

This drops all tables, re-creates them, and re-seeds all demo data:

```bash
php artisan migrate:fresh --seed
```

After running, you'll have a fresh installation with:

- 1 admin user
- 10 customers
- 20 products
- 10 orders with items
- 10 payments
- 10 expenses
- 5 fabric in records
- 5 cutting records
- 10 SMS logs
- 10 voice commands
- Default settings

## Option 2: Fresh Database (Empty - No Demo Data)

This drops all tables and re-creates them WITHOUT any seed data:

```bash
php artisan migrate:fresh
```

This gives you a completely empty database with only table structures.

After this, if you want demo data later, run:

```bash
php artisan db:seed
```

## Option 3: Reset Specific Tables

If you want to keep some data and reset only specific tables:

```bash
# Reset and re-seed everything
php artisan migrate:fresh --seed

# Or re-run just the seeders (if tables already exist)
php artisan db:seed
```

## Option 4: SQLite Specific

If using SQLite, you can also delete the database file entirely:

```bash
# Delete the SQLite database
del database\database.sqlite

# Create a new empty database file
type nul > database\database.sqlite

# Run migrations and seeders
php artisan migrate --seed
```

## Option 5: MySQL Specific

For MySQL, drop and recreate the database:

```sql
DROP DATABASE zihad_garments;
CREATE DATABASE zihad_garments;
```

Then run:

```bash
php artisan migrate --seed
```

## Verify Clean Database

After reset, verify by:

1. Login with `admin@zihadgarments.com` / `admin123456`
2. Check each module loads without errors
3. Dashboard should show zeros for all stats (before seeding)
4. All lists should be empty (before seeding)
