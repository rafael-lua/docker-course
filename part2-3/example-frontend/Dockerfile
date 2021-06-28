FROM alpine:3.14

EXPOSE 5000

WORKDIR /usr/src/app

RUN apk update && apk add curl && curl --version

RUN curl -sL https://deb.nodesource.com/setup_14.x 
RUN apk add --update nodejs npm
RUN node -v && npm -v

COPY . .

RUN npm install

ENV REACT_APP_BACKEND_URL=http://127.0.0.1:8080  
RUN npm run build
RUN npm install -g serve

CMD ["serve", "-s", "-l", "5000", "build"]

