1.
```sql
SELECT population FROM countries WHERE name = 'USA';
```
2.
```sql
SELECT population, capital FROM countries;
```
3.
```sql
SELECT name FROM countries 
ORDER BY name;
```
4.
```sql
SELECT name, capital FROM countries
ORDER BY population;
```
5.
```sql
SELECT name, capital FROM countries
ORDER BY population DESC;
```
6.
```sql
SELECT name, binomial_name, max_weight_kg, max_age_years
FROM animals 
ORDER BY max_age_years, max_weight_kg, name DESC;
```
7.
```sql
SELECT name FROM countries 
WHERE population > 70,000,000;
```
8.
```sql
SELECT name FROM countries
WHERE population > 70,000,000 AND population < 200,000,000;
```
9.
```sql
SELECT first_name, last_name FROM celebrities
WHERE deceased <> true OR deceased IS NULL;
```
10.
```sql
SELECT first_name, last_name FROM celebrities
WHERE occupation LIKE '%Singer%';
```
11.
```sql
SELECT first_name, last_name FROM celebrities
WHERE occupation LIKE '%Actor%' OR occupation LIKE '%Actress%';
```
12.
```sql
SELECT first_name, last_name FROM celebrities
WHERE (occupation LIKE '%Actor%' 
OR occupation LIKE '%Actress%')
AND occupation LIKE '%Singer%';
```
13.
```sql
SELECT burger FROM orders
WHERE burger_cost < 5
ORDER BY burger_cost;
```
14.
```sql
SELECT customer_name, customer_email, customer_loyalty_points FROM orders 
WHERE customer_loyalty_points >= 20 
ORDER BY customer_loyalty_points DESC;
```
15.
```sql
SELECT burger FROM orders 
WHERE customer_name = 'Natasha O''Shea';
```
16.
```sql
SELECT customer_name FROM orders 
WHERE drink IS NULL;
```
17.
```sql
SELECT burger, side, drink FROM orders
where side != 'Fries' OR side IS NULL;
```
18.
```sql
SELECT burger, side, drink FROM orders 
where side IS NOT NULL 
AND drink IS NOT NULL;
```