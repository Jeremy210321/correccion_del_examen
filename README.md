# Corrección del Examen de Análisis de Datos
## Integrantes:
##### *[Yazán Cindy](https://github.com/Cindyk2052)*
##### *[Guachamín Daniel](https://github.com/danielguachamin)*
##### *[León Jeremy](https://github.com/Jeremy210321)*


Para obtener las locaciones de las ciudades, se utilizó la herramienta en la web [Bounding Box](http://boundingbox.klokantech.com/) y el [script1](https://github.com/Jeremy210321/correccion_del_examen/blob/master/script1.ipynb) para pasar la información obtenida a CouchDB. Los datos se ven en la BDD de Couch. 

Locations 

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

Prosigue, la exportación de los dos datasets (“ciudades” y “olímpicos”) de twitter que se encuentran en CouchDB. 

![image](https://user-images.githubusercontent.com/66656757/130702819-6bd7b031-daa7-467f-ba52-bd3ec7a37821.png)

Esto se puede evidenciar con la herramienta Sublime

![image](https://user-images.githubusercontent.com/66656757/130702852-4b3c25ff-ea57-42c5-ab4e-8ef913718bb2.png)

Por último, se muestra la importación de los archivos bajados de CouchDB a MongoCompass:

![image](https://user-images.githubusercontent.com/66534512/130704110-563a3e28-5867-4ad1-a357-a76b6e35c18c.png)


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

Se creó el enlace desde MongoAtlas para establecer la conexión con MongoCompass:
![image](https://user-images.githubusercontent.com/66534512/130699632-1ad08d40-b26c-4dcd-82f0-0fc34c400f86.png)

Mediante el uso del [script 8](https://github.com/Jeremy210321/correccion_del_examen/blob/master/script8.ipynb) se pasaron los datos de MongoCompass a MongoAtlas.

Aquí se evidencia este proceso:
Datos de MongoCompass

![image](https://user-images.githubusercontent.com/66534512/130699767-06069f37-dcee-42be-a3ac-06e3da79f35e.png)

Datos de MongoAtlas

![MicrosoftTeams-image](https://user-images.githubusercontent.com/66692550/130703680-b3df8ce1-8d5f-4a1a-8885-10f084262843.png)

Se verificaron los datos dentro de la colección y la base de datos asignada:

![MicrosoftTeams-image](https://user-images.githubusercontent.com/66692550/130703756-7e925114-b5e0-4502-9df7-7768092f651c.png)

Ahora se procede a exportar la colección "coleccion_mongo" en archivos '.json' y '.csv'
![MicrosoftTeams-image](https://user-images.githubusercontent.com/66692550/130703828-8edfaa2d-1655-4dc1-a357-6c2ada995e1e.png)
![MicrosoftTeams-image (1)](https://user-images.githubusercontent.com/66692550/130703835-8d47e2bb-6cf8-459a-b0b4-121a9b11705c.png)

Para finalizar, comprobamos la correcta exportación de la colección en nuestro computador, los mismos que se evidencian en [mongo_correccionJSON](https://github.com/Jeremy210321/correccion_del_examen/blob/master/mongo_correccionJSON.json), [mongo_correccionCSV](https://github.com/Jeremy210321/correccion_del_examen/blob/master/mongo_correccionCSV.csv).

![MicrosoftTeams-image (2)](https://user-images.githubusercontent.com/66692550/130703874-c0fe07a7-51cc-4665-906e-3ee5ad555f87.png)
