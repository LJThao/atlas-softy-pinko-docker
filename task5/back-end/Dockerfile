FROM ubuntu:22.04
RUN apt-get update
RUN apt-get upgrade -y
RUN apt-get install -y python3 python3-pip
RUN pip3 install flask
RUN pip3 install flask-cors
COPY api.py /app/api.py
WORKDIR /app
CMD ["python3", "/app/api.py"]