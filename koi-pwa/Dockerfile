FROM nginx:stable-alpine

# download the latest version of the koa-pwa
RUN wget https://github.com/koi-learning/koi-pwa/releases/download/latest/dist.zip
RUN unzip -o -q dist.zip -d /
RUN cp -rf /dist/* /usr/share/nginx/html/

# copy our config file
RUN rm /etc/nginx/conf.d/default.conf
COPY ./nginx.conf /etc/nginx/nginx.conf