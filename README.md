# BM SACCO Management System

A modern web application for managing Company Employees SACCO (Savings and Credit Cooperative) operations, built with Laravel, Inertia.js, and React.

## Overview

This system streamlines the management of employee savings and credit cooperative activities, including member registration, contribution tracking, loan management, and financial reporting.

## Tech Stack

- **Backend**: PHP 8.4, Laravel 13
- **Frontend**: React 19, Inertia.js v3
- **Styling**: Tailwind CSS 4
- **Testing**: Pest 4, PHPUnit 12
- **Build**: Vite
- **Package Management**: Composer, npm

## Quick Start

### Prerequisites
- PHP 8.4
- Composer
- Node.js 18+
- Database (SQLite/MySQL/PostgreSQL)

### Installation

```bash
# Install dependencies
composer install
npm install

# Set up environment
cp .env.example .env
php artisan key:generate

# Run migrations
php artisan migrate

# Start development server
php artisan serve

# In another terminal, start frontend build
npm run dev
```

### Running Tests

```bash
# Run all tests
php artisan test

# Run with compact output
php artisan test --compact

# Run specific test file
php artisan test --compact tests/Feature/SomeTest.php
```

## Project Structure

```
app/                 - Application logic (controllers, models, requests)
resources/
  ├── js/           - React components and pages
  ├── views/        - Blade templates
  └── css/          - Stylesheets
routes/              - Route definitions
database/
  ├── migrations/   - Database schema
  ├── factories/    - Model factories
  └── seeders/      - Database seeders
tests/               - Test suites (Feature, Unit)
```

## Features

- **Member Management** - Registration, profiles, and termination
- **Contribution Tracking** - Fixed and percentage-based contributions
- **Loan Management** - Eligibility, approval, and repayment tracking
- **Financial Reports** - Savings, interest, and dividend calculations
- **Role-Based Access** - Admin, treasurer, and member roles

## Development Workflow

### Creating New Features

1. Create database migration: `php artisan make:migration`
2. Create model and factory: `php artisan make:model --factory`
3. Create controller: `php artisan make:controller`
4. Create React pages/components as needed
5. Run migrations: `php artisan migrate`
6. Write tests and implement routes
7. Generate Wayfinder types: `php artisan wayfinder:generate`

### Code Quality

```bash
# Format code with Pint
vendor/bin/pint

# Check syntax
php artisan tinker
```

## Documentation

- [SACCO Constitution](docs/SACCO_CONSTITUTION.md) - Complete bylaws and operational guidelines
- Configuration files in `config/` directory

## SACCO Overview

### Objectives

The SACCO aims to:
- Encourage regular savings among members
- Provide affordable and accessible loans
- Promote financial discipline and stability
- Improve the economic well-being of members

### Membership & Contributions

**Eligibility**: All company employees (drivers, security, managers, casual workers)

**Contribution Options**:
- **Fixed**: KES 2,000/month (monthly) or KES 1,000/15 days (casual)
- **Percentage-Based**: 5–10% of earnings (recommended)

### Loan Policy

- **Max Loan**: 3× member's total savings
- **Guarantors**: Minimum 2 required
- **Interest Rate**: 1–2% per month (reducing balance)
- **Repayment**: 3–12 months per loan type

### Management Structure

- **Chairperson** - Oversees operations
- **Treasurer** - Manages finances
- **Secretary** - Maintains records
- **Loan Committee** - Reviews and approves loans

**For complete details, see [docs/SACCO_CONSTITUTION.md](docs/SACCO_CONSTITUTION.md)**

---

## Support

For questions or support, contact the SACCO management team.
