FROM python:3.7-slim

RUN mkdir /app

WORKDIR /app/api_yamdb

COPY api_yamdb/requirements.txt /app

RUN pip3 install -r /app/requirements.txt --no-cache-dir

COPY requirements.txt/ /app

CMD ["gunicorn", "api_yamdb.wsgi:application", "--bind", "0:8000" ]
