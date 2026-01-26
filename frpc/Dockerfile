FROM alpine:latest

# Install dependencies needed for the download
RUN apk add --no-cache wget tar

# Download and install frpc
RUN wget https://github.com/fatedier/frp/releases/download/v0.58.0/frp_0.58.0_linux_amd64.tar.gz \
    && tar -xzf frp_0.58.0_linux_amd64.tar.gz \
    && mv frp_0.58.0_linux_amd64/frpc /usr/local/bin/frpc \
    && rm -rf frp_0.58.0_linux_amd64* \
    && apk del wget tar

# Run frpc by default
ENTRYPOINT ["/usr/local/bin/frpc"]
CMD ["-c", "/etc/frp/frpc.toml"]
