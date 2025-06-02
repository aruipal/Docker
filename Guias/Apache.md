# 💻 Crear contenedor Apache
## ❗ No es necesario si en mi aplicación web voy a usar un framework como Flask.
### ✅ Paso 1: Crear un contenedor con Apache
- Puedes usar una imagen oficial de Apache basada en Debian (httpd):
```
sudo docker run -d --name apache-server -p 80:80 httpd:latest
```
- **-d:** ejecuta el contenedor en segundo plano (modo detached).
- **--name apache-server:** le da un nombre al contenedor.
- **-p 80:80:** mapea el puerto 80 del host al puerto 80 del contenedor.
- **httpd:latest:** usa la última versión oficial de Apache (httpd).

🔍 Puedes comprobar que el contenedor está corriendo:
```
sudo docker ps
```

### ✅ Paso 2: Verifica que el servidor esté funcionando
- Desde tu navegador, accede a la IP del servidor Ubuntu. Por ejemplo:
```
http://<IP-de-tu-servidor>
```
- Deberías ver el texto **It Works!**.
<image src="https://github.com/aruipal/Docker/blob/main/recursos/web.JPG" alt="web" width="400" height="120">

### ➡️ Acceder a la terminal del contenedor Apache desde Ubuntu:
- Usa docker exec para abrir una shell dentro del contenedor:
```
sudo docker exec -it apache-server bash
```
<image src="https://github.com/aruipal/Docker/blob/main/recursos/ShellApache.JPG" alt="shell" width="600" height="150">
  
### ➡️ Ruta del archivo index.html
- Una vez dentro del contenedor utiliza **ls** para listar el directorio.
- Después tienes que entrar en la carpeta **htdocs**.
```
cd htdocs
```
- Allí se encuentra el archivo **index.html**.
- Para modificarlo vamos a instalar el editor de texto **nano** 📋.
```
apt update
apt install nano
```
- Para editar el **index.html**:\
Cambiamos el texto de la primera linea con por ejemplo: **Hola Mundo!**
```
nano index.html
```
- Editalo y pulsa **Ctl + X** para cerrar el editor y pulsa **Y** y **enter** para guardar.
- Accede a la página desde el navegador y deberías ver los cambios.
<image src="https://github.com/aruipal/Docker/blob/main/recursos/webhola.JPG" alt="web" width="400" height="120">

# 👌
