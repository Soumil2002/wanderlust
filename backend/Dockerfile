<<<<<<< HEAD
# Stage 1
FROM node:21 AS backend-builder

# setup the working dir
WORKDIR /app

# code
COPY . .

# packages install
RUN npm i

# tests
RUN npm run test

# Stage 2
FROM node:21-slim

# setup the working dir
WORKDIR /app

# copy the above stage as compressed
COPY --from=backend-builder /app .

COPY .env.docker .env

# Port
EXPOSE 5000

# App
CMD ["npm", "start"]
=======
FROM node:21

WORKDIR /app

COPY . .

RUN npm i

COPY .env.sample .env

EXPOSE 5000

CMD ["npm","start"]
>>>>>>> main
