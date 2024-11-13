FROM nginx
LABEL maintainer="Dennis"
ARG MY_NAME=change my name
ARG MY_ID=change my id

RUN echo "MY_NAME: $MY_NAME" && echo "MY_ID: $MY_ID"

RUN apt-get update && apt-get install -y git sed

RUN mkdir /mycode && cd /mycode && git clone https://github.com/denhuf/DES424_6722808440.git
RUN cp -r /mycode/DES424_6722808440/src /usr/share/nginx/html/mygitweb

RUN sed -i 's/<MY_NAME>/'"${MY_NAME}"'/g' /usr/share/nginx/html/mygitweb/index.html
RUN sed -i 's/<MY_ID>/'"${MY_ID}"'/g' /usr/share/nginx/html/mygitweb/index.html
