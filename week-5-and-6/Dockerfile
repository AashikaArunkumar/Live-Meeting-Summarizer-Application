# Use a lightweight Python base image
FROM python:3.11-slim

# Prevent Python from writing pyc files to disk and buffering stdout/stderr
ENV PYTHONDONTWRITEBYTECODE=1
ENV PYTHONUNBUFFERED=1

# Set the working directory
WORKDIR /app

# Install system dependencies including FFmpeg!
RUN apt-get update && apt-get install -y \
    ffmpeg \
    build-essential \
    && rm -rf /var/lib/apt/lists/*

# First, install the CPU-only version of PyTorch to save massive amounts of space & time
# This stops pip from downloading the 3GB GPU version
RUN pip install torch torchaudio --index-url https://download.pytorch.org/whl/cpu

# Copy the requirements file and install the rest of the dependencies
COPY requirements.txt .
RUN pip install --no-cache-dir -r requirements.txt

# Copy the rest of the application code
COPY server.py backend.py ./

# Expose the port Render uses
EXPOSE 10000

# Command to run the FastAPI application on Render's required port mapping
CMD ["uvicorn", "server:app", "--host", "0.0.0.0", "--port", "10000"]
