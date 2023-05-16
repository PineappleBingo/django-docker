# ./django-docker/Dockerfile
FROM python:3.7.5-buster

# set environment variables
ENV PYTHONDONTWRITEBYTECODE 1
ENV PYTHONUNBUFFERED 1

# Install & use pipenv
COPY Pipfile Pipfile.lock ./
RUN python -m pip install --upgrade pip
RUN pip install pipenv && pipenv install --dev --system --deploy

WORKDIR /app
COPY . /app

# # install dependencies
# RUN pip install --upgrade pip
# COPY ./requirements.txt /opt/app/requirements.txt 
# RUN chmod +x /opt/app/requirements.txt
# RUN pip install -r requirements.txt
# # copy project
# COPY . /opt/app/




# # set work directory
# WORKDIR /opt/app
# # set environment variables
# ENV PYTHONDONTWRITEBYTECODE 1
# ENV PYTHONUNBUFFERED 1
# # install dependencies
# RUN pip install --upgrade pip
# COPY ./requirements.txt /opt/app/requirements.txt 
# RUN chmod +x /opt/app/requirements.txt
# RUN pip install -r requirements.txt
# # copy project
# COPY . /opt/app/