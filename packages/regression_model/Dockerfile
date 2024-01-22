# Use Python 3.8 as the base image
FROM python:3.8

# Set the working directory inside the container
WORKDIR /app

# Copy the requirements.txt file to the container
COPY requirements.txt .

# Install dependencies from requirements.txt
RUN pip install -r requirements.txt

# Install tox
RUN pip install tox

# Copy the entire project into the container
COPY . .

# Command to run your Python application (or in this case, open a bash shell)
CMD [ "/bin/bash" ]