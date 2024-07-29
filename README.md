![Banner](./img/portainer-agent.png)

# 🖥️ Portainer Agent

Portainer Agent es un repositorio que facilita la configuración de un agente Portainer utilizando Docker Compose.

## 📝 Descripción

Este repositorio contiene un archivo Docker Compose que configura un entorno completo para gestionar tus contenedores Docker a través del agente de Portainer. Incluye la configuración básica necesaria para poner en marcha el agente de Portainer.

## 🛠️ Instalación

### Requisitos

- Docker
- Docker Compose

### Pasos

1. Clona este repositorio:

```bash
git clone https://github.com/JSisques/portainer-agent.git
```

2. Navega hasta el directorio del repositorio:

```bash
cd portainer-agent
```

3. Ejecuta Docker Compose para iniciar el servicio:

```bash
docker-compose up -d
```

Esto iniciará el contenedor del agente de Portainer en segundo plano.

## 🚀 Uso

Una vez que el contenedor esté en ejecución, el agente de Portainer estará escuchando en:

- **Portainer Agent:** https://localhost:9001

## 👨‍💻 Autor

- Nombre: Javier Plaza Sisqués
- GitHub: [JSisques](https://github.com/JSisques)

## 📄 Archivos de Configuración

En este repositorio se incluye el archivo de configuración necesario para personalizar el comportamiento del agente de Portainer:

- **docker-compose.yml:** Configuración principal para desplegar el agente de Portainer.

## 🧾 Ejemplo de docker-compose.yml

Aquí está el archivo docker-compose.yml utilizado para esta configuración:

```yaml
version: "3"
services:
  portainer-agent:
    image: portainer/portainer-ce:latest
    container_name: portainer-agent
    hostname: portainer-agent
    volumes:
      - ./data:/data
    ports:
      - 9443:9443
    restart: unless-stopped
```
