# SQL ÖDEV 7
---
1.  **film** tablosunda bulunan filmleri **rating** değerlerine göre gruplayınız.
2.  **film** tablosunda bulunan filmleri **replacement_cost** sütununa göre grupladığımızda film sayısı 50 den fazla olan replacement_cost değerini ve karşılık gelen film sayısını sıralayınız.
3. **customer** tablosunda bulunan store_id değerlerine karşılık gelen müşteri sayılarını nelerdir? 
4. **city** tablosunda bulunan şehir verilerini **country_id** sütununa göre gruplandırdıktan sonra en fazla şehir sayısı barındıran country_id bilgisini ve şehir sayısını paylaşınız.
---
### CEVAPLAR

1. 
``` SQL
SELECT rating, COUNT(*) FROM film
GROUP BY rating
ORDER BY COUNT(*) DESC;
```
2. 
``` SQL
SELECT replacement_cost, COUNT(*) FROM film
GROUP BY replacement_cost
HAVING COUNT(*) > 50
ORDER BY replacement_cost DESC;
```
3. 
```SQL
SELECT store_id, COUNT(customer_id) FROM customer
GROUP BY store_id;
```
4. 
``` SQL
SELECT country_id, COUNT(city_id) FROM city
GROUP BY country_id
ORDER BY COUNT(city_id) DESC
LIMIT 1;
```