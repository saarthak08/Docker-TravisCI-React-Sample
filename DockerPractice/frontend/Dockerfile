FROM node:alpine as builder

WORKDIR "/app"

COPY DockerPractice/frontend/package.json .

RUN npm install
 
COPY DockerPractice/frontend/ .

RUN npm run build


FROM nginx

COPY --from=builder /app/build /usr/share/nginx/html

EXPOSE 80