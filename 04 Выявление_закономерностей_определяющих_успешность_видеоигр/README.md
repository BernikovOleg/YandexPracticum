# Выявление закономерностей определяющих успешность видеоигр
Мы располагаем данными о продаже разных видеоигр, которые собирались до 2016 года из открытых источников. Нужно помочь магазину "Стримчик", который продаёт по всему миру компьютерные игры, сделать ставку на будущие потенциально популярные продукты и спланировать рекламные кампании.

## Задача
Выявить закономерности, определяющие успешность игры.

*План действий*:
1. Откроем и изучим файл с данными
2. Предобработаем данные для улучшения качества проводимого анализа
3. Проведем исследовательский анализ данных
4. Составим портрет пользователя каждого региона: Северная Америка, Европа и Япония
5. Проверим гипотезы
    - Средние пользовательские рейтинги платформ Xbox One и PC одинаковые
    - Средние пользовательские рейтинги жанров Action и Sports разные
6. Сформулируем общий вывод

## Методы и технологии
- Работа с DataFrame и Series
- Обработка пропусков
- Обработка дубликатов
- Обработка аномалий
- Изменение типов данных
- Исследовательский анализ данных
- Построение графиков: линейные графики, гистограммы, диаграммы размаха, диаграммы рассеяния, столбчатые и круговые диаграммы
- Рассчет корреляции Пирсона
- Формулировка и проверка гипотез с помощью критерия Стьюдента

## Используемые библиотеки
*pandas, numpy, math, matplotlib, seaborn, scipy*

## Описание данных
- `Name` — название игры
- `Platform` — платформа
- `Year_of_Release` — год выпуска
- `Genre` — жанр игры
- `NA_sales` — продажи в Северной Америке (миллионы проданных копий)
- `EU_sales`  — продажи в Европе (миллионы проданных копий)
- `JP_sales` — продажи в Японии (миллионы проданных копий)
- `Other_sales` — продажи в других странах (миллионы проданных копий)
- `Critic_Score` — оценка критиков (максимум 100)
- `User_Score` — оценка пользователей (максимум 10)
- `Rating` — рейтинг от организации ESRB (англ. Entertainment Software Rating Board). Эта ассоциация определяет рейтинг компьютерных - игр и присваивает им подходящую возрастную категорию.

## Вывод
- Две самые актуальные платформы на 2017 год: *PS4* и *XOne*. На них стоит смотреть в первую очередь. Также выявили менее востребованные, но все еще актуальные - *3DS*, *PS3* и *X360*, ими не стоит пренебрегать. 
- Наибольшая средняя продаваемость у платформы X360, немного меньше у *PS4*, *PS3* и *XOne*. У платформы *3DS* маленькая средняя продаваемость и на нее стоит обращать внимание только в отдельных случаях.
- Планировать рекламные кампании стоит в соответствии с *оценками критиков*. Они вероятнее всего предскажут наиболее продаваемые игры.
- Самый продаваемый жанр игр - *Shooter*.
- Игроки Северной Америки и Европы довольно схожи по своим предпочтениям. Геймеры обоих регионов выбирают игры в жанрах *Action* и *Shooter* и возрастным рэйтингом *M*. Есть лишь небольшое различие в выборе игровых платформ: в СА более распространены платформы фирмы Xbox, а в Европе - PlayStation.
- Стоит отличать японских игроков. Наиболее популярной платформой у них является *3DS*, но также 35% играют и в PlayStation. Набиолее предпочтительные жанры *Role-Playing* и *Action*. Японцы предпочитают игры без возрастного рейтинга.

