FROM python:3.7-slim

WORKDIR /app

COPY api_yamdb/requirements.txt /app

RUN pip3 install --upgrade pip

RUN pip3 install -r requirements.txt --no-cache-dir

COPY api_yamdb/ /app

ENV SEC_KEY=api_yamdb/api_yamdb/settings

CMD ["gunicorn", "api_yamdb.wsgi:application", "--bind", "0:8000" ]