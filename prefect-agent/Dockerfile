FROM vladmois/prefect-client

RUN apt update && apt install -y nginx
COPY route-conf.conf /etc/nginx/
RUN echo "include /etc/nginx/route-conf.conf;" >> /etc/nginx/nginx.conf

CMD service nginx start \
    && service nginx status >&2 \
    && (prefect server create-tenant -n default \
        || echo "Got exception while tenant creation. It probably already exists." >&2) \
    && prefect agent local start
