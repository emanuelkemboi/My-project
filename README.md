# My-project
# HMSCI - Hospital Management System

HMSCI is a PHP hospital management system built with the CodeIgniter framework. It manages hospital operations through separate dashboards for administrators, doctors, patients, nurses, pharmacists, laboratorists, and accountants.

## Main Features

- Role-based login for Admin, Doctor, Patient, Nurse, Pharmacist, Laboratorist, and Accountant users
- Admin dashboard for managing departments, staff, patients, notices, system settings, languages, email templates, and database backup/restore
- Doctor dashboard for managing patients, prescriptions, bed allotments, diagnosis reports, and profile details
- Nurse dashboard for managing patients, beds, bed allotments, blood bank records, blood donors, reports, and profile details
- Pharmacist dashboard for managing medicine categories, medicines, prescriptions, and profile details
- Laboratorist dashboard for managing prescriptions, blood bank records, blood donors, and profile details
- Accountant dashboard for managing invoices, payments, cash payments, and profile details
- Patient dashboard for viewing appointments, prescriptions, doctors, admission history, blood bank details, invoices, payment history, and operation history
- Multi-language support
- Password reset email support
- PayPal library included for payment-related functionality

## Technology Stack

- PHP
- CodeIgniter
- MySQL or MariaDB
- HTML, CSS, and JavaScript
- Template assets stored in the `template/` directory

## Project Structure

```text
HMSCI/
├── application/
│   ├── controllers/        # Application controllers for each user role
│   ├── models/             # Database, email, and language models
│   ├── views/              # Interface files for login and user dashboards
│   ├── libraries/          # Custom libraries, including PayPal
│   └── cache/config/       # Configuration files in this project copy
├── DATABASE FILE/
│   └── hmsci.sql           # Main database import file
├── system/                 # CodeIgniter framework files
├── template/               # CSS, JavaScript, fonts, and images
├── uploads/                # Uploaded images, reports, and related files
├── hmsci (1).sql           # Additional SQL dump copy
└── index.php               # Main front controller
```

## Requirements

- PHP 5.6 or another version compatible with this legacy CodeIgniter project
- MySQL or MariaDB
- Apache, XAMPP, WAMP, Laragon, or another PHP web server
- PHP extensions such as `mysqli`, `mbstring`, and `session`

## Installation

1. Copy the `HMSCI` folder into your web server document root.

   Example for XAMPP:

   ```text
   C:\xampp\htdocs\HMSCI
   ```

2. Start Apache and MySQL.

3. Create a MySQL database named:

   ```text
   hmsci
   ```

4. Import the database file:

   ```text
   DATABASE FILE/hmsci.sql
   ```

5. Check the database configuration file:

   ```text
   application/cache/config/database.php
   ```

   Default database settings in this project are:

   ```text
   hostname: localhost
   username: root
   password:
   database: hmsci
   dbdriver: mysqli
   ```

6. Open the system in your browser:

   ```text
   http://localhost/HMSCI/
   ```

## Default Admin Login

The included SQL dump contains this admin account:

```text
Account Type: Admin
Email: admin@mail.com
Password: Password@123
```

Other sample users are included in the database for doctors, patients, nurses, pharmacists, laboratorists, and accountants.

## Useful URLs

```text
http://localhost/HMSCI/index.php?login
http://localhost/HMSCI/index.php?admin/dashboard
http://localhost/HMSCI/index.php?doctor/dashboard
http://localhost/HMSCI/index.php?patient/dashboard
```

## Configuration Notes

- The default controller is `login`.
- The application uses CodeIgniter query-string URLs such as `index.php?admin/dashboard`.
- The database name used by the included configuration is `hmsci`.
- CSRF protection and global XSS filtering are enabled in the configuration.
- Uploaded files are stored in the `uploads/` directory.

## Troubleshooting

### Database connection error

Make sure MySQL is running, the `hmsci` database exists, and the credentials in `application/cache/config/database.php` are correct.

### Page not found or route issue

Use the query-string URL format used by this project:

```text
index.php?login
index.php?admin/dashboard
```

### Assets not loading

Make sure the folder name in the browser URL matches the folder name inside your web server document root.

### Blank page

Check your PHP version and confirm that required PHP extensions such as `mysqli` are enabled.

## Security Notes

This is a legacy project and should be reviewed before production use.

- Passwords in the sample database are stored as plain text.
- Some sample accounts use simple passwords.
- Review upload, payment, email, and database backup/restore features before public deployment.
- Use HTTPS in production.
- Protect configuration files and upload directories with proper server permissions.

## License

No license file is included in this project copy. Confirm usage rights before distribution or commercial deployment.
