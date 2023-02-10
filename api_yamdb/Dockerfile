FROM python:3.7-slim

RUN mkdir /app

COPY . /app

RUN pip3 install -r /app/requirements.txt --no-cache-dir

WORKDIR /app

CMD ["gunicorn", "api_yamdb.wsgi:application", "--bind", "0:8000" ]
CMD ["python3", "manage.py", "runserver", "0:8000"]
