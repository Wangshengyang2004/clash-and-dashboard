FROM --platform=$TARGETPLATFORM dreamacro/clash:v1.16.0

EXPOSE 8080

RUN apk update && apk add nginx

COPY ./dist/ /dashboard
COPY ./build/nginx.conf /etc/nginx
COPY ./build/start.sh /
COPY ./config/config.yaml /root/.config/clash/config.yaml
ENTRYPOINT [ "sh", "/start.sh" ] 