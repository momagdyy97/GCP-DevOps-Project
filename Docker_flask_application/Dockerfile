FROM python:3.8-slim-buster
WORKDIR /app

# deps
COPY requirements.txt .
RUN pip3 install --no-cache-dir -r requirements.txt

# source
COPY . .

EXPOSE 5000

# Be explicit: point flask to app.py and bind host/port
CMD ["flask", "--app", "app.py", "run", "--host=0.0.0.0", "--port=5000"]
