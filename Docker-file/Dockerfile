FROM ubuntu:latest

RUN apt-get -y update
RUN apt-get -y upgrade
RUN apt-get -y install python3-pip
RUN pip3 install flask

ENV HOME /home

COPY flaskapp /home/flaskapp

EXPOSE 5000

STOPSIGNAL SIGTERM

WORKDIR /home/flaskapp

ENTRYPOINT ["python3"]
CMD [ "helloworld.py" ]

# docker build -t ubuntu-flask:latest .