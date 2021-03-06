# Исследование надёжности заёмщиков

Заказчик, в лице кредитного отдела банка, хочет выяснить: влияет ли семейное положение и количество детей клиента на факт погашения кредита в срок. Результаты исследования помогут в построении модели **кредитного скоринга** — специальной системы, которая оценивает способность потенциального заёмщика вернуть кредит банку.

## Задача
Ответить на вопросы:
  - Есть ли зависимость между наличием детей и возвратом кредита в срок?
  - Есть ли зависимость между семейным положением и возвратом кредита в срок?
  - Есть ли зависимость между уровнем дохода и возвратом кредита в срок?
  - Как разные цели кредита влияют на его возврат в срок?

*План действий*:
1. Откроем и изучим файл с данными
2. Предобработаем данные для улучшения качества проводимого анализа
3. Ответим на главные вопросы исследования
4. Сформулируем общий вывод

## Методы и технологии
- Обработка пропусков
- Замена типа данных
- Поиск и обработка артефактов
- Обработка дубликатов
- Лемматизация
- Категоризация данных
- Сводные таблицы

 ## Используемые библиотеки
*pandas, pymystem3, collections*

## Описание данных
Входные данные от банка — статистика о платёжеспособности клиентов.
- `children` — количество детей в семье
- `days_employed` — общий трудовой стаж в днях
- `dob_years` — возраст клиента в годах
- `education` — уровень образования клиента
- `education_id` — идентификатор уровня образования
- `family_status` — семейное положение
- `family_status_id` — идентификатор семейного положения
- `gender` — пол клиента
- `income_type` — тип занятости
- `debt` — имел ли задолженность по возврату кредитов
- `total_income` — ежемесячный доход
- `purpose` — цель получения кредита


## Вывод
- Количество детей практически никак не вляет на возврат долга в срок, однако клиентам у которых вообще нет детей банк может с большей уверенностью предоставить кредит.
- Клиентам побывавшим в браке или находящимся в нем более банк может доверять больше, чем тем кто ни разу не узаконил свои отношения. Отдельно хочется выделить вдов/вдовцов - они надежные заемщики
- Банк может в равной степени доверять как людям с низким, так и свысоким уровнем заработка. В отоношении клиентов со средним заработком банку следует быть осторожнее и ориентировать по другим метрикам.
- Банку следует акцентировать внимание на клиентах, которые указывают образование и приобретение автомобиля как цель заема. Исследование показало что подобные заемщики самые ненадежные.

На основе проведенного анализа возможно приблизительно описать портрет идеального заемщика: это человек, который хотя бы раз был в браке, не имеющий детей, у него либо высокий, либо низкий уровень заработка и как цель заема он указывает ремонт, покупку недвижимости или свадьбу.
