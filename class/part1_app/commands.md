## Building and Running the Docker Container

### Build the Docker Image
Use the following command to build the Docker image. Run it the directory where your `Dockerfile` is located. This command tags the image as `myimage:latest`:

```bash
docker build -t myimage:latest .
```

### Run the Docker Container
Run the container using the command below. This maps port `8000` on your local machine to port `8000` in the container:

```bash
docker run --name mycontainer -p 8000:8000 myimage:latest
```
