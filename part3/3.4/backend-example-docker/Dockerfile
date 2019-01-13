FROM node:10.14.2-alpine

COPY ./package.json /app/
WORKDIR /app/
RUN npm i && npm cache clean --force

COPY . /app/

RUN adduser -D app
RUN chown -R app:app .
USER app

CMD npm start
