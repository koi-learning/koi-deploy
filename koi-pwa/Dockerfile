FROM nginx:stable-alpine

RUN wget https://github.com/koi-learning/koi-pwa/releases/download/latest/dist.zip
RUN unzip -o -q dist.zip -d /
RUN cp -rf /dist/* /usr/share/nginx/html/

RUN rm /etc/nginx/conf.d/default.conf
COPY ./nginx.conf /etc/nginx/nginx.conf