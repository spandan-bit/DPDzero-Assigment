# Use an official Python runtime as a parent image
FROM python:3.12-slim

# Set the working directory in the container
WORKDIR /app

# Install uv, a fast Python package installer
RUN pip install uv

# Copy the dependency definition files
COPY pyproject.toml ./

# Install dependencies using uv from pyproject.toml into the system environment
RUN uv pip install --system --no-cache .

# Copy the rest of the application's code
COPY app.py .

# Expose the port the app runs on
EXPOSE 8002

# Command to run the application
CMD ["python", "app.py"]
