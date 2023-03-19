FROM node:apline as teamalpha
WORKDIR /var/app
COPY package.json .
RUN npm install
COPY . .
RUN npm run build

FROM nginx
EXPOSE 80
COPY --from=teamappha /var/app/build /usr/share/nginx/html
