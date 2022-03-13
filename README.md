# Project-clownInfo
Sql-practice-03
---
Create table clown_info

```Sql
CREATE TABLE clown_info
(
    name       VARCHAR(25),
    last_seen  VARCHAR(30),
    appearance VARCHAR(100),
    activities VARCHAR(30)
);
```
---
Adding information
```sql
INSERT INTO clown_info (name, last_seen, appearance, activities) 
VALUES ('Элси', 'Дом престарелых Черри Хилл', 'Ж, рыжие волосы, зеленый костюм, огромные ботинки', 'шарики, машинки');

INSERT INTO clown_info (name, last_seen, appearance, activities)
VALUES ('Пиклз', 'Вечеринка Джека Грина', 'М, оранжевые волосы, синий костюм, огромные ботинки', 'мим');

INSERT INTO clown_info (name, last_seen, appearance, activities)
VALUES ('Снаглз', 'Болмарт', 'Ж, желтая рубашка, красные штаны', 'рожок, зонтик');

INSERT INTO clown_info (name, last_seen, appearance, activities)
VALUES ('Мистер Хобо', 'Цирк BG', 'М, сигара, черные волосы, маленькая шляпа', 'скрипка');

INSERT INTO clown_info (name, last_seen, appearance, activities)
VALUES ('Кларабелл', 'Дом престарелых Бельмонт', 'Ж, розовые волосы, большой цветок синее палтье', 'кричалки, танцы');

INSERT INTO clown_info (name, last_seen, appearance, activities)
VALUES ('Скутер', 'Больница Окленд', 'М, синие волосы, красный костюм, большой нос', 'шарики');

INSERT INTO clown_info (name, last_seen, appearance, activities)
VALUES ('Зиппо', 'Торговый центр Милстоун', 'Ж, оранжевый костюм, штаны', 'танцы');

INSERT INTO clown_info (name, last_seen, appearance, activities)
VALUES ('Бэйб', 'Автокшола Эрла', 'Ж, розовый костюм с блестками', 'эквилибристка, машинки');

INSERT INTO clown_info (name, appearance, activities)
VALUES ('Бонзо', 'М, женское платье в горошек', 'пение, танцы');

INSERT INTO clown_info (name, last_seen, appearance)
VALUES ('Снифлз', 'Заведение Трэйси', 'М, зелено-фиолетовый костюм, длинный нос');

INSERT INTO clown_info (name, last_seen, appearance, activities)
VALUES ('Зиппо', 'Торговый центр Милстоун', 'Ж, оранжевый костюм, штаны', 'танцы, пение');

INSERT INTO clown_info (name, last_seen, appearance, activities)
VALUES ('Снаглз', 'Болмарт', 'Ж, желтая рубашка, красные штаны', 'рожок, зонтик');

INSERT INTO clown_info (name, last_seen, appearance, activities)
VALUES ('Бонзо', 'Парк Диксон', 'М, женское платье в горошек', 'пение, танцы');

INSERT INTO clown_info (name, last_seen, appearance, activities)
VALUES ('Снифлз', 'Заведение Трэйси', 'М, зелено-фиолетовый костюм, длинный нос', 'разъезжает на машинке');

INSERT INTO clown_info (name, last_seen, appearance, activities)
VALUES ('Мистер Хобо', 'Цирк BG', 'М, сигара, черные волосы, маленькая шляпа', 'скрипка');

INSERT INTO clown_info (name, last_seen, appearance, activities)
VALUES ('Танир', 'Торговый центр Милстоун', 'Ж, оранжевый костюм, штаны', 'танцы, пение');
```
---
Requests
```Sql
DELETE FROM clown_info WHERE activities = 'танцы';

DELETE FROM clown_info WHERE activities = 'кричалки, танцы' AND name = 'Кларабелл';

SELECT * FROM clown_info WHERE activities = 'танцы';

DELETE FROM clown_info WHERE activities = 'танцы';

UPDATE clown_info SET activities = 'домбыра' WHERE activities = 'скрипка';

SELECT * FROM clown_info WHERE last_seen IS NULL;

UPDATE clown_info SET last_seen='Болмарт' WHERE last_seen IS NULL;

SELECT * FROM clown_info WHERE activities IS NULL;

UPDATE clown_info SET activities='танцы' WHERE activities IS NULL;

SELECT * FROM clown_info WHERE activities = 'танцы, пение' AND name='Танир';

UPDATE clown_info SET activities='домбыра' WHERE activities = 'танцы, пение' AND name = 'Танир';

UPDATE clown_info SET appearance = 'Ж, желтая рубашка, синие штаны' WHERE name = 'Снаглз';

UPDATE clown_info SET last_seen='Парк Диксон' WHERE name = 'Бонзо';

UPDATE clown_info SET activities = 'разъезжает на машинке' WHERE activities = 'танцы' AND name ='Снифлз';

UPDATE clown_info SET last_seen = 'Вечеринка Эрика Грея' WHERE name = 'Мистер Хобо';
```
