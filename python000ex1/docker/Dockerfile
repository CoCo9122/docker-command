FROM python:3.8.13-slim-buster

WORKDIR /usr/app/src

RUN apt-get update && apt-get -y install gcc libmariadb-dev

RUN pip install jupyterlab
RUN pip install numpy
RUN pip install matplotlib

CMD ["jupyter", "lab", "--port", "8080", "--ip=0.0.0.0", "--allow-root", "--no-browser"]