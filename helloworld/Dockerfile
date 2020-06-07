FROM gcc:8.2 as builder
COPY . /hellosrc
WORKDIR /hellosrc
RUN gcc hello.c -o hello.out

FROM alpine:latest
COPY --from=builder /hellosrc/hello.out /hello.out
CMD ["/hello.out"]
