# Определение возраста покупателей
Сетевой супермаркет «Хлеб-Соль» внедряет систему компьютерного зрения для обработки фотографий покупателей. 

Фотофиксация в прикассовой зоне поможет определять возраст клиентов, чтобы:

- Анализировать покупки и предлагать товары, которые могут заинтересовать покупателей этой возрастной группы
- Контролировать добросовестность кассиров при продаже алкоголя

## Задача
Построить модель, которая по фотографии определит возраст человека.

## Методы и технологии
- Computer Vision
- ImageDataGenerator
- Adam
- ResNet50
- Построение нейросети
  - Сверотчные слои
  - Полносвязные слои

## Используемые библиотеки
*pandas, keras, matplotlib, seaborn*

## Описание данных
В нашем распоряжении одна папка со всеми изображениями `/final_files` и csv-файл `labels.csv` с двумя колонками: `file_name` и `real_age`.

## Вывод
С помощью архитектуры ResNet50 и добавлением к ней нескольких слоев мы получили неплохую модель, которая оценивает возраст человека на фотографии и ошибается в среднем на 6 лет от реального возраста человека.


