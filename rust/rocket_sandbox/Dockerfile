FROM rust:latest AS build-env

WORKDIR /

COPY src ./src
COPY Cargo.toml Cargo.lock ./

RUN cargo build --release

# Rlease Stage
FROM debian:12-slim
WORKDIR /

COPY --from=build-env /target/release/rocket_sandbox ./

ENV ROCKET_ADDRESS=0.0.0.0
EXPOSE 8000

CMD ["./rocket_sandbox"]