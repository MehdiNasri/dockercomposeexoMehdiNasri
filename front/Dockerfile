FROM node as build
RUN apt-get update && apt-get upgrade -y \
&& npm i @angular/cli -g
RUN ng new front-app
WORKDIR /front-app/
RUN npm run build

#Stage 2 : Run the app
FROM nginx as run
COPY --from=build front-app/dist/front-app /usr/share/nginx/html