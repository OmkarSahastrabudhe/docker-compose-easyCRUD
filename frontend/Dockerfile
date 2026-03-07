FROM node:22-alpine AS build
WORKDIR /app
COPY . .
RUN npm install && npm run build

FROM httpd:latest
COPY --from=build /app/dist/  htdocs/
EXPOSE 80
CMD ["httpd", "-D", "FOREGROUND"]




