FROM node:10

COPY ./package.json /app/
WORKDIR /app/
RUN npm i

COPY . /app/

RUN npm run build

FROM nginx:1.15.8-alpine

RUN adduser -D app

COPY --from=0 /app/dist/ /usr/share/nginx/html
COPY ./nginx.conf /etc/nginx/nginx.conf
