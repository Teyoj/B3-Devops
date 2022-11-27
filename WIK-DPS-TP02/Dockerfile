FROM rust:slim
RUN useradd -ms /bin/bash hugoj
USER hugoj

COPY . .
ENTRYPOINT cargo run