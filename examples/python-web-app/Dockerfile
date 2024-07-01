FROM ubuntu

WORKDIR /app

COPY requirements.txt /app
COPY devops /app

RUN apt-get update -y && \
    #apt-get install -y python3.12-venv && \
    apt-get install -y python3 python3-pip && \ 
    apt-get install -y python3-requests && \
    #python3 -m venv my-venv && \
    #sudo -s
    #source ./my-venv/bin/activate && \
    #my-venv/bin/pip install django && \
    #my-venv/bin/pip install virtualenv virtualenvwrapper && \
    #my-venv/bin/pip install -r requirements.txt 
    pip install django && \
    pip install -r requirements.txt

ENTRYPOINT ["python3"]
CMD ["manage.py", "runserver", "0.0.0.0:8000"]




