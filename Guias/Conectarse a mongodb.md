# Cómo conectarte a MongoDB desde:

**1. 🌐 Mongo Express** (interfaz web)\
**2. 🧭 MongoDB Compass** (GUI de escritorio)

## ✅ 1. Conectarte con Mongo Express (interfaz web en navegador)
Para version MongoDB 4.4
### 📦 Paso 1: Lanzar Mongo Express apuntando a esa IP
- Descargar la imagen de Mongo Express y crear contenedor.
- Ejecuta el siguiente comando:
```
sudo docker run -d \
  --name mongo-express \
  --network host \
  -e ME_CONFIG_MONGODB_SERVER=127.0.0.1 \
  -e ME_CONFIG_MONGODB_PORT=27017 \
  -e ME_CONFIG_MONGODB_ADMINUSERNAME=admin \
  -e ME_CONFIG_MONGODB_ADMINPASSWORD=secret \
  -e ME_CONFIG_BASICAUTH_USERNAME=web \
  -e ME_CONFIG_BASICAUTH_PASSWORD=web123 \
  mongo-express:0.54.0
```
- 🔐 Esto hará que Mongo Express se conecte a la IP estática del servidor (donde está MongoDB corriendo).
- Cambiar los usuarios y contraseñas por los correspondientes.\
### 🌐 Acceder desde el navegador
- Desde cualquier equipo en la red, abre:
```
http://192.168.1.5:8081
```
- Y usa:
**Usuario web**: web\
**Contraseña web**: web123
<image src="https://github.com/aruipal/Docker/blob/main/recursos/express.JPG" alt="express" width="800" height="400">

___

## ✅ 2. Conectarte con MongoDB Compass (aplicación de escritorio)
### 💻 Paso 1: Descargar Compass
- Descarga desde: https://www.mongodb.com/try/download/compass

### 🔗 Paso 2: Ingresar la cadena de conexión
- En Compass, en la pantalla de inicio, elige “Fill in connection fields individually” o directamente pega la **URI de conexión**:
```
mongodb://admin:secret@192.168.1.5:27017/admin
```
<image src="https://github.com/aruipal/Docker/blob/main/recursos/compass.JPG" alt="compass" width="800" height="500">
  
### Si la conexión fue exitosa, verás la siguiente pantalla:

<image src="https://github.com/aruipal/Docker/blob/main/recursos/compass2.JPG" alt="compass2" width="300" height="400">


### 🚀 Si se conecta correctamente:
- Verás el dashboard de Compass con tus bases de datos, podrás explorar documentos, hacer consultas, y más.


