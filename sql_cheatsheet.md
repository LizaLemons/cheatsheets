
# SQL cheatsheet

---


### Installation

- Follow the directions here to download the native OSX PostgreSQL app:
  - http://postgresapp.com/
- Afterwards, you should see the happy elephant in your toolbar.


---


### PostgreSQL official docs

- http://www.postgresql.org/docs/9.1/static/index.html


---

## Style Guide

- Use lowercase `snake_case` for most components
- Table names should be plural: `library_branches`
- Join tables for many-to-many relationships:
  - e.g.: `artist_song_maps`
  - Formula:
  - `<singular table name of entity A> _ <singular table name of entity B> _maps`
  - Put table names in alphabetical order
  - This table is a collection of mappings between the two tables.


---


### Commands

- In general below, everything that is in `ALL CAPS` is `SQL` and anything with the format `\command` is `psql`


---


### Start up psql

- Drop into psql from anywhere in your terminal: `psql`
- Or, drop into a specific DB: `psql -d name_of_database`
- Exit psql: `\q`


---


### Help

- General help: `help`
- Help with psql commands: `\?`
- Help with SQL commands: `\h`


---


### PostgreSQL level

- Show all databases: `\l`
- Create database: `CREATE DATABASE liza_tester_db;`
- Connect to specific database: `\c liza_tester_db`
- Drop database: `DROP DATABASE liza_tester_db;`


---


### Database level

- List all tables: `\d`
- Create a table with columns:
```
CREATE TABLE students (
    id SERIAL PRIMARY KEY,
    first_name VARCHAR,
    last_name VARCHAR,
    quote TEXT,
    birthday VARCHAR,
    ssn INT UNIQUE,
    is_admin BOOLEAN
);
```
- Drop a table: `DROP TABLE students;`


---


### Table level

- See all **columns** in a specific table: `\d <table_name>`
- See all **rows** of a table: `SELECT * FROM users;`


---


# CRUD actions


---


### Find

- Select all columns from all rows:
  - `SELECT * FROM STUDENTS;`
- Select only some columns, from all rows:
  - `SELECT first_name, last_name FROM students;`
- Select all columns from row that meets specific criteria:
  - `SELECT * FROM students WHERE first_name='Liza';`
- Select some columns from certain rows:
  - `SELECT name FROM students WHERE id=2;`


---


### Insert

- Insert one:
  - `INSERT INTO students (first_name, last_name, quote, birthday, ssn, is_admin) VALUES ('Liza', 'ramo', 'hello', 'nov 15', 87654, TRUE);`
- Insert one without quote, birthday, ssn:
  - `INSERT INTO students (first_name, last_name) VALUES ('Ethan', 'Friedman');`


---


### Update

- `UPDATE students SET first_name='Loki' WHERE first_name='Liza';`
- `UPDATE students SET first_name='Adam B.', ssn=1986 WHERE name='Adam Bray';`


---


### Delete

- `DELETE FROM students WHERE first_name='Loki';`


---


### Joins

- Examples of querying two tables at once:
  - `SELECT * FROM weather, cities WHERE city = name;`
- Find all books written by any author from the USA
  - `SELECT * FROM books JOIN authors on books.author_id = authors.id WHERE authors.nationality='United States of America';`




---
