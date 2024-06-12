<p align="center"><a href="https://laravel.com" target="_blank"><img src="https://raw.githubusercontent.com/laravel/art/master/logo-lockup/5%20SVG/2%20CMYK/1%20Full%20Color/laravel-logolockup-cmyk-red.svg" width="400" alt="Laravel Logo"></a></p>

<p align="center">
<a href="https://github.com/laravel/framework/actions"><img src="https://github.com/laravel/framework/workflows/tests/badge.svg" alt="Build Status"></a>
<a href="https://packagist.org/packages/laravel/framework"><img src="https://img.shields.io/packagist/dt/laravel/framework" alt="Total Downloads"></a>
<a href="https://packagist.org/packages/laravel/framework"><img src="https://img.shields.io/packagist/v/laravel/framework" alt="Latest Stable Version"></a>
<a href="https://packagist.org/packages/laravel/framework"><img src="https://img.shields.io/packagist/l/laravel/framework" alt="License"></a>
</p>

## About Laravel

Laravel is a web application framework with expressive, elegant syntax. We believe development must be an enjoyable and creative experience to be truly fulfilling. Laravel takes the pain out of development by easing common tasks used in many web projects, such as:

- [Simple, fast routing engine](https://laravel.com/docs/routing).
- [Powerful dependency injection container](https://laravel.com/docs/container).
- Multiple back-ends for [session](https://laravel.com/docs/session) and [cache](https://laravel.com/docs/cache) storage.
- Expressive, intuitive [database ORM](https://laravel.com/docs/eloquent).
- Database agnostic [schema migrations](https://laravel.com/docs/migrations).
- [Robust background job processing](https://laravel.com/docs/queues).
- [Real-time event broadcasting](https://laravel.com/docs/broadcasting).

Laravel is accessible, powerful, and provides tools required for large, robust applications.

## Learning Laravel

Laravel has the most extensive and thorough [documentation](https://laravel.com/docs) and video tutorial library of all modern web application frameworks, making it a breeze to get started with the framework.

You may also try the [Laravel Bootcamp](https://bootcamp.laravel.com), where you will be guided through building a modern Laravel application from scratch.

If you don't feel like reading, [Laracasts](https://laracasts.com) can help. Laracasts contains thousands of video tutorials on a range of topics including Laravel, modern PHP, unit testing, and JavaScript. Boost your skills by digging into our comprehensive video library.

## Laravel Sponsors

We would like to extend our thanks to the following sponsors for funding Laravel development. If you are interested in becoming a sponsor, please visit the [Laravel Partners program](https://partners.laravel.com).

### Premium Partners

- **[Vehikl](https://vehikl.com/)**
- **[Tighten Co.](https://tighten.co)**
- **[WebReinvent](https://webreinvent.com/)**
- **[Kirschbaum Development Group](https://kirschbaumdevelopment.com)**
- **[64 Robots](https://64robots.com)**
- **[Curotec](https://www.curotec.com/services/technologies/laravel/)**
- **[Cyber-Duck](https://cyber-duck.co.uk)**
- **[DevSquad](https://devsquad.com/hire-laravel-developers)**
- **[Jump24](https://jump24.co.uk)**
- **[Redberry](https://redberry.international/laravel/)**
- **[Active Logic](https://activelogic.com)**
- **[byte5](https://byte5.de)**
- **[OP.GG](https://op.gg)**

## Contributing

Thank you for considering contributing to the Laravel framework! The contribution guide can be found in the [Laravel documentation](https://laravel.com/docs/contributions).

## Code of Conduct

In order to ensure that the Laravel community is welcoming to all, please review and abide by the [Code of Conduct](https://laravel.com/docs/contributions#code-of-conduct).

## Security Vulnerabilities

If you discover a security vulnerability within Laravel, please send an e-mail to Taylor Otwell via [taylor@laravel.com](mailto:taylor@laravel.com). All security vulnerabilities will be promptly addressed.

## License

The Laravel framework is open-sourced software licensed under the [MIT license](https://opensource.org/licenses/MIT).

# Laravel API with Sanctum

This repository contains the source code for the Laravel API project using Sanctum, following the "[Laravel API Crash Course With Sanctum](https://www.youtube.com/watch?v=TzAJfjCn7Ks)" by Code With Dary. This project demonstrates how to implement authentication for SPAs, mobile applications, and simple API tokens using Laravel Sanctum.

## Table of Contents
- [Introduction](#introduction)
- [Features](#features)
- [Installation](#installation)
- [Usage](#usage)
- [API Endpoints](#api-endpoints)
- [Technologies](#technologies)

## Introduction
This project serves as a comprehensive tutorial on setting up and using Laravel Sanctum for API authentication. It covers everything from setting up a Laravel project to implementing user authentication, protecting routes, and managing tasks.

## Features
- User Registration and Authentication
- API Token Generation and Revocation
- Protected Routes
- CRUD Operations for Tasks

## Installation
To run this project locally, follow these steps:

1. Clone the repository:
    ```bash
    git clone https://github.com/diandrarad/Laravel-API-with-Sanctum.git
    cd laravel-api-with-sanctum
    ```

2. Install dependencies:
    ```bash
    composer install
    npm install
    ```

3. Copy the example environment file and configure the environment variables:
    ```bash
    cp .env.example .env
    ```

4. Generate the application key:
    ```bash
    php artisan key:generate
    ```

5. Set up the database:
    - Create a MySQL database.
    - Update the `.env` file with your database credentials.

6. Run the migrations:
    ```bash
    php artisan migrate
    ```

7. Start the local development server:
    ```bash
    php artisan serve
    ```

8. Compile the assets:
    ```bash
    npm run dev
    ```

## Usage
After setting up the project, you can use Postman or any other API client to interact with the API. The available endpoints and their functionalities are described below.

## API Endpoints

### Authentication
- **Register**: `POST /api/register`
    - Request: 
        ```json
        {
            "name": "John Doe",
            "email": "john@example.com",
            "password": "password"
        }
        ```
    - Response:
        ```json
        {
            "success": true,
            "data": {
                "user": {
                    "id": 1,
                    "name": "John Doe",
                    "email": "john@example.com",
                    "created_at": "2024-06-09T12:00:00.000000Z",
                    "updated_at": "2024-06-09T12:00:00.000000Z"
                },
                "token": "your-api-token"
            }
        }
        ```

- **Login**: `POST /api/login`
    - Request: 
        ```json
        {
            "email": "john@example.com",
            "password": "password"
        }
        ```
    - Response:
        ```json
        {
            "success": true,
            "data": {
                "user": {
                    "id": 1,
                    "name": "John Doe",
                    "email": "john@example.com",
                    "created_at": "2024-06-09T12:00:00.000000Z",
                    "updated_at": "2024-06-09T12:00:00.000000Z"
                },
                "token": "your-api-token"
            }
        }
        ```

- **Logout**: `POST /api/logout`
    - Header: `Authorization: Bearer {token}`
    - Response:
        ```json
        {
            "success": true,
            "data": {
                "message": "You have successfully been logged out and your token has been deleted"
            }
        }
        ```

### Tasks
- **Get All Tasks**: `GET /api/tasks`
    - Header: `Authorization: Bearer {token}`
    - Response:
        ```json
        [
            {
                "id": 1,
                "user_id": 1,
                "name": "Task 1",
                "description": "Description 1",
                "priority": "High",
                "created_at": "2024-06-09T12:00:00.000000Z",
                "updated_at": "2024-06-09T12:00:00.000000Z"
            },
            ...
        ]
        ```

- **Create Task**: `POST /api/tasks`
    - Header: `Authorization: Bearer {token}`
    - Request: 
        ```json
        {
            "name": "New Task",
            "description": "New Description",
            "priority": "High"
        }
        ```
    - Response:
        ```json
        {
            "data": {
                "id": 1,
                "user_id": 1,
                "name": "New Task",
                "description": "New Description",
                "priority": "High",
                "created_at": "2024-06-09T12:00:00.000000Z",
                "updated_at": "2024-06-09T12:00:00.000000Z"
            }
        }
        ```

- **Get Task by ID**: `GET /api/tasks/{id}`
    - Header: `Authorization: Bearer {token}`
    - Response:
        ```json
        {
            "data": {
                "id": 1,
                "user_id": 1,
                "name": "Task 1",
                "description": "Description 1",
                "priority": "High",
                "created_at": "2024-06-09T12:00:00.000000Z",
                "updated_at": "2024-06-09T12:00:00.000000Z"
            }
        }
        ```

- **Update Task**: `PUT /api/tasks/{id}`
    - Header: `Authorization: Bearer {token}`
    - Request:
        ```json
        {
            "name": "Updated Task",
            "description": "Updated Description",
            "priority": "Medium"
        }
        ```
    - Response:
        ```json
        {
            "data": {
                "id": 1,
                "user_id": 1,
                "name": "Updated Task",
                "description": "Updated Description",
                "priority": "Medium",
                "created_at": "2024-06-09T12:00:00.000000Z",
                "updated_at": "2024-06-09T12:00:00.000000Z"
            }
        }
        ```

- **Delete Task**: `DELETE /api/tasks/{id}`
    - Header: `Authorization: Bearer {token}`
    - Response:
        ```json
        {
            "success": true,
            "message": "Task deleted"
        }
        ```

## Technologies
- Laravel
- PHP
- MySQL
- Laravel Sanctum
- Composer
- NPM