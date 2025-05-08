# Use Ubuntu 22.04 as base image
FROM ubuntu:22.04

# Set environment variable to skip interactive prompts
ENV DEBIAN_FRONTEND=noninteractive

# Update package list and install Python, pip, and required dependencies
RUN apt-get update && \
    apt-get install -y python3 python3-pip && \
    rm -rf /var/lib/apt/lists/*

# Remove EXTERNALLY-MANAGED to allow pip installs (safely skip if not found)
RUN rm -f /usr/lib/python3*/EXTERNALLY-MANAGED

# Install Flask and Flask-CORS via pip
RUN pip3 install --no-cache-dir flask flask-cors

# Set working directory
WORKDIR /app

# Copy Flask app into container
COPY ./api.py /app/api.py

# Run Flask app
CMD ["python3", "api.py"]