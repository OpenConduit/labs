FROM jupyter/pyspark-notebook:python-3.11

USER root

# Install OS tools for "peeking" at files (hexdump, etc)
RUN apt-get update && apt-get install -y \
    postgresql-client \
    bsdmainutils \
    tree \
    && rm -rf /var/lib/apt/lists/*

USER ${NB_UID}

# Install Python packages
COPY requirements.txt /tmp/
RUN pip install --no-cache-dir -r /tmp/requirements.txt