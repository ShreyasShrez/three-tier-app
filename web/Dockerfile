FROM node:22-alpine3.19

COPY ./bin /app/bin
COPY ./public /app/public
COPY ./routes /app/routes
COPY ./views /app/views
COPY ./app.js /app/
COPY ./package.json /app/

WORKDIR /app

RUN npm install

EXPOSE 3000

ENTRYPOINT ["npm", "start"]
