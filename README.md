# Barangay Fiscal Portal

A comprehensive fiscal transparency portal for Barangay Del Remedio, San Pablo City, Laguna.

## Features

- **Public Dashboard**: View budget allocations, tax information, and project timelines
- **User Authentication**: Registration and login system
- **Admin Panel**: Manage taxes, projects, users, and generate reports
- **Tax Management**: Track and manage various tax types (Property, Business, Community, Professional)
- **Project Tracking**: Monitor project progress and expenditures
- **Budget Allocation**: Track budget distribution across different sectors

## Setup Instructions

### 1. Prerequisites

- XAMPP (or similar PHP/MySQL environment)
- PHP 7.4 or higher
- MySQL 5.7 or higher
- Apache web server

### 2. Installation

1. Place all files in your web server directory (e.g., `C:\xampp\htdocs\Tax`)

2. Start XAMPP Control Panel and start Apache and MySQL services

3. Open your browser and navigate to:
   ```
   http://localhost/Tax/setup_database.php
   ```

4. This will create the database and all necessary tables automatically.

5. Once setup is complete, delete or secure the `setup_database.php` file for security.

### 3. Default Admin Credentials

After database setup, you can login with:

- **Username**: `admin`
- **Password**: `admin123`

**⚠️ IMPORTANT**: Change the admin password immediately after first login!

### 4. Access the Application

- **Homepage**: `http://localhost/Tax/index.php`
- **Admin Dashboard**: `http://localhost/Tax/dashboard.php`
- **User Dashboard**: `http://localhost/Tax/dashboardd.php`

## Database Structure

The database includes the following tables:

- `users` - User accounts (admin and regular users)
- `properties` - Property records
- `tax_types` - Different types of taxes
- `tax_records` - Tax payment records
- `projects` - Project information and tracking
- `budget_allocation` - Budget distribution by sector
- `expenditures` - Expense records
- `settings` - System settings

## File Structure

```
Tax/
├── index.php              # Main homepage
├── config.php            # Database configuration
├── auth.php              # Authentication functions
├── login.php             # Login handler
├── register.php          # Registration handler
├── logout.php            # Logout handler
├── dashboard.php         # Admin dashboard
├── dashboardd.php        # User dashboard
├── taxes.php             # Tax management (admin)
├── projects.php          # Project management (admin)
├── users.php             # User management (admin)
├── reports.php           # Reports (admin)
├── profile.php           # User profile
├── database_schema.sql   # Database schema
├── setup_database.php    # Database setup script
└── README.md            # This file
```

## Configuration

Edit `config.php` to change database connection settings:

```php
$host = 'localhost';
$dbname = 'barangay_fiscal_portal';
$username = 'root';
$password = '';
```

## Security Notes

1. Change default admin password immediately
2. Keep `setup_database.php` secured or deleted after setup
3. Update database credentials in production
4. Ensure proper file permissions on the server
5. Use HTTPS in production environment

## Support

For issues or questions, please contact the development team.

## License

This project is developed for Barangay Del Remedio, San Pablo City, Laguna.

