FROM node:14-alpine as builder

WORKDIR /app

COPY package.json .

RUN npm install -g @ionic/cli

RUN npm i -D typescript@3.5.3

RUN npm install @angular/cli -g

RUN npm install

COPY . /app/

RUN ionic build --prod

FROM nginx
RUN rm -rf /var/www/html/*
COPY --from=builder /app/www /usr/share/nginx/html
