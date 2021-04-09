FROM ubuntu:18.04

WORKDIR /tmp
RUN apt-get update && apt-get install -y curl

COPY init_script.sh .
RUN chmod +x init_script.sh

CMD ./init_script.sh
