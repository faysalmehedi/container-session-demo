FROM ubuntu:20.04

RUN apt-get update -y
RUN apt-get install python3.9 -y
RUN apt-get install python3-pip -y

WORKDIR /app

COPY ./requirements.txt /app
RUN pip install -r requirements.txt

COPY . .

EXPOSE 5000

ENV FLASK_APP=app.py
CMD ["flask", "run", "--host", "0.0.0.0"]
