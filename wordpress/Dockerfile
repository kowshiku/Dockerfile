# Use the latest version of the official WordPress image as a base
FROM wordpress:latest

# Set the working directory to /var/www/html
WORKDIR /var/www/html

# Copy the contents of the current directory to the working directory
COPY . .

# Install necessary packages
RUN apt-get update && apt-get install -y \
    curl \
    wget \
    vim \
    && rm -rf /var/lib/apt/lists/*

# Expose port 80 for HTTP traffic
EXPOSE 80

# Start the Apache web server
CMD ["apache2-foreground"]