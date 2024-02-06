FROM nginx:alpine

WORKDIR /app/front

COPY /usr/share/nginx/html/index.html

#COPY . .

ENV WS_BACK_URL http://localhost:8080 

EXPOSE 80

ENTRYPOINT ["./app/front/entrypoint.sh"]