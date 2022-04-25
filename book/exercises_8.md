1.
```sql
ALTER TABLE animals
  ADD COLUMN class varchar(100);
UPDATE animals SET class = 'Aves';
```
2.
```sql
ALTER TABLE animals
  ADD COLUMN phylum varchar(100),
  ADD COLUMN kingdom varchar(100);
UPDATE animals SET phylum = 'Chordata', kingdom = 'Animalia';
```
3.
```sql
ALTER TABLE countries 
  ADD COLUMN continent varchar(50);
UPDATE countries 
SET continent = 'Europe'
WHERE name = 'France' OR name = 'Germany',
SET continent = 'Asia'
WHERE name = 'Japan',
SET continent = 'North America'
WHERE name = 'USA';
```
4.
```sql
UPDATE celebrities 
SET deceased = true
WHERE first_name = 'Elvis';

ALTER TABLE celebrities
  ALTER COLUMN deceased 
    SET NOT NULL;
```
5.
```sql
DELETE FROM celebrities 
WHERE first_name = 'Tom' AND last_name = 'Cruise';
```
6.
```sql
ALTER TABLE celebrities
  RENAME TO singers;
DELETE FROM singers
WHERE occuption NOT LIKE '%Singer%';
```
7.
```sql
DELETE FROM countries
```
8.
```sql
UPDATE orders SET drink = 'Lemonade'
WHERE id = 1;
```
9.
```sql
UPDATE orders SET side = 'Fries', side_cost = 0.99, customer_loyalty_points = 13
WHERE id = 4;
```
10.
```sql
UPDATE orders set side_cost = 1.20
WHERE side = 'Fries'
end
