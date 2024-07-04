# Stage 1: Build Angular application
FROM node:14 AS build
RUN npm install -g @angular/cli
WORKDIR /app

COPY package*.json ./
RUN npm install
COPY . .


EXPOSE 4200
CMD ["ng", "serve"]


