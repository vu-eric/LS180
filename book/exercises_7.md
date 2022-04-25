1.
```sql
SELECT * FROM countries 
LIMIT 1;
```
2.
```sql
SELECT name FROM countries
ORDER BY population DESC
LIMIT 1;
```
3.
```sql
SELECT name FROM countries
ORDER BY population DESC
LIMIT 1 OFFSET 1;
```
4.
```sql
SELECT DISTINCT binomial_name FROM animals;
```
5.
```sql
SELECT binomial_name FROM animals
ORDER BY length(binomial_name) DESC
LIMIT 1;
```
6.
```sql
SELECT first_name FROM celebrities
WHERE date_part('year', date_of_birth) = 1958;
```
7.
```sql
SELECT max(max_age_years) FROM animals;
```
8.
```sql
SELECT avg(max_weight_kg) FROM animals;
```
9.
```sql
SELECT count(id) FROM countries;
```
10.
```sql
SELECT sum(population) FROM countries;
```
11.
```sql
SELECT conservation_status, count(id) FROM animals
GROUP BY conservation_status;
```
12.
```sql
SELECT avg(burger_cost) FROM orders
WHERE side = 'Fries';
```
13.
```sql
SELECT min(side_cost) FROM orders
WHERE side IS NOT NULL;
```
14.
```sql
SELECT side, count(id) FROM orders
WHERE side = 'Fries' OR side = 'Onion Rings'
GROUP BY side;
```