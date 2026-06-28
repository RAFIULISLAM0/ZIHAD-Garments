# Zihad Garments - Final Testing Checklist

## Authentication
- [ ] Login page loads correctly
- [ ] Login with correct credentials works (`admin@zihadgarments.com` / `admin123456`)
- [ ] Login with wrong credentials shows error
- [ ] Logout works
- [ ] Remember me checkbox persists session
- [ ] Demo credentials are visible on login page

## Dashboard
- [ ] Dashboard loads without errors
- [ ] Stats cards show correct numbers
- [ ] Monthly sales chart renders
- [ ] Recent orders table loads
- [ ] Recent payments list loads
- [ ] Quick action buttons work
- [ ] Factory overview panel shows data

## Customers (Buyers)
- [ ] Customer list loads with 10 demo customers
- [ ] Search/filter works
- [ ] Create new customer works
- [ ] Edit customer works
- [ ] View customer profile shows orders & payments

## Products
- [ ] Product list loads with 20 demo products
- [ ] Create new product works
- [ ] Edit product works
- [ ] Categories, sizes, colors display correctly

## Orders / Sales
- [ ] Order list loads with 10 demo orders
- [ ] Create new order works
- [ ] Add multiple items to order
- [ ] Automatic total calculation works
- [ ] Order status changes work
- [ ] Order detail view shows items
- [ ] Sale history loads with filters

## Invoice Printing
- [ ] A4 invoice print works
- [ ] Thermal memo print works

## Payments
- [ ] Payment list loads with 10 demo payments
- [ ] Create new payment works
- [ ] Payment methods display correctly

## Expenses
- [ ] Expense list loads with 10 demo expenses
- [ ] Create new expense works
- [ ] Categories display correctly

## Fabric Management
- [ ] Fabric in list loads with 5 records
- [ ] Create fabric in works
- [ ] Fabric value page shows calculations

## Cutting Management
- [ ] Cutting list loads with 5 records
- [ ] Linked to fabric in and product correctly

## Production Management
- [ ] Production list loads
- [ ] Linked to cutting correctly

## Stock Management
- [ ] Stock dashboard shows products with quantities
- [ ] Stock movements log loads
- [ ] Stock-in works
- [ ] Stock adjustment works

## Stock Value
- [ ] Stock value page shows total inventory value

## Due Management
- [ ] Due dashboard shows all dues
- [ ] Collect due payment works

## Reports
- [ ] Summary reports load with charts
- [ ] Factory reports load
- [ ] Shop reports load

## SMS
- [ ] SMS page loads
- [ ] Send SMS works
- [ ] SMS history shows 10 demo records
- [ ] Due reminder SMS works

## AI Voice
- [ ] AI Voice page loads
- [ ] Simulate voice command works
- [ ] Demo command history shows 10 records

## Settings
- [ ] Settings page loads
- [ ] Company settings save correctly
- [ ] Invoice settings save correctly
- [ ] Shop/factory settings save correctly
- [ ] System settings save correctly
- [ ] Admin profile update works

## Navigation
- [ ] All sidebar links navigate correctly
- [ ] No broken links (404 errors)
- [ ] Dashboard link works

## Responsiveness
- [ ] Page works on desktop (1920x1080)
- [ ] Sidebar collapses appropriately

## Data Integrity
- [ ] No duplicate records in any table
- [ ] Foreign key relationships are correct
- [ ] All seeders ran without errors
- [ ] Order totals match item calculations
