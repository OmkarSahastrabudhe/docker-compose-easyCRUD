FROM node:22-alpine AS build

WORKDIR /app/

COPY  . .

#RUN apk update && apk add apache2

RUN npm install && npm run build 

FROM httpd:latest

COPY --from=build /app/dist/   htdocs/

EXPOSE 80

CMD [ "httpd","-D","FOREGROUND"]

