### 🐳-image for the Php Security Checker

This Docker image packs the [php security checker](https://github.com/fabpot/local-php-security-checker) into a standalone docker image which can be used in pipelines to check for known security issues in you're composer dependencies.

The Security checker is executable from everywhere in the image by calling "local-security-checker"


### Gitlab-Ci

Example setup for the gitlab-ci

```yaml
# Checks the composer dependencies for known security flaws
Check Composer packages:
  stage: testing
  image: ghcr.io/arne1303/php-security-checker-docker:main
  when: always
  script:
    - local-security-checker
```