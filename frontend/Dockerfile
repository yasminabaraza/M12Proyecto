FROM node:24.14

# Crear directorio de la app
WORKDIR /app

# Copiar package.json y package-lock.json
COPY package*.json ./

# Instalar dependencias + TypeScript + ts-node + tipos
RUN npm install \
    && npm install --save-dev typescript ts-node @types/node @types/express @types/cors @types/pg

# Copiar todo el código
COPY . .

# Exponer puerto
EXPOSE 5000

# Comando para desarrollo con ts-node
CMD ["npx", "ts-node", "index.ts"]