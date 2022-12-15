# Final Project Tennis. Iron Salam 🎾

<img src="https://github.com/AnaChaparro/Final-Project-Tennis/blob/main/img/close-up-view-tennis-ball-caught-net-court.jpg?raw=true"> 

## ÍNDICE

1. [Introducción y objetivos](#introducción-y-objetivos)
2. [Pasos seguidos](#pasos-seguidos)
3. [Machine Learning](#machine-learning)
4. [Visualización](#visualización)
5. [Conclusiones](#conclusiones)


### 1. Introducción y objetivos 🎯

Se trata de un proyecto en el que se ha recreado la organización de un torneo en el que participan los 32 jugadores con ranking ATP más alto actualmente. El objetivo era realizar un modelo predicitivo que pudiese establecer quien tienen más probabilidad de ganar el torneo, denominado Iron Slam, cruzando aleatoriamente estos jugadores en varias rondas, definiendo quien es el ganador de cada encuentro en función de su ratio de victorias predecidas.

Posteriromente se ha hecho un análisis de las ventajas competitivas de los dos finalistas que se han enfrentado en la ronda final del torneo y como han influido estas en el resultado.

--------------------------------------------------------

### 2. Pasos seguidos 📌

- Extracción de datos:

  Se han extrído datos de rankings, efectividades e hitórico de enfrentamientos entre los 32 jugadores indicados:
  - Fichero de enfrentamientos de torneos ATP250, ATP500, Master 1000, Grand Slam y Master Cup vía kaggle con fecha desde 2008 a 2022.
  - Datos de los enfrentamientos en los Master 1000 y Grand Slam de 20222 al estar incompleto el archivo de kaggle mediante Web Scraping de la web ATP   estadísticas.
  - Ranking de la ATP de mediante Web Scraping de la web ESPN.
  - Datos de efectividades en cuanto a saque, resto y líderes bajo presión mediante Web Scraping de la web ATP estadísticas.
  - Datos históricos de los dos finalistas del torneo mediante Web Scraping de la web ATP estadísticas.

- Transformación:
  
  Se realiza la importación de los dataframes para realizar su limpieza, homogeneizar los datos y reducir las dimensiones de manera acorde a los datos que   interesan, ya que en este caso solo se tendrán en cuenta los datos desde el 2018 en adelante, ya que el tipo de juego y habillidades de un jugador         cambian mucho a lo largo del tiempo, e influirín de manera negativa en una predicción del tipo de juego actual.

  También se concatenan los dataframen de cara a realizar el modelo predictivo y tener los datos que interesan en un mismo DF.

--------------------------------------------------------

### 3. Machine Learning 🤖

El proceso para obtener un ganador del torneo se ha basado en la predicción partido a partido para establecer un ratio de victorias por cada jugador.
Se ha realizado la formación de parejas de manera random entre los 32 jugadores y se enfrentan por partidos en diferentes rondas hasta llegar a la final, en la que únicamente quedaban dos jugadores.

Del modelo predictivo se esxtraía un ratio de victorias por jugador en función de su hístorico de partidos, sus efectividades en saque, resto y presión, en función de la superficie y del año. Con los resultados de la predición, se dividen los partidos ganados entre todos los partidos preedichos, así el jugador de la pareja con mayor ratio de victorias gana el partido y pasa a la siguiente ronda.

Para escoger el modelo que mejor se ajusta en cada ocasión, se ha utilizado Lazy Clasifier que nos ofrecía todos los accuracy y F1 de todos los modelos, para así escoger el mejor.

Los jugadores que alcanzan la ronda final son Rafa Nadal y Novak Djokovic, siendo Djokovic el jugador ganador con un ratio de victorias del 80%, y nadal con un 70%.

--------------------------------------------------------

### 4. Visualización 📊

La visualización se ha basado en el estudio de las efectividades de saque, resto y líder bajo presión de ambos finalistas, los dos jugadores tienen efectividades con valores muy ajustados, destacando ligeramente Djokovic. También se observa que sus efectividades han disminuido desde 2018 a la actualizadad en ambos jugadores.

<p align="center">
<img src="https://github.com/AnaChaparro/Final-Project-Tennis/blob/main/img/Captura%20de%20pantalla%202022-12-15%20a%20las%2014.13.02.png?raw=true" width="443" height="344">         <img src="https://github.com/AnaChaparro/Final-Project-Tennis/blob/main/img/Captura%20de%20pantalla%202022-12-15%20a%20las%2014.12.47.png?raw=true" width="443" height="344">
</p>

Con Folium se ha realizado el mapa con las coordenas de Matadero, que es donde se hubicará la pista para disputarse el torneo.
 <p align="center">
  <img src="https://github.com/AnaChaparro/Final-Project-Tennis/blob/main/img/Captura%20de%20pantalla%202022-12-15%20a%20las%2014.14.32.png?raw=true" width="725" height="433">
  </p>

--------------------------------------------------------

### 5. Conclusiones 🔎

Como predicción entendemos que intervienen muchos más factores que se podrían incluir en los modelos predictivos. Habría que tener en cuenta los eventos que han ocurrido en cada partido, para poder aproximar más el resultado a una "verdad". Siempre nos quedaríamos a gran distancia de la realidad ya que lo bonito de un desporte como este es lo que puede sorprender cada jugador en el partido y lo diferentes que pueden ser los resultados.

-------------------------------------------------------

🚀 **HERRAMIENTAS**

  - **_Python_**: numpy, pandas, Folium, selenium, sklearn, LazyClassifier
  - **_Excel_**
  - **_Tableau_**

-------------------------------------------------------

© **FUENTES**

- Fichero de kaggle: https://www.kaggle.com/datasets/edoardoba/atp-tennis-data
- Web ATP estadíticas: https://www.atptour.com/es/stats
- Web ESPN:https://www.espn.com.ar/tenis/rankings





 
 
 
