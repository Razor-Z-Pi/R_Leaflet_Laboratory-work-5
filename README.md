# R_Leaflet_Laboratory-work-5
Лабораторная работа №5 – Создание интерактивных карт с помощью пакета leaflet / Laboratory work №5 - Creating interactive maps with the help of leaflet package
___

Для построения карт изначально необходимо собрать и подготовить информацию. Для отображения точечных объектов на карте достаточно знать координаты этих точек. В географии для определения точек используются два параметра:

Широта – это координата, которая определяет положение точки на поверхности к северу от экватора. Широта – это угол, равный в любой точке экватора. Принято считать, что в северном полушарии широта положительная, а в южном – отрицательная. Точки с одинаковой широтой образуют линии, называемые параллелями. Параллели проходят с востока на запад в виде кругов, параллельных экватору.

Долгота – двугранный угол λ между плоскостью меридиана, проходящего через данную точку и плоскостью начального нулевого меридиана, от которого ведется отсчет долготы. Долготу от 0° до 180° к востоку от нулевого меридиана называют восточной, к западу – западной. Восточные долготы принято считать положительными, западные – отрицательными.

Для удобства в наборах данных рекомендуется переменную, отвечающую за долготу именовать lng, за широту – lat.
___
# Работа с `leaflet` / Working with `leaflet` 
Создание полотна карты осуществляется с помощью функкции leaflet(). Добавление элементов рекомендуется с использованием конструкции конвеера (pipe) с использованием оператора magrittr %>%. / The map canvas is created using the leaflet() function. Adding elements is recommended using the pipe construction with the magrittr %>% operator.
```R
leaflet() %>%
  addTiles()
```
___
# Практическая часть / Practical part
___
Задание 1 – Соберите исходные данные в виде датафрейма, используя сведения о 100 крупнейших городах Канады. Используя документацию к пакету leaflet изучите функцию addCircleMarkers() и постройте карту с произвольным слоем из providers. Визуализируйте данные с использованием круглых маркеров, добавьте всплывающие подсказки, содержащие сведения об объектах.

Общая структура датафрейма должна иметь следуюший вид:
lng – долгота;
lat – широта;
municipality – название города;
province – название провинции;
status – статус города;
area – площадь города;
pop_96 – численность населения на 1996 год;
pop_01 – численность населения на 2001 год;
pop_06 – численность населения на 2006 год;
pop_11 – численность населения на 2011 год;
pop_16 – численность населения на 2016 год.
___
In order to build maps, it is initially necessary to collect and prepare information. To display point objects on a map, it is sufficient to know the coordinates of these points. In geography, two parameters are used to define points:

Latitude is a coordinate that defines the position of a point on the surface north of the equator. Latitude is the angle equal at any point on the equator. It is generally accepted that latitude is positive in the northern hemisphere and negative in the southern hemisphere. Points with the same latitude form lines called parallels. Parallels run from east to west in the form of circles parallel to the equator.

Longitude - dihedral angle λ between the plane of the meridian passing through a given point and the plane of the initial zero meridian, from which the longitude is counted. Longitude from 0° to 180° to the east of the prime meridian is called eastern, to the west - western. Eastern longitudes are considered positive, western longitudes are considered negative.

For convenience in data sets, it is recommended to name the variable responsible for longitude as lng and latitude as lat.
___
Task 1 - Collect raw data in the form of a dataframe using information about the 100 largest cities in Canada. Using the leaflet package documentation, examine the addCircleMarkers() function and build a map with an arbitrary layer of providers. Visualize the data using circular markers, add tooltips containing information about the objects.

The overall structure of the dataframe should look like the following:
lng - longitude;
lat - latitude;
municipality - city name;
province - name of the province;
status - city status;
area - area of the city;
pop_96 - population for 1996;
pop_01 - population for 2001;
pop_06 - population for 2006;
pop_11 - population for 2011;
pop_16 - population for 2016.
