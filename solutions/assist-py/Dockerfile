FROM python:3.11-slim

LABEL maintainer="manuk@lab.local"
LABEL version="1.0"
 
WORKDIR /app

ENV PORT=5455

COPY requirements.txt .

RUN pip install --no-cache-dir -r requirements.txt

COPY . .

EXPOSE ${PORT}

CMD uvicorn app.main:app --host 0.0.0.0 --port ${PORT}