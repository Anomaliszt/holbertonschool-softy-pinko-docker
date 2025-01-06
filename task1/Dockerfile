# Use Ubuntu
FROM ubuntu:latest

# Update system
RUN apt update && apt upgrade -y

# Install Python and pip
RUN apt install python3 python3-pip -y 

# Configure pip
RUN rm /usr/lib/python*/EXTERNALLY-MANAGED

# Install Flask
RUN pip3 install flask

# Set workdir
WORKDIR /app

# Copy script
COPY app/api.py /app

# Expose port
EXPOSE 5252

# Run app
CMD [ "python3", "/app/api.py"]
