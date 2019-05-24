FROM promregator/promregator:0.5.7
COPY promregator.yml /etc/promregator/promregator.yml

ARG username="please set pcf username using --build-arg"
ARG password="please set pcf password using --build-arg"

ENV CF_USERNAME=$username
ENV CF_PASSWORD=$password

EXPOSE 9393/tcp