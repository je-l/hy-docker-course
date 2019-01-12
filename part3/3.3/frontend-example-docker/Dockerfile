FROM node:10.14.2-alpine

COPY ./package.json /app/
WORKDIR /app/
RUN npm i

COPY . /app/

RUN npm run build

FROM nginx:1.15.8-alpine

COPY --from=0 /app/dist/ /usr/share/nginx/html
