FROM node 
RUN apt-get update && apt-get upgrade -y \
&& npm install -g express-generator@4 \
&& express /back
WORKDIR /back/
RUN npm i