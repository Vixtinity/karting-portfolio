FROM node:lts-alpine AS build
WORKDIR /app
COPY package*.json ./
RUN npm install
COPY . .
RUN npm run build

FROM node:lts-alpine
WORKDIR /app
COPY --from=build /app/dist .
EXPOSE 80
CMD ["npx", "serve", "-s", ".", "-l", "80"]