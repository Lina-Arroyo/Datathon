![HenryLogo](https://d31uz8lwfmyn8g.cloudfront.net/Assets/logo-henry-white-lg.png) 

# PROYECTO INDIVIDUAL II

## Descripción del proyecto: </br>   
En este proyecto usaremos python para crear un modelo predictivo de Machine Learning con el cual vamos a predecir el precio de las propiedades en venta en Colombia </br>

Nuestros datos pertenecen al mercado inmobiliario en Colombia para el año 2020, tenemos nuestros datos dividos en dos grupos, unos que usaremos para entrenar el modelo (train) y unos que usaremos para testear ese modelos (test) nuestro fin con este modelo de ML es permitir clasificar el precio de las propiedades en venta, utilizando los datos que se han puesto a nuestra disposición. </br>

Para esto, específicamente, debemos predecir la **categorización** de las propiedades entre baratas o caras, considerando como criterio el valor promedio de los precios (la media).  </br>

Una vez listo el modelo de predicción vamos a evaluar su desempeño con la metrica de exhaustividad (Recall) para las propiedades caras a partir de la mátriz de confusion (Confusion Matrix)

$$ Recall=\frac{TP}{TP+FN}$$
​
Donde $TP$ son los verdaderos positivos y $FN$ los falsos negativos.

Adicionalmente, se incluye la Accuracy como métrica de control.

## Descripción de los archivos

 - 'properties_colombia_train.csv': Contiene 197549 registros y 26 dimensiones, el cual incluye la información **numérica** del precio.
 - 'propiedades_colombia_test.csv': Contiene 65850 registros y 25 dimensiones, el cual no incluye la información del precio. 

## Descripción de las dimensiones del archivo de train 
- id - Identificador del aviso. No es único: si el aviso es actualizado por la inmobiliaria (nueva versión del aviso) se crea un nuevo registro con la misma id pero distintas fechas: de alta y de baja.
- ad_type - Tipo de aviso (Propiedad, Desarrollo/Proyecto).
- start_date - Fecha de alta del aviso.
- end_date - Fecha de baja del aviso.
- created_on - Fecha de alta de la primera versión del aviso.
- lat - Latitud.
- lon - Longitud.
- l1 - Nivel administrativo 1: país.
- l2 - Nivel administrativo 2: usualmente provincia.
- l3 - Nivel administrativo 3: usualmente ciudad.
- l4 - Nivel administrativo 4: usualmente barrio.
- l5 - Nivel administrativo 5.
- l6 - Nivel administrativo 6.
- rooms - Cantidad de ambientes.
- bedrooms - Cantidad de dormitorios (útil en el resto de los países).
- bathrooms - Cantidad de baños.
- surface_total - Superficie total en m².
- surface_covered - Superficie cubierta en m².
- price - Precio publicado en el anuncio.
- currency - Moneda del precio publicado.
- price_period - Periodo del precio (Diario, Semanal, Mensual)
- title - Título del anuncio.
- description - Descripción del anuncio.
- property_type - Tipo de propiedad (Casa, Departamento, PH).
- operation_type - Tipo de operación (Venta).
- geometry - Puntos geométricos formados por las coordenadas latitud y longitud. 

## Fases del proyecto
1. Carga de los archivos de train y test en un dataframe de pandas
2. Visualizacion de la informacion en los dataframe
3. Preprocesamiento de datos
    * Valores faltantes
    * Valores atipicos
    * Normalizacion
    * Codificacion y Discretizacion 
    * Seleccion de atributos relevantes
4. Creacion del modelo
5. Entrenamiento del modelo
6. Test del modelo
7. Creación de la matriz de confusión
8. Evaluación del modelo
9. Predicción con el dataset de test
10. Exportamos 