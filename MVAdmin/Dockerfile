FROM node:12.18.0 AS node
WORKDIR /app
COPY . .

RUN npm install
RUN npm run build --prod


FROM nginx:alpine
COPY --from=node /app/dist/MVAdmin /usr/share/nginx/html