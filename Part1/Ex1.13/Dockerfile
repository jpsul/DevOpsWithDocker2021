FROM ubuntu

RUN apt-get update && apt-get install -y curl

RUN cd /tmp \
    && curl -sLO https://golang.org/dl/go1.16.3.linux-amd64.tar.gz \
    && tar -C /usr/local -zxvf go1.16.3.linux-amd64.tar.gz \
	&& rm go1.16.3.linux-amd64.tar.gz

ENV PATH=$PATH:/usr/local/go/bin	
ENV PORT=8080

EXPOSE 8080

WORKDIR /usr/src/app

COPY . .

RUN go build

CMD ["./server"]