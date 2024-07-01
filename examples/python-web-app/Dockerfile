FROM ubuntu

WORKDIR /app

COPY requirements.txt /app
COPY devops /app

RUN apt-get update -y && \
    apt-get install -y python3 python3-pip && \
    apt-get install -y python3.12-venv && \
    python3 -m venv my-venv && \
    my-venv/bin/pip install django && \
    my-venv/bin/pip install -r requirements.txt 

ENTRYPOINT ["python3"]
CMD ["manage.py", "runserver", "0.0.0.0:8000"]




