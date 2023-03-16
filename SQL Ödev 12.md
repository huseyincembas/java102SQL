# SQL ÖDEV 12
---
1.  **film** tablosunda film uzunluğu **length** sütununda gösterilmektedir. Uzunluğu ortalama film uzunluğundan fazla kaç tane film vardır?
2.  **film** tablosunda en yüksek rental_rate değerine sahip kaç tane film vardır?
3.  **film** tablosunda en düşük rental_rate ve en düşük replacement_cost değerlerine sahip filmleri sıralayınız.
4.  **payment** tablosunda en fazla sayıda alışveriş yapan müşterileri(customer) sıralayınız.
---
### CEVAPLAR
1. 
```sql 
SELECT COUNT(film_id) FROM film
WHERE length > (
	SELECT AVG(length) FROM film);
```
2. 
```sql 
SELECT COUNT(film_id) FROM film
WHERE rental_rate = (
	SELECT MAX(rental_rate) FROM film
);
```
3. 
```sql 
SELECT * FROM film
WHERE rental_rate = 
	(SELECT MIN(rental_rate) FROM film)
AND replacement_cost = 
	(SELECT MIN(replacement_cost) FROM film);
```
4. 
```sql 
SELECT customer_id, COUNT(payment_id) FROM payment 
GROUP BY customer_id
ORDER BY COUNT DESC;
```