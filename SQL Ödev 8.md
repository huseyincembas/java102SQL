# SQL ÖDEV 8
---
1.  **test** veritabanınızda **employee** isimli sütun bilgileri id(INTEGER), name VARCHAR(50), birthday DATE, email VARCHAR(100) olan bir tablo oluşturalım.
2.  Oluşturduğumuz **employee** tablosuna 'Mockaroo' servisini kullanarak 50 adet veri ekleyelim.
3.  Sütunların her birine göre diğer sütunları güncelleyecek 5 adet UPDATE işlemi yapalım.
4.  Sütunların her birine göre ilgili satırı silecek 5 adet DELETE işlemi yapalım.
---
### CEVAPLAR

1. 
``` SQL
CREATE TABLE employee (
	id INTEGER,
	name VARCHAR(50),
	birtday DATE,
	email VARCHAR(100)
);
```
2. 
```SQL 
insert into employee (id, name, birtday, email) values (1, 'Gar', '30/12/2022', 'gwylder0@blogs.com'); insert into employee (id, name, birtday, email) values (2, 'Sarette', '31/1/2023', 'sfranke1@salon.com'); insert into employee (id, name, birtday, email) values (3, 'Linda', '5/1/2023', 'lschimank2@boston.com'); insert into employee (id, name, birtday, email) values (4, 'Kamila', '11/7/2022', 'ksargeant3@about.me'); insert into employee (id, name, birtday, email) values (5, 'Christean', '3/5/2022', 'coxborough4@flavors.me'); insert into employee (id, name, birtday, email) values (6, 'Aliza', '18/5/2022', 'adigiacomo5@reverbnation.com'); insert into employee (id, name, birtday, email) values (7, 'Parke', '7/8/2022', 'plamborne6@paginegialle.it'); insert into employee (id, name, birtday, email) values (8, 'Ree', '15/2/2023', 'rtetley7@pagesperso-orange.fr'); insert into employee (id, name, birtday, email) values (9, 'Torrence', '3/2/2023', 'tatrill8@webs.com'); insert into employee (id, name, birtday, email) values (10, 'Dagny', '30/5/2022', 'deagell9@harvard.edu'); insert into employee (id, name, birtday, email) values (11, 'Errol', '16/10/2022', 'eglanistera@skyrock.com'); insert into employee (id, name, birtday, email) values (12, 'Brent', '23/8/2022', 'bbloxamb@hexun.com'); insert into employee (id, name, birtday, email) values (13, 'Elyssa', '8/7/2022', 'eumbertc@bloomberg.com'); insert into employee (id, name, birtday, email) values (14, 'Sallee', '11/10/2022', 'smulvyd@buzzfeed.com'); insert into employee (id, name, birtday, email) values (15, 'Antoni', '1/12/2022', 'aglozmane@sohu.com'); insert into employee (id, name, birtday, email) values (16, 'Andria', '24/9/2022', 'avotierf@weebly.com'); insert into employee (id, name, birtday, email) values (17, 'Maurine', '2/7/2022', 'mamosg@addtoany.com'); insert into employee (id, name, birtday, email) values (18, 'Adams', '3/10/2022', 'amaffioneh@theatlantic.com'); insert into employee (id, name, birtday, email) values (19, 'Allie', '31/3/2022', 'apattersoni@ebay.com'); insert into employee (id, name, birtday, email) values (20, 'Jemie', '24/12/2022', 'jemneyj@discuz.net'); insert into employee (id, name, birtday, email) values (21, 'Jeromy', '4/6/2022', 'johickeyk@hhs.gov'); insert into employee (id, name, birtday, email) values (22, 'Sherlock', '28/4/2022', 'ssheehyl@opensource.org'); insert into employee (id, name, birtday, email) values (23, 'Fidela', '31/10/2022', 'fmorsleym@hp.com'); insert into employee (id, name, birtday, email) values (24, 'Malorie', '12/8/2022', 'mohonen@cargocollective.com'); insert into employee (id, name, birtday, email) values (25, 'Bone', '12/9/2022', 'bghidettio@pen.io'); insert into employee (id, name, birtday, email) values (26, 'Patti', '18/11/2022', 'pcottap@tmall.com'); insert into employee (id, name, birtday, email) values (27, 'Easter', '19/7/2022', 'ecruxtonq@miibeian.gov.cn'); insert into employee (id, name, birtday, email) values (28, 'Lyndsay', '24/2/2023', 'lsmithermanr@mediafire.com'); insert into employee (id, name, birtday, email) values (29, 'Beckie', '4/3/2023', 'bcominis@cafepress.com'); insert into employee (id, name, birtday, email) values (30, 'Feliks', '28/6/2022', 'fbaylayt@slate.com'); insert into employee (id, name, birtday, email) values (31, 'Clair', '6/2/2023', 'crostonu@xrea.com'); insert into employee (id, name, birtday, email) values (32, 'Lucy', '12/1/2023', 'lfurlowv@qq.com'); insert into employee (id, name, birtday, email) values (33, 'Koressa', '10/7/2022', 'kbuxseyw@etsy.com'); insert into employee (id, name, birtday, email) values (34, 'Jethro', '12/10/2022', 'jcharrettex@rakuten.co.jp'); insert into employee (id, name, birtday, email) values (35, 'Bud', '31/12/2022', 'bsotherony@1688.com'); insert into employee (id, name, birtday, email) values (36, 'Rorke', '30/6/2022', 'rdumbrillz@princeton.edu'); insert into employee (id, name, birtday, email) values (37, 'Maribelle', '4/7/2022', 'mmeus10@indiatimes.com'); insert into employee (id, name, birtday, email) values (38, 'Emilia', '12/3/2022', 'etipperton11@twitter.com'); insert into employee (id, name, birtday, email) values (39, 'Lotta', '2/2/2023', 'lscott12@people.com.cn'); insert into employee (id, name, birtday, email) values (40, 'Garrott', '9/6/2022', 'gneilus13@accuweather.com'); insert into employee (id, name, birtday, email) values (41, 'Rouvin', '26/5/2022', 'rfranssen14@feedburner.com'); insert into employee (id, name, birtday, email) values (42, 'Cozmo', '31/3/2022', 'cpolding15@storify.com'); insert into employee (id, name, birtday, email) values (43, 'Melody', '21/10/2022', 'mascrofte16@examiner.com'); insert into employee (id, name, birtday, email) values (44, 'Norbert', '12/5/2022', 'nblankman17@facebook.com'); insert into employee (id, name, birtday, email) values (45, 'Sallie', '19/4/2022', 'shadkins18@mozilla.org'); insert into employee (id, name, birtday, email) values (46, 'Coletta', '9/7/2022', 'cickov19@ebay.com'); insert into employee (id, name, birtday, email) values (47, 'Caryl', '7/7/2022', 'cpaffitt1a@blinklist.com'); insert into employee (id, name, birtday, email) values (48, 'Vannie', '5/2/2023', 'vklaes1b@alibaba.com'); insert into employee (id, name, birtday, email) values (49, 'Giulietta', '6/6/2022', 'gwhitelaw1c@devhub.com'); insert into employee (id, name, birtday, email) values (50, 'Sibbie', '19/11/2022', 'scrumpe1d@hao123.com');
```
3. 
```sql 
UPDATE employee
SET first_name = 'test',
last_name = 'tes'
WHERE id < 6;
```
4. 
```sql 
DELETE FROM employee
WHERE id < 6;
```