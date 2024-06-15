# Imagen base de Python
FROM python:3.9-slim

# Establece el directorio de trabajo dentro del contenedor
WORKDIR /app

# Copia el archivo requirements.txt (si tienes uno) al contenedor
# y luego instala las dependencias
COPY requirements.txt requirements.txt
RUN pip install -r requirements.txt

# Copia todo el contenido del directorio actual al directorio /app en el contenedor
COPY . .

# Comando para ejecutar la aplicación
CMD ["python", "app.py"]
