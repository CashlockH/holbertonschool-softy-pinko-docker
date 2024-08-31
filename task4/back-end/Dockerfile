FROM ubuntu:latest
RUN apt-get update
RUN apt-get upgrade -y
RUN apt-get install python3 -y
RUN apt-get install python3-pip -y
RUN rm /usr/lib/python*/EXTERNALLY-MANAGED
RUN pip3 install flask
RUN pip3 install flask-cors
WORKDIR /app
COPY . /app
EXPOSE 5252
ENV FLASK_APP=api.py
CMD ["flask", "run", "--host=0.0.0.0", "--port=5252"]