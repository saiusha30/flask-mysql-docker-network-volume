# Use official Python image
FROM python:3.9

# Set working directory
WORKDIR /app

# Copy application files
COPY . /app

# Install dependencies
RUN pip install flask mysql-connector-python python-dotenv

# Expose port
EXPOSE 5000

# Start the Flask app
CMD ["python", "app.py"]

