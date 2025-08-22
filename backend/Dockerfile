FROM node:18-alpine

WORKDIR /usr/src/app

# Install dependencies
COPY package*.json ./
RUN npm ci --omit=dev || npm ci

# Copy source
COPY . .

ENV NODE_ENV=production
EXPOSE 5000

CMD ["node", "index.js"]


