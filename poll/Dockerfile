FROM python:3.11.5-slim as base
ENV PYTHONDONTWRITEBYTECODE=1
ENV PYTHONUNBUFFERED=1
WORKDIR /app

RUN --mount=type=cache,target=/root/.cache/pip \
    --mount=type=bind,source=requirements.txt,target=requirements.txt \
    pip3 install -r requirements.txt

COPY . .
EXPOSE 80
CMD falsk run --host=0.0.0.0 --port=80
