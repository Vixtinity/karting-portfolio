# Etapa 1: Construcción
FROM node:lts-alpine AS build
WORKDIR /app
COPY package*.json ./
RUN npm install
COPY . .
RUN npm run build

# Etapa 2: Servidor (Usando 'serve')
FROM node:lts-alpine AS runtime
WORKDIR /app

# Instalamos 'serve' para entregar los archivos estáticos
RUN npm install -g serve

# Copiamos solo los archivos construidos de la etapa anterior
COPY --from=build /app/dist ./dist

# Exponemos el puerto 80
EXPOSE 80

# Comando para servir la carpeta dist en el puerto 80
# -s es para Single Page Application (evita errores 404 al recargar)
CMD ["serve", "-s", "dist", "-l", "80"]