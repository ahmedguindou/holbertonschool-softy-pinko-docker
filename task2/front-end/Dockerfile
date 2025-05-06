# Use the latest official Nginx image
FROM nginx:latest

# Copy front-end files into the Nginx web directory
COPY ./softy-pinko-front-end /var/www/html/softy-pinko-front-end

# Copy custom Nginx config into container
COPY ./softy-pinko-front-end.conf /etc/nginx/conf.d/default.conf
