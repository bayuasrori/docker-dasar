FROM python:3.9
ENV PYTHONUNBUFFERED=1

USER root

WORKDIR /code
COPY requirements.txt /code/
RUN pip install -r requirements.txt
COPY . /code/
RUN python3 manage.py makemigrations
RUN python3 manage.py migrate

