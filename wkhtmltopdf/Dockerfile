FROM debian:buster-slim
RUN apt update && \ 
    apt install -y ca-certificates wkhtmltopdf && \
    rm -Rf /var/lib/apt/lists/*