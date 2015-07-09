FROM golang:1.4.2

WORKDIR /go/src/github.com/grafana/grafana/
RUN apt-get -y install git
#ADD . /go/src/github.com/grafana/grafana
RUN git clone https://github.com/anarcher/grafana.git
RUN go run build.go setup
RUN godep restore
RUN go build .

RUN curl -sL https://deb.nodesource.com/setup_0.10 | bash -
RUN apt-get -y install nodejs
RUN npm install
RUN npm install -g grunt-cli
RUN grunt

CMD ["./grafana"]

