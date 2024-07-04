FROM node:16-alpine AS builder

WORKDIR /app

COPY package*.json ./

RUN npm install

COPY . .

RUN npm run build --prod

# Stage 2: Serve Angular application using Nginx
FROM nginx:alpine

COPY --from=build /app/dist/angular-15-client /usr/share/nginx/html

EXPOSE 80

CMD ["nginx", "-g", "daemon off;"]
