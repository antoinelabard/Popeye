FROM python:3.11.5-slim as base
ENV FLASK_APP=app.py
WORKDIR /app
COPY . .

RUN pip3 install -r requirements.txt

EXPOSE 80

CMD ["flask", "run", "--host=0.0.0.0", "--port=80"]
