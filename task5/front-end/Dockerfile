# Use Nginx as base image
FROM nginx:latest

# Copy the static website files to the Nginx HTML directory
COPY ./softy-pinko-front-end /var/www/html/softy-pinko-front-end

# Copy custom Nginx configuration
COPY ./softy-pinko-front-end.conf /etc/nginx/conf.d/default.conf

# Expose port 9000
EXPOSE 9000

# Start Nginx when the container runs
CMD ["nginx", "-g", "daemon off;"]