FROM node:22-alphine

WORKDIR /app/

COPY  . .

RUN apk update && apk add apache2

RUN npm install && npm run build 

RUN cp -r dist/*  /var/www/html/

EXPOSE 80

CMD [ "httpd","D","FOREGROUND"]

