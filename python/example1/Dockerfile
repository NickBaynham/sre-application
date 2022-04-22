FROM ubuntu:20.04

RUN apt-get update -y && \
    apt-get install -y python3-pip python3-dev flask

# We copy just the requirements.txt first to leverage Docker cache
COPY ./requirements.txt /app/requirements.txt

WORKDIR /app

RUN pip3 install -r requirements.txt
RUN export FLASK_APP=main2
RUN export FLASK_ENV=development

COPY ./main2.py /app/main2.py

CMD [ "flask run" ]
