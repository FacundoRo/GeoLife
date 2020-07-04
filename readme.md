Proyecto GeoLife
Curso Visualizacion de Datos

El proyecto inicia son 4 Python Notebooks para preprocesamiento:

_Preprocesamiento:_

 **GeolifePrj_00_plt2df.ipynb**:
 La data original de GeoLife se encuentra en un formato llamado PLT, parecido a CSV.
 El primer paso es crear DataFrames de Pandas y serializarlas , para trabajar despues
 con ellas.Además facilita la transformación entre otros formatos como GeoJSon, CSV, etc
 
 **GeolifePrj_01_df2geojson.ipynb**
 Una vez con toda la data en DataFrames la transformamos en GeoJSON, en versiones
 ligeras y completas, para poder visualizarla y explorarla con diferentes herramientas
 y tener una idea intuitiva del tipo de informacion con la que estamos lidiando.
 
 
 _Features extra:_
 
 **GeolifePrj_02_extrafeatures.ipynb**
 Deducimos informaciones extra utiles en base a la data original para enriquecer el dataset y poder sacar conclusiones
 -calculamos la velocidad en cada punto
 -calculamos la aceleracion
 -calculamos la velocidad filtrada con un "Moving Average" , para evitar picos en las velocidad,
 producto de ruido en la informacion GPS propia del sistema GPS.
 -calculamos distancias recorridas
 -con la distribucion de velocidades se puede intuir los diferentes modos de transporte utilizados y en que porcentajes
 
 
 _Data Mining:_
 
 **GeolifePrj_03_clustering.ipynb**
 
 Utilizamos DBSCAN de sklearn como algortimo de clusterizacion porque se adapta muy bien al tipo 
 de data geolocalizada y es resistente al ruido, correspondiente a ubicaciones poco visitadas por los
 usuarios.
 Aplicamos el algoritmo a cada usuario , para descubrir sus "stay points" , como universidad , centros comerciales, casa ,etc y poder deducir su comportamiento (Futuro: cruzar esa información con
 la información temporal para deducir a que tipo de actividad se relaciona ciertas areas geograficas)
 
 Agregamos en base de datos grupos de 10 a 20 usuarios, con un promedio de 1'500'000 de registros,
 probamos un random undersampling y probamos la clusterizacion con diferentes subconjuntos aleatorios 
 de esa data para confirmar que tienen los mismos clusteres.
 Ademas se puede deducir de los clusteres los lugares que visitan en COMUN ese grupo de usuarios.
 
 
 _Visualización_
 
 Usamos diferentes herramientas para visualizar la data preprocesada y taggeada como
 MapBox
 Kibana
 geojson.io
 
 
 
 
 
 
 
 
 
 -Edwin Contreras
 -Jesús Chavez  
 -Facundo Rodriguez
