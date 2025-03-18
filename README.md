# <center> Проект 2. Анализ вакансий из HeadHunter

## Оглавление
[1. Описание проекта](https://github.com/romash23/project-2/blob/master/README.md#Описание-проекта)  
[2. Какой кейс решаем?](https://github.com/romash23/project-2/blob/master/README.md#Какой-кейс-решаем)  
[3. Краткая информация о данных](https://github.com/romash23/project-2/blob/master/README.md#Краткая-информация-о-данных)  
[4. Этапы работы над проектом](https://github.com/romash23/project-2/blob/master/README.md#Этапы-работы-над-проектом)  
[5. Результат](https://github.com/romash23/project-2/blob/master/README.md#Результат)    
[6. Выводы](https://github.com/romash23/project-2/blob/master/README.md#Выводы) 


### Описание проекта

В данном проекте будет проводится анализ базы данных о вакансиях, взятые с сайта HeadHunter.ru. Суть проекта: попрактиковаться в написании sql-запросов на реальнных данных и проанализировать их.

:point_right: [К оглавлению](https://github.com/romash23/project-2/blob/master/README.md#%D0%9E%D0%B3%D0%BB%D0%B0%D0%B2%D0%BB%D0%B5%D0%BD%D0%B8%D0%B5)

### Краткая информация о данных

 Сама база данных является являтся интелектаульной собственностью компании Scillfactory. По это причине в данной проекте нет возможности выложить исходные данные или ссылку на них.

 *Сама базы данных состоит из нескольких таблиц:*
 * VACANCIES - эта таблица хранит в себе данные по вакансиям и содержит следующие столбцы: 
 
 <img src=https://lms-cdn.skillfactory.ru/assets/courseware/v1/837cf6ff79f483e387a16c993634f3e4/asset-v1:SkillFactory+DST-3.0+28FEB2021+type@asset+block/SQL_pj2_2_2.png width="600" height="280">

 * AREAS - таблица-справочник, которая хранит код региона и его название

 <img src=https://lms-cdn.skillfactory.ru/assets/courseware/v1/682c2306f3d46a25915a89d4ec7e16ed/asset-v1:SkillFactory+DST-3.0+28FEB2021+type@asset+block/SQL_pj2_2_3.png width="600" height="95">

 * EMPLOYERS - таблица-справочник со списком работодателей

<img src=https://lms-cdn.skillfactory.ru/assets/courseware/v1/d2a26db623c75572c71923b57241e038/asset-v1:SkillFactory+DST-3.0+28FEB2021+type@asset+block/SQL_pj2_2_4.png width="600" height="130">

* INDUSTIES - таблица-справочник вариантов сфер деятельности работодателей

<img src=https://lms-cdn.skillfactory.ru/assets/courseware/v1/2c76bca09937a1a05a9e66d51008e298/asset-v1:SkillFactory+DST-3.0+28FEB2021+type@asset+block/SQL_pj2_2_5.png width="600" height="95">

* EMMPLOYERS_INDUSTRIES - дополнительная таблица, которая существует для организации связи между работодателями и сферами их деятельности

<img src=https://lms-cdn.skillfactory.ru/assets/courseware/v1/16ff3df0bb0ddecd922562f3c4bdd32c/asset-v1:SkillFactory+DST-3.0+28FEB2021+type@asset+block/SQL_pj2_2_6.png width="600" height="95">

Сами таблицы связаны друг с другом через специальные колонки - id следующим образом:

<img src=https://lms-cdn.skillfactory.ru/assets/courseware/v1/efd63819603e7d4f4433ed2fedec717c/asset-v1:SkillFactory+DST-3.0+28FEB2021+type@asset+block/SQL_pj2_2_1.png width="400" height="400">

:point_right: [К оглавлению](https://github.com/romash23/project-2/blob/master/README.md#%D0%9E%D0%B3%D0%BB%D0%B0%D0%B2%D0%BB%D0%B5%D0%BD%D0%B8%D0%B5)


### Этапы работы над проектом

Работа над проектом была разбита на несколько частей:

1. *Исследование структуры данных* 

То есть это первичное знакомство с данными, не подразумевающее какие-либо серьезных вычислений

2. *Преобразование данных*  

После изучения данных, мы приступили к преобразованию признаков в датафрейме. В данных было много лишней, ненужной инфомации, а также сами признаки были представлены в неудобном для создании графиков и различных моделей формате. Для этого было написано несколько функций,
которые применялись к изначальным признакам и с помощью метода *apply* были созданы более удобныые признаки.

3. *Исследование зависимостей в данных*

Данный этап представляет собой визуализацию данных. То есть в этой части проекта как-таковых преобразований не было. Здесь мы исследовали зависимости одних признаков от других на графиках с помощью библиотеки *plotly*

4. *Очистка данных*

При исследовании зависимостей данные были обнаружены некие аномалии в данных - те значения, которые выбиваются из общего спектра. Обычно их называют выбросами. На данном этапе были удалены некоторый строки данных, которые не отражают общую картину. Можно сказать даже, что такие данные вредны, посколько они могли бы учесться некой моделью для анализа данных, и в последствие она бы начала давать неверные прогнозы

5. *Создание репозитория на GiHub*

Последний шаг также немаловажен - именно благодаря ему вы сейчас читаете этот текст :smirk: и имеете возможность ознакомиться с моей работой :raising_hand:

:point_right: [К оглавлению](https://github.com/romash23/project-2/blob/master/README.md#%D0%9E%D0%B3%D0%BB%D0%B0%D0%B2%D0%BB%D0%B5%D0%BD%D0%B8%D0%B5)


### Результат

Так как на GitHub не отображаются графики из библиотеки *plotly*, сами графики были загружены в отдельную [папку](https://github.com/romash23/project-1/tree/master/plotly_graphics). Но для удобства, для каждого графика в [*jupyter-ноутбуке*](https://github.com/romash23/project-1/blob/master/%D0%9F%D1%80%D0%BE%D0%B5%D0%BA%D1%82%201.%20%D0%90%D0%BD%D0%B0%D0%BB%D0%B8%D0%B7%20%D1%80%D0%B5%D0%B7%D1%8E%D0%BC%D0%B5%20%D0%B8%D0%B7%20HeadHunter.ipynb) были выложены скриншоты всех графиков (конечно самой анимации от *plotly* не будет, но лучше хотя бы так, чем совсем без графиков :grin:)

:point_right: [К оглавлению](https://github.com/romash23/project-2/blob/master/README.md#%D0%9E%D0%B3%D0%BB%D0%B0%D0%B2%D0%BB%D0%B5%D0%BD%D0%B8%D0%B5)

### Выводы

В данном проекте мы на практике применили знания, полученные ранее: работа с библиотеками *Numpy* и *Pandas*, визуализация данных в библиотеке *plotly*. Смогли примерить на себя "шкуру" настоящего дата-сайентиста :muscle: : попрактиковались в преобразовании, а также очистке данных от выбросов. Как оказалось, это задача достаточно важная и трудоемкая. Сама обработка датасета может занимать до 60-70% от всего времени, что затрачивает датасайентист при работе с данными. Но без этого - никак. На "сырых" данных любая, даже дорогостоющая и очень качественная модель, не даст нужных предсказаний, и возможно руковоство компании, видя "ложные" предсказания, соверших ряд стратегичех ошибок.

:point_right: [К оглавлению](https://github.com/romash23/project-2/blob/master/README.md#%D0%9E%D0%B3%D0%BB%D0%B0%D0%B2%D0%BB%D0%B5%D0%BD%D0%B8%D0%B5)
