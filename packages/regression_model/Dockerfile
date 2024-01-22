# Use Python 3.8 as the base image
FROM python:3.8

# Set the working directory inside the container
WORKDIR /app

# Copy the requirements.txt file to the container
COPY requirements.txt .

# Install dependencies
RUN pip install -r requirements.txt

# Copy the entire project into the container
COPY . .

# Command to run your Python application (replace with your own command)
CMD [ "/bin/bash" ]
