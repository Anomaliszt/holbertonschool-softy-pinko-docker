# Use Ubuntu image
FROM ubuntu:latest

# Update and upgrade
RUN apt update && apt upgrade -y

# Install requirements
RUN apt install python3 python3-pip -y 

# Configure pip
RUN rm /usr/lib/python*/EXTERNALLY-MANAGED

# Install Flask
RUN pip3 install flask flask-cors

# Set work directory
WORKDIR /app

# Copy script
COPY ./api.py /app

# Expose port
EXPOSE 5252

# Run API
CMD [ "python3", "/app/api.py"]
