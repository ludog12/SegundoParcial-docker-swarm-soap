# Instrucciones de Ejecución con Docker Swarm y SOAP

Este README proporciona una guía detallada sobre cómo ejecutar el proyecto utilizando Docker Swarm y SOAP.

## Pasos a Seguir

### Paso 1: Preparación del Entorno

En la línea de comandos (CMD), navega hasta la carpeta del proyecto:

```bash
cd tp_docker_swarm_soap-main
```

### Paso 2: Construcción de la Base de Datos en Docker

Ejecuta el siguiente comando para construir la imagen de la base de datos para Docker Swarm:

```bash
docker build -t db_swarm_parcial .
```

### Paso 3: Construcción del Servicio REST

Navega a la carpeta `rest_service` y ejecuta:

```bash
docker build -t servicio_rest .
```

### Paso 4: Construcción del Servicio SOAP

Navega a la carpeta `soap_service` y ejecuta:

```bash
docker build -t swarm_soap_service .
```

### Paso 5: Construcción del Servicio Frontend

Navega a la carpeta `view` y ejecuta:

```bash
docker build -t swarm_front_service .
```

### Paso 6: Inicialización de Docker Swarm

Vuelve a la carpeta principal del proyecto y ejecuta:

```bash
docker swarm init
```

### Paso 7: Implementación del Proyecto con Docker Compose

Ejecuta el siguiente comando para implementar el proyecto utilizando el archivo `docker_compose.yml`:

```bash
docker stack deploy -c docker_compose.yml parcial 
```

Estos pasos te permitirán desplegar la aplicación en un entorno de Docker Swarm. Asegúrate de seguir las instrucciones detalladas en cada paso y verifica la salida de los comandos para detectar posibles errores.
