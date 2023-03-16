# SQL ÖDEV 10
---
1.  **city** tablosu ile **country** tablosunda bulunan şehir (city) ve ülke (country) isimlerini birlikte görebileceğimiz LEFT JOIN sorgusunu yazınız.
2.  **customer** tablosu ile **payment** tablosunda bulunan payment_id ile customer tablosundaki first_name ve last_name isimlerini birlikte görebileceğimiz RIGHT JOIN sorgusunu yazınız.
3.  **customer** tablosu ile **rental** tablosunda bulunan rental_id ile customer tablosundaki first_name ve last_name isimlerini birlikte görebileceğimiz FULL JOIN sorgusunu yazınız.
---
### CEVAPLAR
1. 
``` SQL
SELECT country.country, city.city FROM country
LEFT JOIN city ON city.country_id = country.country_id
ORDER BY country;
```
2. 
```sql 
SELECT customer.first_name, customer.last_name, payment.payment_id FROM payment
RIGHT JOIN customer ON payment.customer_id = customer.customer_id
ORDER BY first_name;
```
3. 
```sql 
SELECT customer.first_name, customer.last_name, rental.rental_id FROM customer
FULL JOIN rental ON rental.customer_id = customer.customer_id
ORDER BY first_name;
```