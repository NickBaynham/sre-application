FROM ubuntu:20.04

RUN apt-get update -y && \
    apt-get install -y python-pip python-dev

RUN pip install --upgrade pip

# We copy just the requirements.txt first to leverage Docker cache
COPY ./requirements.txt /app/requirements.txt

WORKDIR /app

RUN pip install -r requirements.txt

COPY main2.py main2.py

ENTRYPOINT [ "python" ]

CMD [ "main2.py" ]
