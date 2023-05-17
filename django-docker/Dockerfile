# ./django-docker/Dockerfile
FROM python:3.11-bullseye

# set environment variables
ENV PYTHONDONTWRITEBYTECODE 1
ENV PYTHONUNBUFFERED 1

WORKDIR /app

# Install & use pipenv
COPY Pipfile requirements.txt ./
RUN python3 -m pip install \
    --trusted-host pypi.org --trusted-host files.pythonhosted.org \
    --upgrade pip

RUN pip3 install --trusted-host pypi.org --trusted-host files.pythonhosted.org \
    pipenv \
    && \
    pipenv install -r requirements.txt
# pipenv lock --pre && \
#  --skip-lock
# pipenv install --dev --system --deploy


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


# # Install & use pipenv
# COPY Pipfile Pipfile.lock ./
# RUN python3 -m pip install \
#     --trusted-host pypi.org --trusted-host files.pythonhosted.org \
#     --upgrade pip
# RUN pip3 install --trusted-host pypi.org --trusted-host files.pythonhosted.org \
#     pipenv \
#     && \
#     pipenv install --dev --system --deploy
