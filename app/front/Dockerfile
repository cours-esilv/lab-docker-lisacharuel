FROM nginx:alpine

# Set the working directory in the container to the root of Nginx server
WORKDIR /usr/share/nginx/html

# Remove default nginx static assets
RUN rm -rf ./*

# Copy the static content (index.html) into the container
COPY index.html .

# Copy the entrypoint script into the container
COPY entrypoint.sh /entrypoint.sh

# Make the entrypoint script executable
RUN chmod +x /entrypoint.sh


# Use the entrypoint script to configure and start your application
ENTRYPOINT ["/entrypoint.sh"]

# By default, Nginx listens on port 80
EXPOSE 80