# data_platform
DataPlatform that uses Minio as datalake. Minio hosted on local machine.

## Run minio UI
1. Build the minio docker image
```bash
docker build -t data_platform .
```

2. Create folder for minio Volume
```bash
mkdir -p /minio-data
chomd -R a+rwx minio-data
```

3. Run the minio docker container
```bash
docker run -p 9000:9000 -p 9001:9001 -v $(pwd)/minio-data:/data data_platform
```