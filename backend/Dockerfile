FROM node:24.14

WORKDIR /app

COPY package*.json ./

RUN npm install
RUN npm install --save-dev @types/node @types/express @types/cors @types/pg

COPY . .

EXPOSE 4000

CMD ["npx", "ts-node", "index.ts"]