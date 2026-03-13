# Usamos Node 24
FROM node:24-alpine

# Carpeta de trabajo
WORKDIR /app

# Copiamos package.json y package-lock.json y hacemos npm install
COPY package*.json ./
RUN npm install

# Copiamos todo el código
COPY . .

# Exponemos el puerto
EXPOSE 4000

# Comando para arrancar backend
CMD ["npx", "ts-node", "index.ts"]