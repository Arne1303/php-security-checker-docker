FROM alpine:3.15

# Installing curl
RUN apk update
RUN apk add --no-cache curl

# Downloading local php security checker
RUN curl -o local-security-checker -L https://github.com/fabpot/local-php-security-checker/releases/download/v1.2.0/local-php-security-checker_1.2.0_linux_amd64
RUN chmod +x local-security-checker

# Moving security checker to make it easely executable
RUN mv local-security-checker /usr/local/bin/local-security-checker

# Clearing cache
RUN rm -rf /var/cache/apk/*

# Creating workdir
RUN mkdir workdir
WORKDIR workdir
