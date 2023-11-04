FROM node:14-alpine

COPY ["package.json", "backend/"]
# COPY ["src/*", "client/src/"]
# COPY ["public/*", "client/public/"]

WORKDIR /backend

RUN npm install

EXPOSE 5001

CMD ["npm", "start"]