FROM ubuntu:20.04
RUN apt update && \
    apt install curl gnupg2 ca-certificates lsb-release ubuntu-keyring -y && \
    curl https://nginx.org/keys/nginx_signing.key | gpg --dearmor \
| tee /usr/share/keyrings/nginx-archive-keyring.gpg >/dev/null && \
    echo "deb [signed-by=/usr/share/keyrings/nginx-archive-keyring.gpg] http://nginx.org/packages/ubuntu `lsb_release -cs` nginx" | tee /etc/apt/sources.list.d/nginx.list && \
    printf "Package: *\nPin: origin nginx.org\nPin: release o=nginx\nPin-Priority: 900\n" > /etc/apt/preferences.d/99nginx && \
    apt update && \
    apt install nginx -y && \
    apt remove curl -y
CMD nginx && sleep 10000
