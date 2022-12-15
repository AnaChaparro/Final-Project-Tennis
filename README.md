# Final Project Tennis. Iron Salam 🎾

## ÍNDICE

1. [Introducción y objetivos](#introducción-y-objetivos)
2. [Pasos seguidos](#pasos-seguidos)
3. [Machine Learning](#machine-learning)
4. [Visualización](#visualización)
5. [Conclusiones](#conclusiones)


### 1. Introducción y objetivos

Se trata de un proyecto en el que se ha recreado la organización de un torneo en el que participan los 32 jugadores de ranking ATP más alto actualmente. Los objetivos eran realizar un modelo predicitivo que pudiese establecer quien tienen más probabilidad de ganar el torneo, denominado Iron Slam, cruzando aleatoriamente estos jugadores en varias rondas, definiendo quien es el ganador de cada encuentro en función de su ratio de victorias predecidas.

Posteriromente se ha hecho un análisis de las ventajas competitivas de los dos finalistas que se han enfrentado en la ronda final del torneo.

### 2. Pasos seguidos

- Extracción de datos:

  Se han extrído datos de ranking, efectividades e hitórico de enfrentamientos entre los 32 jugadores indicados:
  - Fichero de enfrentamientos de torneos ATP250, ATP500, Master 1000, Grand Slam y Master Cup vía kaggle con fecha desde 2008 a 2022.
  - Datos de los enfrentamientos en los Master 1000 y Grand Slam al estar incompleto el archivo de kaggle mediante Web Scraping de la web ATP estadísticas.
  - Ranking de la ATP de mediante Web Scraping de la web ESPN.
  - Datos de efectividades en cuanto a saque, resto y líderes bajo presión mediante Web Scraping de la web ATP estadísticas.
  - Datos históricos de los dos finalistas del torneo mediante Web Scraping de la web ATP estadísticas.

- Transformación:
  
Se realiza la importación de los dataframes para realizar su limpieza, homogeneizar los datos y reducir las dimensiones de manera acorde a los datos que interesan, ya que en este caso solo se tendrán en cuenta los datos desde el 2018 en adelante, ya que el tipo de juego y habillidades de un jugador cambian mucho a lo largo del tiempo, e influirín de manera negativa en una predicción del tipo de juego actual.

También se concatenan los dataframen se cara a realizar el modelo predictivo y tener los datos que interesan en un mismo DF.

### 3. Machine Learning

El proceso para obtener un ganador del torneo se ha basado en la predicción partido a partido para establecer un ratio de victorias por cada jugador.
Se ha realizado la formación de parejas de manera random de los 32 jugadores y se enfrentaban por partidos en diferentes rondas hasta llegar a la final, en la que únicamente quedaban dos jugadores.

Del modelo predictivo se esxtraía un ratio de victorias por jugador en funciónd de su hístorico de partidos, sus efectividades en saque, resto y presión, en función de la superficie y del año. Con la predición se dividen los partidos ganados entre todos los partidos preedichos, así el jugador de la pareja con mayot ratio de victorias gana el partido y pasa a la siguiente ronda.

Los jugadores que alcanzan la ronda final son Rafa Nadal y Novak Djokovic, siendo Djokovic el jugador ganador con un ratio de victorias del 80%, y superior al resto de los jugadores.

### 4. Visualización

La visualización se ha basado en el estudio de las efectividades de saque, resto y líder bajo presión de ambos finalistas, los dos jugadores tienen efectividades con valores muy ajustados, destacando ligeramente Djokovic. También se observa que sus efectividades han disminuido desde 2018 a la actualizadad.

Con Folium se ha realizado el mapa con las coordenas de Matadero, que es donde se hubicará la pista para disputarse el torneo.



 
 
 
