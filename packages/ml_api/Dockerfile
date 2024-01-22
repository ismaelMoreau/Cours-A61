# Use Python 3.8 as the base image
FROM python:3.8

# Set the working directory in the container
WORKDIR /app

# Copy the requirements.txt file and install packages
COPY requirements.txt .
RUN pip install -r requirements.txt
RUN pip install pytest

# Copy the rest of the application
COPY . /app

# Expose the port the app runs on
EXPOSE 5000

