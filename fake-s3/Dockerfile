FROM ruby:2

RUN gem install fakes3

VOLUME /data

EXPOSE 4567

ENTRYPOINT ["fakes3"]

CMD ["-r","/data","-p","4567"]
