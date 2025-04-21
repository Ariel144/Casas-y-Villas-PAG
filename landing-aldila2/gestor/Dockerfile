FROM node:20.18.0-alpine

# Establece el directorio de trabajo
WORKDIR /app

# Copia los archivos necesarios para instalar dependencias
COPY package.json package-lock.json ./

# Instala las dependencias
RUN npm install --production

# Copia todo el proyecto al contenedor
COPY . .

# Construye el proyecto
RUN npm run build

# Exponer el puerto por defecto de Payload CMS
EXPOSE 3000

# Configura las variables de entorno necesarias
ENV NODE_ENV production
ENV PORT 3000

# Comando para iniciar la aplicación
CMD ["npm", "start"]
