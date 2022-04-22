FROM ubuntu:20.04

RUN apt-get update -y && \
    apt-get install -y python3-pip python3-dev

# We copy just the requirements.txt first to leverage Docker cache
COPY ./requirements.txt /app/requirements.txt

WORKDIR /app

RUN pip3 install -r requirements.txt
RUN 

COPY ./main2.py /app/main2.py

ENTRYPOINT [ "python3" ]

CMD [ "main2.py" ]
