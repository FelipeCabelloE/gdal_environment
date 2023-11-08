# Use an official Python runtime as a parent image
FROM python:3.8-slim-buster

# Set the working directory in the container to /app
WORKDIR /app

# Add metadata to the image to describe that the container is used for
LABEL org.opencontainers.image.title="GDAL Dev Container" \
      org.opencontainers.image.description="Development container for GDAL"

# Install any needed packages specified in requirements.txt
# COPY requirements.txt /app
# RUN pip install --no-cache-dir -r requirements.txt

# Install GDAL
RUN apt-get update && apt-get install -y \
    libgdal-dev \
    && rm -rf /var/lib/apt/lists/*

# Set environment variables
ENV CPLUS_INCLUDE_PATH=/usr/include/gdal
ENV C_INCLUDE_PATH=/usr/include/gdal

# Run app.py when the container launches
# CMD ["python", "app.py"]