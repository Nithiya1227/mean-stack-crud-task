# Stage 1: Build the Angular application
FROM node:18-alpine as build

WORKDIR /usr/src/app

COPY package*.json ./

RUN npm install

COPY . .

RUN npm run build

# Stage 2: Serve the application with Nginx
FROM nginx:alpine

# Copy the built output from Stage 1 to Nginx's default HTML directory
COPY --from=build /usr/src/app/dist/angular-15-crud /usr/share/nginx/html

EXPOSE 80

CMD ["nginx", "-g", "daemon off;"]
