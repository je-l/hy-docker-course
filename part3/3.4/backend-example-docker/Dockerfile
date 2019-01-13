FROM node:10

COPY ./package.json /app/
WORKDIR /app/
RUN npm i && npm cache clean --force

COPY . /app/

RUN adduser --disabled-password --gecos "" app
RUN chown -R app:app .
USER app

CMD npm start
