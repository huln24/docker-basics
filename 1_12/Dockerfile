FROM ubuntu:latest

EXPOSE 5001

WORKDIR /usr/src/app

COPY package.json ./

RUN apt-get update && apt-get install -y curl 
RUN curl -sL https://deb.nodesource.com/setup_16.x | bash && apt-get install -y nodejs

RUN npm install

COPY . ./

RUN npm run build

RUN npm install -g serve

CMD ["serve", "-s", "-l", "5001", "build"]
