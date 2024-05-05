FROM node:22-alpine3.19

COPY ./bin /app/bin
COPY ./app.js /app/
COPY ./package.json /app/

WORKDIR /app

RUN npm install

EXPOSE 8080

HEALTHCHECK --interval=10s --timeout=3s \
    CMD curl -f -s http://localhost:8080/api/status

ENTRYPOINT ["npm", "start"]
