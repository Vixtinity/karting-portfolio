FROM node:lts-alpine AS build
WORKDIR /app
COPY package*.json ./
RUN npm install
COPY . .
RUN npm run build

# Solo necesitamos los archivos estáticos, sin Nginx
FROM alpine:3.18
WORKDIR /app
COPY --from=build /app/dist .