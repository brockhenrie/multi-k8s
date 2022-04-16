FROM node:latest as builder
WORKDIR /app
COPY package.json .
RUN npm install
COPY . .
RUN npm run build --prod

FROM nginx
EXPOSE 80 443
COPY ./nginx/default.conf ./etc/nginx/conf.d/default.conf
COPY --from=builder ./app/dist/angular-app ./usr/share/nginx/html

