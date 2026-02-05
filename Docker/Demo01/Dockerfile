# Use an official Python image
FROM python:3.11-slim

# Set working directory inside the container
WORKDIR /app

# Copy dependency file first (better caching)
COPY requirements.txt .

# Install dependencies
RUN python -m pip install --upgrade pip \
 && python -m pip install --no-cache-dir -r requirements.txt
 

# Copy the rest of the application
COPY . .

# Run the application
CMD ["python", "app.py"]