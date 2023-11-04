# Use the Python 3.10 base image
FROM python:3.10

ENV PYTHONUNBUFFERED 1
ENV PYTHONDONTWRITEBYTECODE 1

RUN mkdir /code
COPY . /code/
WORKDIR /code

RUN /usr/local/bin/python -m pip install --upgrade pip
RUN python -m pip install -r /code/requirements.txt
RUN chmod +x /code/docker/entrypoints/entrypoint.sh

EXPOSE 8000
ENTRYPOINT ["/code/docker/entrypoints/entrypoint.sh"]
