# Use the official MinIO image as the base
FROM minio/minio

# Set environment variables (optional, but avoid hardcoding secrets here)
#ENV MINIO_ROOT_USER=<your-root-user> \
#    MINIO_ROOT_PASSWORD=<your-root-pwd>

# Expose ports for API and Console
EXPOSE 9000 9001

# Persist data (declare a volume)
VOLUME /data

# Start MinIO server
CMD ["server", "/data", "--console-address", ":9001"]