# Final Project Tennis. Iron Salam 馃幘

<img src="https://github.com/AnaChaparro/Final-Project-Tennis/blob/main/img/close-up-view-tennis-ball-caught-net-court.jpg?raw=true"> 

## 脥NDICE

1. [Introducci贸n y objetivos](#introducci贸n-y-objetivos)
2. [Pasos seguidos](#pasos-seguidos)
3. [Machine Learning](#machine-learning)
4. [Visualizaci贸n](#visualizaci贸n)
5. [Conclusiones](#conclusiones)


### 1. Introducci贸n y objetivos 馃幆

Se trata de un proyecto en el que se ha recreado la organizaci贸n de un torneo en el que participan los 32 jugadores con ranking ATP m谩s alto actualmente. El objetivo era realizar un modelo predicitivo que pudiese establecer quien tienen m谩s probabilidad de ganar el torneo, denominado Iron Slam, cruzando aleatoriamente estos jugadores en varias rondas, definiendo quien es el ganador de cada encuentro en funci贸n de su ratio de victorias predecidas.

Posteriromente se ha hecho un an谩lisis de las ventajas competitivas de los dos finalistas que se han enfrentado en la ronda final del torneo y como han influido estas en el resultado.

--------------------------------------------------------

### 2. Pasos seguidos 馃搶

- Extracci贸n de datos:

  Se han extr铆do datos de rankings, efectividades e hit贸rico de enfrentamientos entre los 32 jugadores indicados:
  - Fichero de enfrentamientos de torneos ATP250, ATP500, Master 1000, Grand Slam y Master Cup v铆a kaggle con fecha desde 2008 a 2022.
  - Datos de los enfrentamientos en los Master 1000 y Grand Slam de 20222 al estar incompleto el archivo de kaggle mediante Web Scraping de la web ATP   estad铆sticas.
  - Ranking de la ATP de mediante Web Scraping de la web ESPN.
  - Datos de efectividades en cuanto a saque, resto y l铆deres bajo presi贸n mediante Web Scraping de la web ATP estad铆sticas.
  - Datos hist贸ricos de los dos finalistas del torneo mediante Web Scraping de la web ATP estad铆sticas.

- Transformaci贸n:
  
  Se realiza la importaci贸n de los dataframes para realizar su limpieza, homogeneizar los datos y reducir las dimensiones de manera acorde a los datos que   interesan, ya que en este caso solo se tendr谩n en cuenta los datos desde el 2018 en adelante, ya que el tipo de juego y habillidades de un jugador         cambian mucho a lo largo del tiempo, e influir铆n de manera negativa en una predicci贸n del tipo de juego actual.

  Tambi茅n se concatenan los dataframen de cara a realizar el modelo predictivo y tener los datos que interesan en un mismo DF.

--------------------------------------------------------

### 3. Machine Learning 馃

El proceso para obtener un ganador del torneo se ha basado en la predicci贸n partido a partido para establecer un ratio de victorias por cada jugador.
Se ha realizado la formaci贸n de parejas de manera random entre los 32 jugadores y se enfrentan por partidos en diferentes rondas hasta llegar a la final, en la que 煤nicamente quedaban dos jugadores.

Del modelo predictivo se esxtra铆a un ratio de victorias por jugador en funci贸n de su h铆storico de partidos, sus efectividades en saque, resto y presi贸n, en funci贸n de la superficie y del a帽o. Con los resultados de la predici贸n, se dividen los partidos ganados entre todos los partidos preedichos, as铆 el jugador de la pareja con mayor ratio de victorias gana el partido y pasa a la siguiente ronda.

Para escoger el modelo que mejor se ajusta en cada ocasi贸n, se ha utilizado Lazy Clasifier que nos ofrec铆a todos los accuracy y F1 de todos los modelos, para as铆 escoger el mejor.

Los jugadores que alcanzan la ronda final son Rafa Nadal y Novak Djokovic, siendo Djokovic el jugador ganador con un ratio de victorias del 80%, y nadal con un 70%.

--------------------------------------------------------

### 4. Visualizaci贸n 馃搳

La visualizaci贸n se ha basado en el estudio de las efectividades de saque, resto y l铆der bajo presi贸n de ambos finalistas, los dos jugadores tienen efectividades con valores muy ajustados, destacando ligeramente Djokovic. Tambi茅n se observa que sus efectividades han disminuido desde 2018 a la actualizadad en ambos jugadores.

<p align="center">
<img src="https://github.com/AnaChaparro/Final-Project-Tennis/blob/main/img/Captura%20de%20pantalla%202022-12-15%20a%20las%2014.13.02.png?raw=true" width="443" height="344">         <img src="https://github.com/AnaChaparro/Final-Project-Tennis/blob/main/img/Captura%20de%20pantalla%202022-12-15%20a%20las%2014.12.47.png?raw=true" width="443" height="344">
</p>

Con Folium se ha realizado el mapa con las coordenas de Matadero, que es donde se hubicar谩 la pista para disputarse el torneo.
 <p align="center">
  <img src="https://github.com/AnaChaparro/Final-Project-Tennis/blob/main/img/Captura%20de%20pantalla%202022-12-15%20a%20las%2014.14.32.png?raw=true" width="725" height="433">
  </p>

--------------------------------------------------------

### 5. Conclusiones 馃攷

Como predicci贸n entendemos que intervienen muchos m谩s factores que se podr铆an incluir en los modelos predictivos. Habr铆a que tener en cuenta los eventos que han ocurrido en cada partido, para poder aproximar m谩s el resultado a una "verdad". Siempre nos quedar铆amos a gran distancia de la realidad ya que lo bonito de un desporte como este es lo que puede sorprender cada jugador en el partido y lo diferentes que pueden ser los resultados.

-------------------------------------------------------

馃殌 **HERRAMIENTAS**

  - **_Python_**: numpy, pandas, Folium, selenium, sklearn, LazyClassifier
  - **_Excel_**
  - **_Tableau_**

-------------------------------------------------------

漏 **FUENTES**

- Fichero de kaggle: https://www.kaggle.com/datasets/edoardoba/atp-tennis-data
- Web ATP estad铆ticas: https://www.atptour.com/es/stats
- Web ESPN:https://www.espn.com.ar/tenis/rankings





 
 
 
