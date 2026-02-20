# Etapa 1: Construcción
FROM node:lts-alpine AS build
WORKDIR /app

# Copiar archivos de dependencias
COPY package*.json ./
RUN npm install

# Copiar el resto del código y construir el sitio
COPY . .
RUN npm run build

# Etapa 2: Servidor de Producción
FROM nginx:stable-alpine AS runtime

# Copiar los archivos estáticos desde la etapa de build
# Nota: Astro por defecto construye en la carpeta /dist
COPY --from=build /app/dist /usr/share/nginx/html

# Exponer el puerto 80
EXPOSE 80

CMD ["nginx", "-g", "daemon off;"]