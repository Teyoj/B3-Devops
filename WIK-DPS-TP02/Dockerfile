FROM rust:slim AS build_stage

WORKDIR /build
COPY . .
RUN cargo build --release

RUN adduser -S wikuser
USER wikuser

FROM rust:slim
COPY --from=build_stage /build .

ENTRYPOINT cargo run