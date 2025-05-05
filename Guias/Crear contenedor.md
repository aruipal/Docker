# Descargar imagen de MongoDB y crear contenedor
### 1️⃣ Descargar la imagen oficial de MongoDB
- Ejecuta el siguiente comando para obtener la última versión de MongoDB desde Docker Hub:
```
sudo docker pull mongo
```
- Si necesitas una versión específica, puedes agregar el número de versión. Por ejemplo:
```
sudo docker pull mongo:6.0
```
- Verificar la imagen descargada
```
sudo docker images
```
<image src="https://github.com/aruipal/Docker/blob/main/recursos/images.JPG" alt="images" width="520" height="80">
  
- Borrar una imagen por su id
```
sudo docker rmi <IMAGE_ID>
```
- Forzar la eliminación (si hay contenedores en uso).\
Si la imagen está siendo utilizada por un contenedor, intenta eliminarlo con:
```
sudo docker rm -f <CONTAINER_ID>
```
- Luego, elimina la imagen con:
```
sudo docker rmi -f <IMAGE_ID>
```
### 2️⃣ Crear y ejecutar un contenedor MongoDB
- Si quieres establecer una contraseña para el acceso:
```
sudo docker run -d --name mongodb-container -p 27017:27017 \
  -e MONGO_INITDB_ROOT_USERNAME=admin \
  -e MONGO_INITDB_ROOT_PASSWORD=secret mongo:4.4
```
**-d:** Ejecuta el contenedor en segundo plano.\
**--name mongodb-container:** Asigna un nombre al contenedor.\
**-p 27017:27017:** Expone el puerto predeterminado de MongoDB.

### 3️⃣ Verificar que el contenedor está corriendo
```
sudo docker ps
```
Esto mostrará la lista de contenedores en ejecución.

### 4️⃣ Acceder a MongoDB desde el contenedor
- Si quieres ingresar a la CLI de MongoDB:
```
sudo docker exec -it mongodb-container mongosh
```
Si aún no tienes **mongosh**, puedes usar **mongo**.

<image src="https://github.com/aruipal/Docker/blob/main/recursos/mongosh.JPG" alt="mongosh" width="750" height="200">
