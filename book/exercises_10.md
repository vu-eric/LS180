1.
```sql
SELECT countries.name, continents.continent_name
FROM countries 
JOIN continents 
ON countries.continent_id = continents.id;
```
2.
```sql
SELECT countries.name, countries.capital
FROM countries JOIN continents
ON countries.continent_id = continents.id
WHERE continents.continent_name = 'Europe';
```
3.
```sql
SELECT DISTINCT singers.first_name
FROM singers JOIN albums
ON singers.id = albums.singer_id
WHERE albums.label LIKE '%Warner Bros%';
```
4.
```sql
SELECT singers.first_name, singers.last_name, albums.album_name, albums.released
FROM singers JOIN albums
ON singers.id = albums.singer_id
WHERE singers.deceased = false 
AND datepart('year', albums.released) LIKE '18%'
ORDER BY singers.date_of_birth DESC;
```
5.
```sql
SELECT singers.first_name, singers.last_name
FROM singers LEFT JOIN albums
ON singers.id = albums.singer_id
WHERE albums.id IS NULL;
```
6.
```sql
SELECT first_name, last_name 
FROM singers
WHERE id NOT IN (
  SELECT singer_id FROM albums
);
```
7.
```sql
SELECT orders.*, products.*
FROM orders JOIN order_items
ON orders.id = order_items.order_id 
JOIN products 
ON order_items.product_id = products.id;
```
8.
```sql
select o.id
from orders o join order_items i
on o.id = i.order_id 
join products p
on i.product_id = p.id
where p.product_name = 'fries';
```
9.
```sql
select DISTINCT c.customer_name AS "Customers who like Fries"
from customers as c join orders o 
on c.id = o.customer_id 
join order_items i
on o.id = i.order_id 
join products p
on i.product_id = p.id
where p.product_name = 'fries';
```
10.
```sql
SELECT sum(p.product_cost) 
from customers as c join orders o 
on c.id = o.customer_id 
join order_items i
on o.id = i.order_id 
join products p
on i.product_id = p.id
where c.customer_name = 'Natasha O''Shea';
```
11.
```sql
SELECT p.product_name, count(oi.id)
FROM products AS p JOIN order_items AS oi
ON p.id = oi.product_id
GROUP BY p.product_name
ORDER BY p.product_name ASC;
```