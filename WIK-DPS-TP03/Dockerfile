FROM rust:slim AS build_stage

WORKDIR /build

RUN adduser --group --no-create-home --disabled-login --system builder
RUN chown -R builder /build
USER builder

RUN cargo new --bin wik_dps_tp03
WORKDIR /build/wik_dps_tp03

COPY Cargo.* ./
RUN cargo build --release

RUN rm src/*.rs
RUN rm ./target/release/deps/wik_dps_tp03*

COPY ./src ./src
RUN cargo build --release

FROM rust:slim
WORKDIR /app
COPY --from=build_stage /build/wik_dps_tp03/target/release/wik_dps_tp03 ./

CMD ["/app"]