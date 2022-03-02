FROM alpine:3.15

RUN apk update
RUN apk add --no-cache curl

# Downloading local php security checker
RUN mkdir checker-path && cd checker-path
RUN curl -o local-security-checker -L https://github.com/fabpot/local-php-security-checker/releases/download/v1.2.0/local-php-security-checker_1.2.0_linux_amd64
RUN chmod +x local-security-checker
RUN cd ..

ENV PATH="/checker-path:${PATH}"

RUN rm -rf /var/cache/apk/*

RUN mkdir src-dir

WORKDIR src-dir