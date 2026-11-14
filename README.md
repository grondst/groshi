# groshi

A command-line expense tracker written in Rust.

`groshi` is designed for a single user, a single currency, and a PostgreSQL database.

This is a personal project built to learn Rust and its ecosystem while tracking my own spending.

## Features

- Add expenses with an amount, category, date, and note.
- List expenses with optional date-range and category filters.
- Remove expenses by ID.
- List and remove categories.

## Usage

```sh
# Add an expense
groshi add <amount> [--category <name>] [--date <YYYY-MM-DD>] [--note <text>]

# Remove an expense
groshi rm <id> [--yes]

# List expenses
groshi list [--from <date>] [--to <date>] [--category <name>]

# List categories
groshi cat list

# Remove a category
groshi cat rm <name>
```

## Build

### Requirements

- Rust and Cargo
- PostgreSQL

Set `DATABASE_URL` to your PostgreSQL connection string:

```sh
export DATABASE_URL=postgres://user:password@localhost/groshi
```

Build the project in release mode:

```sh
cargo build --release
```

