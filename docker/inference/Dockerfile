# Base image
FROM python:3.11-slim

# Setup working directory
WORKDIR /app

# Copy requirements.txt and install dependencies
COPY docker/inference/requirements.txt .
RUN pip install --no-cache-dir -r requirements.txt

# Copy the training script to the working directory
COPY docker/inference/server.py .

# Expone el puerto 8080 (que es el que definimos en el código de Flask)
EXPOSE 8080

# TODO: Set the command to run the training script
CMD ["python", "server.py"]
