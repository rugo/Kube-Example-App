# Use an official Python runtime as a parent image
FROM python:3.8-slim

# Set the working directory in the container
WORKDIR /app
COPY requirements.txt /app

RUN pip install --no-cache-dir -r requirements.txt
# Copy the current directory contents into the container at /code
COPY . /app

# Install any needed packages specified in requirements.txt

# Make port 8000 available to the world outside this container
EXPOSE 8000

# Run gunicorn when the container launches
CMD ["gunicorn", "-b", "0.0.0.0:8000", "webapp:app"]