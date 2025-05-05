# Instalación de Docker en Ubuntu
### 1️⃣ Actualizar el sistema
- Antes de comenzar, asegúrate de que tu sistema está actualizado:
```
sudo apt update && sudo apt upgrade -y
```
### 2️⃣ Instalar paquetes necesarios
- Docker requiere algunos paquetes adicionales:
```
sudo apt install ca-certificates curl gnupg -y
```
### 3️⃣ Agregar el repositorio oficial de Docker
- Importa la clave GPG y añade el repositorio:
```
sudo install -m 0755 -d /etc/apt/keyrings
curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo tee /etc/apt/keyrings/docker.asc > /dev/null
echo "deb [arch=$(dpkg --print-architecture) signed-by=/etc/apt/keyrings/docker.asc] https://download.docker.com/linux/ubuntu $(lsb_release -cs) stable" | sudo tee /etc/apt/sources.list.d/docker.list > /dev/null
```
- Luego, actualiza los paquetes disponibles:
```
sudo apt update
```
### 4️⃣ Instalar Docker
- Ahora instala Docker y sus componentes:
```
sudo apt install docker-ce docker-ce-cli containerd.io docker-buildx-plugin docker-compose-plugin -y
```
### 5️⃣ Verificar instalación
- Después de la instalación, confirma que Docker está funcionando correctamente:
```
sudo systemctl enable --now docker
sudo docker --version
sudo docker run hello-world
```
- Esto te devolverá un mensaje de bienvenida si todo está en orden. 🚀
