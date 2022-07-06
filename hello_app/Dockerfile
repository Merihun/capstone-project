FROM python:3.7.9-stretch
# python:3.7-slim-buster

LABEL author="merihun.m@yahoo.com"

# Working Directory
WORKDIR /app

ENV PIP_NO_CACHE_DIR=1
# Copy source code to working directory
COPY . /app/

# Install packages from requirements.txt
# hadolint ignore=DL3013
RUN pip install --upgrade pip && \
    pip install --trusted-host pypi.python.org -r requirements.txt
# RUN pip install  --no-cache-dir --upgrade pip && \
#     pip install  --no-cache-dir --trusted-host pypi.python.org -r requirements.txt

# Expose port 80
EXPOSE 80

# Run app at container launch
CMD ["python", "hello.py"]
