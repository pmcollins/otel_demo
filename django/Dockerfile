FROM python:3.10
WORKDIR /app
COPY . /app
RUN pip install --no-cache-dir -r requirements.txt
EXPOSE 4317
CMD ["python", "manage.py", "ingest"]
