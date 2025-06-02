# Estructura de un proyecto Flask. 🌶️
- **Flask** es un <u>framework web de Python</u> pequeño y ligero que proporciona herramientas y funciones útiles que facilitan la creación de aplicaciones web en Python. 
- Ofrece flexibilidad a los desarrolladores y es un framework más accesible para los nuevos desarrolladores, ya que permite crear una aplicación web rápidamente con un solo archivo de Python.
---
A diferencia de otros frameworks más complejos como Django, Flask proporciona solo lo esencial para comenzar:
- Un servidor integrado.
- Un sistema de rutas.
- Una arquitectura mínima y herramientas básicas de desarrollo.


### 1️⃣ 💻 Preparando el entorno de programación.
<ins>virtualenv</ins> nos permite aislar nuestra aplicación junto con todas sus dependencias de otras aplicaciones Python que tengamos en nuestro sistema, de manera que las librerías de cada una de las aplicaciones no entren en conflicto.
- En nuestro servidor Ubuntu, o Visual Studio Code (Windows), preparamos nuestro entorno virtual.
  - Instalamos <ins>pip y virtualenv</ins>:
    - Actualizamos: ```sudo apt update```
    - Instalamos pip: ```sudo apt install python3-pip```
    - Instalamos virtualenv: ```sudo apt install python3-virtualenv```
    - Para comprobar la versión de python: ```python3 --version``` y de pip: ```pip3 --version```
      <image src="https://github.com/aruipal/Docker/blob/main/recursos/pip.JPG" alt="shell" width="600" height="100">
    
  - Para crear un entorno virtual nos situaremos en el directorio raíz de nuestro proyecto (cd /opt/proyecto) y ejecutaremos el siguiente comando: ```python3 -m venv venv```
  - Esto creará el directorio <ins>venv</ins>, el cuál contiene el entorno virtual:
    - El directorio **bin** (Scripts en Windows) contiene los ejecutables como el intérprete de Python o pip.
    - Los directorios **include y lib** contienen las librerías necesarias para correr nuestro código.
    - Las librerías de terceros se instalarán en **venv/lib/pythonX.X/site-packages/**.
  - Para activar el entono virtual:
    ```source venv/bin/activate```
  <image src="https://github.com/aruipal/Docker/blob/main/recursos/venv.JPG" alt="shell" width="600" height="150">
  
  *Al activarlo verás (venv) al inicio de la terminal*
  
  - Para desactivar el entorno virtual:
    ```deactivate```

### 2️⃣ 🌶️ Instalando Flask
- Para instalar Flask escribiremos en el terminal el siguiente comando:
```
pip install Flask
```
- De manera que dentro de nuestro entorno «venv», se instalarán el framework y las librerías que necesite.
- Podemos ver todas las dependencias de nuestra aplicación si ejecutamos el siguiente comando desde el terminal:
```
pip freeze
```
  <image src="https://github.com/aruipal/Docker/blob/main/recursos/dependencias.JPG" alt="shell" width="560" height="150">
    
- Crear/Actualizar el fichero requirements.txt:
```
pip freeze > requirements.txt
```

👌 Con esto ya tenemos todo listo para crear nuestra primera aplicación Flask.

### 3️⃣ Instalacion de pymongo


### 4️⃣ 🐍 Crear aplicación básica
- Crear archivo base **app.py**:
  - Se crea una ruta /
  - Corre en http://127.0.0.1:5000/




### Plantillas HTML
