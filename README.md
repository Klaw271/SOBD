# Большие данные и распределённые вычисления (SOBD)

Репозиторий по курсу «Обработка больших данных» на учебном кластере `Hadoop` (YARN + HDFS), `Apache Spark 3.5.2` и `Apache Iceberg 1.6.0`.

## Лабораторные работы

* **Лабораторная работа № 1.** [Выполнение разведочного анализа больших данных с использованием Apache Spark](lab1/README.md)
  * [Часть 1 -- загрузка CSV, отбор признаков, приведение типов, запись в Iceberg](lab1/1_Data_cleansing_US_Accidents.ipynb)
  * [Часть 2 -- разведочный анализ, обработка пропусков, выбросов и аномалий](lab1/2_Exploratory_analysis_US_Accidents.ipynb)

* **Лабораторная работа № 2.** [Машинное обучение на больших данных с использованием Apache Spark и SparkML](lab2/README.md)
  * [Часть 1 -- линейная регрессия длительности происшествия, подбор регуляризации](lab2/1_Linear_Regression_US_Accidents.ipynb)
  * [Часть 2 -- случайный лес для классификации тяжести происшествия на несбалансированной выборке](lab2/2_Random_Forest_Classification_US_Accidents.ipynb)
  * [Выборка из 1000 строк в CSV](lab2/us_accidents_sample.csv) и модель в HDFS -- артефакты для следующей работы

Ноутбуки сохранены уже выполненными на кластере: все выводы и графики видны без повторного запуска.

## Датасет

[US Accidents (2016 -- 2023)](https://www.kaggle.com/datasets/sobhanmoosavi/us-accidents) -- 7 728 394 строки, 46 столбцов, один CSV весом ≈ 2,84 ГиБ. Сам файл в репозиторий не коммитится (слишком большой); он загружен в HDFS по пути `hdfs:///user/user7/otpushchennikov/data/US_Accidents_March23.csv` и записан в таблицу Iceberg `otpushchennikov_database.otpushchennikov_us_accidents`.
