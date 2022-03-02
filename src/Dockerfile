FROM alpine:3.15

RUN apk update
RUN apk add --no-cache curl

# Downloading local php security checker
RUN curl -o local-security-checker -L https://github.com/fabpot/local-php-security-checker/releases/download/v1.2.0/local-php-security-checker_1.2.0_linux_amd64
RUN chmod +x local-security-checker

RUN mv local-security-checker /usr/local/bin/local-security-checker

RUN rm -rf /var/cache/apk/*

RUN mkdir workdir

WORKDIR workdir
