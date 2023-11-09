# docker-image-for-.net-4.5
1. First need to create Dockerfile and this file must be in the main directory of that project.   --- must be the name like Dockerfile
2. Inside Dockerfile need to copy and past the bellow code
```
FROM mcr.microsoft.com/dotnet/framework/aspnet:4.8-windowsservercore-ltsc2019

WORKDIR /inetpub/wwwroot

# Copy the application files
COPY . .

# Expose the default HTTP port
EXPOSE 80
```
3. Build and Run:

Build the Docker image using the docker build command.
Run the Docker container using the docker run command, specifying the exposed ports and any other runtime options.
Example commands:
```
docker build -t your-image-name .
docker run -p 8080:80 --name your-container-name your-image-name
```
