# Use Python 3.8 as the base image
FROM python:3.8

# Set the working directory in the container
WORKDIR /app

# Copy the requirements.txt file and install packages
COPY regression_model/requirements.txt /app
RUN pip install -r requirements.txt
RUN pip install pytest tox flask

# Copy the rest of the application
COPY . /app

RUN cd /app/regression_model && \
    tox -e install_locally

RUN cd /app/regression_model && \
    pip install -e .


# Expose the port the app runs on
EXPOSE 5000

# Command to run your Python application (or in this case, open a bash shell)
CMD ["python", "ml_api/run.py"]