FROM python:alpine3.17

COPY . .

EXPOSE 80

RUN pip install -r requirements.txt

RUN pip install gunicorn

RUN pip freeze > requirements.txt

CMD ["python3", "app.py"]