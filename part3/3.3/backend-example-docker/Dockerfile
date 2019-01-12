FROM node:10.14.2-alpine

COPY ./package.json /app/
WORKDIR /app/
RUN npm i && npm cache clean --force

COPY . /app/

CMD npm start
