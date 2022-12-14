# Práctica Módulo Exploración y Visualización de Datos

- Partiendo del dataset *airbnb-listings Madrid.csv* se hace un primer tratamiento de la fuente de datos eliminando items sin fecha de *Host since* y de *Neighbourhood*, así como aquellos que no sean de la ciudad de Madrid ni tengan su código postal (28...) 
- También se ocultan aquellas columnas de URL, que no tienen utilidad para el análisis

- En la primera hoja se dibuja un mapa de la zona, convirtiendo primero las latitudes y longitudes dadas en la fuente a valores flotantes y de tipo geográfico
- Se representan los barrios (*Neighbourhood*) y códigos postales (*Zipcode*), agrupándolos en 3 zonas: Norte, Sur y Centro

- En la segunda hoja se representa en un eje temporal el promedio de reseñas que reciben los alojamientos de cada Zona, a lo largo de los años. En la vista emergente también se muestra la valoración media que reciben para cada año

- La tercera hoja se dedica a analizar si la valoración media de cada barrio mejoró o no en el año 2017 con respecto al anterior. Para esto se crea primero un campo calculado para convertir el *Reviews Scores Value* en un campo que va de las 0 a 5 estrellas, que es como aparece en la web de airbnb. También se generan 2 campos calculados (*Valoraciones 2017* y *Valoraciones 2016*) y se hace una operación lógica para ver si la media de valoración de un año mejora o no

- La cuarta hoja es una nube de palabras que hace uso de un parámetro Top N generado para mostrar los barrios con mejor valoración promedio. Los barrios también se colorean según la zona a la que pertenecen


**Como conclusiones:**
- Los alojamientos de Madrid tienen una valoración muy alta, superior a las 4/5 estrellas.
- Se perciben diferencias entre la zona norte y centro con respecto al sur, teniendo el sur una puntuación media ligeramente inferior
- A pesar de lo dicho, se observa que en muchos barrios céntricos la valoracion media empeora de un año a otro (**Ver Hoja 3**), lo que puede indicar un problema con las viviendas turísticas en el centro de Madrid
- Todos estos promedios están contrastados en el sentido de que el nº medio de reseñas es considerable, así que no se cae en la "trampa" de que haya pocas reseñas pero con mucha/poca puntuación
