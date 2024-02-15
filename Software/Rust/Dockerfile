FROM rust

WORKDIR /comilador
COPY . .

RUN apt-get update -y
RUN apt-get upgrade -y
RUN apt-get -y install avr-libc gcc-avr pkg-config avrdude libudev-dev build-essential
# RUN cargo +stable install ravedude


CMD [ "cargo", "build" ]
