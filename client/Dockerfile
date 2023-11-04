FROM node:14-alpine

COPY ["package.json", "client/"]
COPY ["src/*", "client/src/"]
COPY ["public/*", "client/public/"]

RUN ls -l

WORKDIR /client

RUN npm install

EXPOSE 3000

CMD ["npm", "start"]