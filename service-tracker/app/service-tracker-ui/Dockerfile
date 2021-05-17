FROM node:10

RUN mkdir -p /home/node/app && chown -R node:node /home/node/app
WORKDIR /home/node/app

RUN id
COPY package*.json ./
USER node
RUN npm install

COPY --chown=node:node . .
ENV NODE_ENV "development"
EXPOSE 8080

CMD [ "npm", "run", "container" ]

