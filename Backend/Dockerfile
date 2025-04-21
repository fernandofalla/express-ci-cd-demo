# Usa una imagen base oficial de Node.js
FROM node:slim

# Establece el directorio de trabajo en el contenedor
WORKDIR /app

# Copia los archivos de dependencias primero para aprovechar el caché de Docker
COPY package*.json ./

# Instala las dependencias
RUN npm install

# Copia el resto del código de la aplicación
COPY . .

# Expone el puerto que usa tu app (3000 por defecto)
EXPOSE 3000

# Comando para correr la aplicación
CMD ["npm", "start"]
