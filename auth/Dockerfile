FROM node:alpine

WORKDIR /app
COPY package.json ./
RUN npm install --omit=dev
COPY . .
RUN npm run build

EXPOSE 3000

# Run compiled JS
CMD ["node", "dist/index.js"]