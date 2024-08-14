FROM python:3.9-slim-bullseye

# Install necessary packages, including pkg-config and MariaDB client libraries
RUN apt-get update \
    && apt-get install -y --no-install-recommends \
        build-essential default-libmysqlclient-dev ffmpeg\
        pkg-config \
        libmariadb-dev \
    && pip install --no-cache-dir --upgrade pip \
    && apt-get clean \
    && rm -rf /var/lib/apt/lists/*

WORKDIR /app
COPY ./requirements.txt /app

# Install Python dependencies
RUN pip install --no-cache-dir -r /app/requirements.txt

COPY . /app

CMD ["python", "consumer.py"]
