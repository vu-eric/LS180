1. `createdb encyclopedia`, `psql -d encyclopedia`
2. 
```sql 
CREATE TABLE countries (
  id serial,
  name varchar(50) UNIQUE NOT NULL,
  capital varchar(50) NOT NULL,
  population integer
);
```
3.
```sql
CREATE TABLE famous_people (
  id serial, 
  name varchar(100) NOT NULL,
  occupation varchar(150),
  date_of_birth varchar(50),
  deceased boolean DEFAULT false
);
```
4.
```sql
CREATE TABLE animals (
  id serial,
  name varchar(100) NOT NULL,
  binomial_name varchar(100) NOT NULL,
  max_weight_kg decimal(8,3),
  max_age_years integer,
  conservation_status char(2)
);
```

5. `\dt`
6. `\d animals`
7. `CREATE DATABASE ls_burger;`, `\c ls_burger`
8. 
```sql
CREATE TABLE orders (
  id serial,
  customer_name varchar(100) NOT NULL,
  burger varchar(50),
  side varchar(50),
  drink varchar(50),
  order_total decimal(4,2) NOT NULL
);
```