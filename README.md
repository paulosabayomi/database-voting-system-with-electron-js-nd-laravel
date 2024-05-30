# Voting System API

It is built with Laravel

## Requirements

- Composer >=v2.6.6
- Laravel >=v11
- PHP >=8.2.4

## How to run

- Clone this repository to a directory on your computer
- Install dependencies run:

```bash
composer install
```

- Then create a MySQL database with the name `voting_system` and configure the `.env` file, you can check the laravel documentation on how to configure a `.env` file for database connection or follow the tutorial.
- Then generate the key by running

```bash
php artisan key:generate
```

- Then run the migration with

```bash
php artisan migrate
```

- Then seed the database

```bash
php artisan db:seed
```

This will run the seeder for all the seeder classes, which are `DatabaseSeeder`, `VotesSeeder`, and `CandidatesSeeder`, but because the `VotesSeeder` depends on both the `users` and `candidates` table, you might want to run the seeding serially by running `DatabaseSeeder` and `CandidatesSeeder` before the `VotesSeeder`, example of how to run a seeder class, to run the `CandidatesSeeder` class:

```bash
php artisan db:seed --class=CandidatesSeeder
```

- Then finally start the server with

```bash
php artisan serve
```
