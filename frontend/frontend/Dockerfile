FROM node:18

WORKDIR /app

COPY package*.json ./
RUN npm ci --ignore-optional
RUN npm install -g vite

COPY . .

EXPOSE 5174

CMD ["npm", "run", "dev"]