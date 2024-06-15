# Ejercicio de DevOps

## Descripción General
Este repositorio contiene la solución para el ejercicio de DevOps, incluyendo un Dockerfile, configuración de pod de Kubernetes, pipeline de Azure DevOps y un diagrama para mejorar la observabilidad.

## Dockerfile
El `Dockerfile` se utiliza para construir una imagen Docker para un microservicio en Python.

### Variables
- `WORKDIR`: Directorio de trabajo dentro del contenedor Docker.
- `COPY`: Copia el contenido del directorio actual al contenedor en `/app`.
- `EXPOSE`: Expone el puerto 80 para el contenedor.
- `CMD`: Comando que se ejecuta al iniciar el contenedor.

## Configuración de Pod de Kubernetes
El archivo `pod.yaml` define un pod de Kubernetes para el microservicio en Python.

### Variables
- `name`: Nombre del pod.
- `namespace`: El namespace de Kubernetes (`tech-prod`).
- `image`: La imagen Docker (`image01:v1`).
- `memory`: Límite de memoria para el contenedor (`3Gi`).
- `nodeSelector`: Asegura que el pod se ejecute en nodos con la etiqueta `network: prod-internal`.

## Pipeline de Azure DevOps
El archivo `azure-pipelines.yml` configura un pipeline de CI/CD en Azure DevOps.

### Pasos
1. **Instalar Python**: Configura Python 3.x.
2. **Instalar Dependencias**: Instala los paquetes Python necesarios.
3. **Ejecutar Pruebas Unitarias**: Ejecuta las pruebas unitarias utilizando `unittest`.
4. **Construir y Publicar Imagen Docker**: Construye y publica la imagen Docker en un registro de contenedores.
5. **Publicar Artefacto**: Publica el `Dockerfile` como un artefacto.

## Diagrama de Observabilidad
El archivo `observability-diagram.png` ilustra la configuración de observabilidad utilizando Prometheus y Grafana.

![Diagrama de Observabilidad](observability-diagram.png)
