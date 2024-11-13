# Use an official Python runtime as a parent image
FROM python:3.9-slim

# Set the working directory within the container to /app/notes
WORKDIR /app

# Copy the backend code (including the notes app and manage.py) into the container
COPY . .

# Install Python dependencies
RUN pip install --no-cache-dir -r requirements.txt

# Make migrations and migrate the Django database
RUN python manage.py makemigrations
RUN python manage.py migrate

# Expose the Django default port
EXPOSE 8000

# Run Django server
CMD ["python", "manage.py", "runserver", "0.0.0.0:8000"]