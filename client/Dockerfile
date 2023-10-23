FROM node:alpine
# 安装 bash
RUN apk update && apk add bash
WORKDIR /client

COPY package.json yarn.lock ./

RUN apk add curl && \
    yarn install && yarn cache clean


COPY . .

EXPOSE 8080
CMD ["yarn", "dev","--port","8080","--host", "0.0.0.0"]


#  docker build -t go_react_todos/client .           
# docker run -d -p 8080:8080 go_react_todos/client
# docker run -p 8080:8080 go_react_todos/client
