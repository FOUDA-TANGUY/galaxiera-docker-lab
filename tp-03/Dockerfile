FROM ubuntu:latest AS build

WORKDIR /lourd

RUN touch pata.txt && apt update && apt install apache2 -y

CMD service apache2 start && sleep infinity



FROM scratch AS leger

COPY --from=build /lourd /leger

