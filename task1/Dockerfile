# Use Ubuntu 22.04 as base image
FROM ubuntu:22.04

# Set environment variables to skip prompts
ENV DEBIAN_FRONTEND=noninteractive

# Update and upgrade system
RUN apt-get update && apt-get upgrade -y

# Install Python3 and pip3
RUN apt-get install -y python3 python3-pip

# Fix externally-managed Python environment issue
RUN rm /usr/lib/python*/EXTERNALLY-MANAGED || true

# Install Flask using pip3
RUN pip3 install flask

# Set working directory
WORKDIR /app

# Copy Flask app file into container
COPY ./api.py /app/api.py

# Set the command to run the Flask server
CMD ["python3", "api.py"]
