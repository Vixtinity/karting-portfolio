# --------- FASE 1: Build ---------
FROM node:20-alpine AS builder

WORKDIR /app

COPY package*.json ./
RUN npm install

COPY . .
RUN npm run build


# --------- FASE 2: Producción ---------
FROM nginx:alpine

# Borramos config default
RUN rm -rf /usr/share/nginx/html/*

# Copiamos el build de Astro
COPY --from=builder /app/dist /usr/share/nginx/html

EXPOSE 80

CMD ["nginx", "-g", "daemon off;"]