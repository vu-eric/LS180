1. 
```sql
INSERT INTO countries (name, capital, population)
VALUES ('France', 'Paris', 67158000);
```
2.
```sql
INSERT INTO countries (name, capital, population)
VALUES ('USA', 'Washington D.C.', 325365189), 
       ('Germany', 'Berlin', 82349400),
       ('Japan', 'Tokyo', 126672000);
```
3.
```sql
INSERT INTO celebrities (first_name, last_name, occupation, date_of_birth)
VALUES ('Bruce', 'Springsteen', 'Singer, Songwriter', '1949-9-23');
```
4.
```sql
INSERT INTO celebrities (first_name, last_name, occupation, date_of_birth)
VALUES ('Scarlett', 'Johansson', 'Actress', '1984-11-22');
```
5.
```sql
  INSERT INTO celebrities (first_name, last_name, occupation, date_of_birth, deceased)
  VALUES ('Frank', 'Sinatra', 'Singer, Actor', '1915-12-12', true),
         ('Tom', 'Cruise', 'Actor', '1962-7-03', false);
```
6. We'll get an error because `last_name` has a `NOT NULL` constraint. 
7.
```sql
  ALTER TABLE celebrities
    ALTER COLUMN last_name DROP NOT NULL;
```
8. We would get a `NULL` value for `deceased`. 
9. 
```sql
ALTER TABLE animals
  DROP CONSTRAINT unique_binomial_name;
```
8.
```sql
INSERT INTO orders (customer_name, customer_email, customer_loyalty_points, burger, side, drink, burger_cost, side_cost, drink_cost)
            VALUES ('James Bergman', 'james1998@email.com', 28, 'LS Chicken Burger', 'Fries', 'Cola', 4.50, 0.99, 1.50),
                   ('Natasha O''Shea', 'natasha@osheafamily.com', 18, 'LS Cheeseburger', 'Fries', NULL, 3.50, 0.99, DEFAULT),
                   ('Natasha O''Shea', 'natasha@osheafamily.com', 42, 'LS Double Deluxe Burger', 'Onion Rings', 'Chocolate Shake', 6.00, 1.50, 2.00),
                   ('Aaron Muller', NULL, 10, 'LS Burger', NULL, NULL, 3.00, DEFAULT, DEFAULT);
```
