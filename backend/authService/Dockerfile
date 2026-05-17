# syntax=docker/dockerfile:1
FROM node:20-alpine AS builder
WORKDIR /app
COPY package*.json ./
RUN npm ci --only=production
COPY . .
EXPOSE 3001  # Change per service: 3001 auth, 3002 streaming, etc.
CMD ["npm", "start"]
