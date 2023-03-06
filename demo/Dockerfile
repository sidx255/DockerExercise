FROM alpine:latest

# install nodejs
RUN apk add --update nodejs npm

# copy dependencies
COPY package.json /app/package.json
COPY package-lock.json /app/package-lock.json

# install dependencies
WORKDIR /app
RUN npm install

# copy app
COPY . /app

# run app
ENTRYPOINT ["npm", "start"]