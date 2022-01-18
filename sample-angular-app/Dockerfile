FROM node:latest as build

WORKDIR /usr/local/app

COPY . .

RUN npm install npm-run-all --save-dev


RUN npm run build

FROM nginx:latest

COPY --from=build /usr/local/app/dist/sample-angular-app /usr/share/nginx/html

EXPOSE 80
