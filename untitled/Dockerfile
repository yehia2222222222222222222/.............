# Use official lightweight Alpine-based Nginx
FROM nginx:alpine

# Remove default Nginx website
RUN rm -rf /usr/share/nginx/html/*

# Copy your car website HTML file into Nginx's web root as index.html
COPY car_showroom.html /usr/share/nginx/html/index.html

# (Optional) If you have extra assets like images/css/js folders, copy them:
# COPY assets /usr/share/nginx/html/assets/

# Copy custom Nginx configuration for gzip compression and clean routing
COPY nginx.conf /etc/nginx/conf.d/default.conf

# Expose HTTP port 80
EXPOSE 80

# Start Nginx in the foreground
CMD ["nginx", "-g", "daemon off;"]