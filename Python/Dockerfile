FROM python:3.9

WORKDIR /app

COPY app.py /app

RUN pip install flask netifaces gunicorn

EXPOSE 8000

CMD ["gunicorn", "-w", "4", "-b", "0.0.0.0:8000", "app:app"]
