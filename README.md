# Corrección del Examen de Análisis de Datos
## Integrantes:
##### *[Yazán Cindy](https://github.com/Cindyk2052)*
##### *[Guachamín Daniel](https://github.com/danielguachamin)*
##### *[León Jeremy](https://github.com/Jeremy210321)*


Para obtener las locaciones de las ciudades, se utilizó la herramienta en la web [Bounding Box](http://boundingbox.klokantech.com/) y el [script1](https://github.com/Jeremy210321/correccion_del_examen/blob/master/script1.ipynb) para pasar la información obtenida a CouchDB. Los datos se ven en la BDD de Couch. 

Locations (1.py) 

![image](https://user-images.githubusercontent.com/66692550/130687394-cd01bff1-fb3c-4469-bb3f-7ee6ae586538.png)

Track 

Ahora, se utilizará el [script2](https://github.com/Jeremy210321/correccion_del_examen/blob/master/script2.ipynb) para hacer una búsqueda por palabra clave o también llamada “track” para después almacenar esos datos en CouchDB. 
![image](https://user-images.githubusercontent.com/66692550/130687424-04c8a815-9c7a-41dd-a954-314e903df95d.png)


Se implementa el [script3](https://github.com/Jeremy210321/correccion_del_examen/blob/master/script3.ipynb) para webScraping desde una página sobre juegos olímpicos obteniendo así un documento con extensión  .json. Luego de ellos almacenamos los datos en Mongo Compass en una base de datos “olímpicos” 

![image](https://user-images.githubusercontent.com/66692550/130687462-04067715-4af7-45e4-b066-a55f77723321.png)

Se utiliza el [script4](https://github.com/Jeremy210321/correccion_del_examen/blob/master/script4.ipynb) en Python para recopilar datos de Facebook, se hace uso del Facebook-scraper para encontrar datos específicos y se los guarda en una colección. Los datos recopilados se los pasa a la base de datos local “olimpicosfacebook” de MongoDB Compass. 

![image](https://user-images.githubusercontent.com/66692550/130687583-da73f890-85f5-40c9-ac6b-b67f12406e5d.png)

Se usa el tiktok-scraper para recopilar datos en csv de tiktokers con temática de los juegos olímpicos. Se recolectan de dos tiktoks; “juegos_olimpicos_”, “juegosolimpicos” , utilizando los comandos declarados en el [5.txt](https://github.com/Jeremy210321/correccion_del_examen/blob/master/5.txt) 

![image](https://user-images.githubusercontent.com/66692550/130687628-50810749-7479-4eea-9b35-92b180b87691.png)

El csv juegos_olimpicos se lo importra a MySQL en la base de datos con el mismo nombre del csv. 

![image](https://user-images.githubusercontent.com/66692550/130687656-a35bf640-a04f-45cd-b428-0452d0e40b66.png)

El mismo proceso se realiza para el juegosolimpicos.csv, estos datos se encuentran en la base de datos “juegosolimpicos” de MySQL. 

![image](https://user-images.githubusercontent.com/66692550/130687692-adb64504-1732-497c-810d-620a74c57edf.png)

Se transfiere los datos recopilados en MySQL hacia MongoDB para esto se deben exportar los datos de ambas bases, “juegos_olimpicos” y “juegosolimpicos” para importarlos a Mongo DB Compass. 
![image](https://user-images.githubusercontent.com/66692550/130689141-696acdee-fbbf-4786-b392-1d824cbdbc87.png)

![image](https://user-images.githubusercontent.com/66692550/130689172-36e6d0a9-fe8a-4cd6-83b8-d2f49dd48971.png)

Los dos datasets se encuentran en MongoDB en la base de datos llamada MySQL_MongoDB en la colección “juegosolimpicos” 
![image](https://user-images.githubusercontent.com/66656757/130689919-ecb487a4-62ba-4726-adae-ffc11cbd7106.png)



Para realizar la conexión de MongoCompass a MongoAtlas se hizo lo siguiente.

Primero, se ingresa a MongoAtlas mediante una cuenta de google y se crea un nuevo proyecto:
![image](https://user-images.githubusercontent.com/66534512/130698692-2348b1f3-57b3-4835-8abf-e1d24c30181c.png)

Luego, la plataforma online da la opción de agregar los miembros del proyecto:
![image](https://user-images.githubusercontent.com/66534512/130698786-24af8f0a-0474-4afa-ba7c-ca07f95dc632.png)

Después de crear el proyecto, se procede a crear una base de datos de forma gratuita:
![image](https://user-images.githubusercontent.com/66534512/130698875-91e9855b-2c13-4d81-a5b6-8d6ba00a618a.png)

![image](https://user-images.githubusercontent.com/66534512/130698891-55a8e0d5-67c2-4114-a1d7-9e4ad70ee2ad.png)

A continuación, se muestra el proceso de creación del clúster:
![image](https://user-images.githubusercontent.com/66534512/130698984-10ac27a2-ffc3-46bf-a9fb-c96ad43b85c8.png)

