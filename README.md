# Technical Formative Assessment 7 (Module 7)
## Forms, Validation, and File Upload (Laravel POS)

## Project Description

This Laravel 12 Point of Sale application demonstrates database-backed customer and user management. It includes create and edit forms, server-side validation, clear validation feedback, and preservation of submitted form values. User profiles support validated avatar uploads, display-ready 200 × 200 thumbnails, public storage, and a placeholder image when no avatar is available.

## Student Information

- **Name:** Juraly Siray
- **Section:** BSIT-DW31-1
- **Professor:** Tio, Rene Christopher

## Features Implemented

- Customer Create
- Customer Edit
- Customer Validation
- User Create
- User Edit
- User Validation, including unique usernames
- Avatar Upload
- Avatar Validation (image file, maximum 2 MB)
- Thumbnail Generation (200 × 200 JPEG)
- `Storage::disk('public')` for avatar storage
- Validation Error Display
- `old()` Input Preservation
- Placeholder avatar for users without an uploaded image

## System Requirements

- PHP 8.2+
- Composer
- MySQL
- Laravel 12
- PHP GD extension for image processing

## Installation

From the project directory, install dependencies and prepare the local environment:

```sh
composer install
cp .env.example .env
php artisan key:generate
```

If `.env` already exists, keep it and update its settings rather than overwriting it.

## Database Setup

Create a MySQL database (the default project configuration uses `pos`) and configure the database connection in `.env`:

```dotenv
DB_CONNECTION=mysql
DB_HOST=127.0.0.1
DB_PORT=3306
DB_DATABASE=pos
DB_USERNAME=root
DB_PASSWORD=
```

Apply the database migrations:

```sh
php artisan migrate
```

To also insert the sample records, run:

```sh
php artisan db:seed
```

## Storage Setup

Create Laravel's public storage link so uploaded avatars can be served by the application:

```sh
php artisan storage:link
```

## Run Application

Start the local Laravel development server:

```sh
php artisan serve
```

Open [http://127.0.0.1:8000](http://127.0.0.1:8000). Customer records are managed at `/customers`; user records are managed at `/users`.

## Testing

Run the complete feature test suite:

```sh
composer test
```

## TFA7 Verification Results

Verified for this project:

- **13 application routes** registered.
- **13 tests passed.**
- **72 assertions passed.**
- Avatar upload and public-disk storage verified by feature tests.
- 200 × 200 thumbnail generation verified by feature tests.
- Invalid and oversized avatar uploads rejected by validation tests.

## GitHub Repository

[current Link]

## Hosted Application

[Not Yet]

## Author

[Student#:202410268-Juraly Siray]
