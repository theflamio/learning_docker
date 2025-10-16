# learning_docker — Quick start

## Prerequisites
- Docker installed and running on Windows.

## Build the image
Open PowerShell or CMD in the repository root (c:\Dev\learning_docker) and run:
```powershell
docker build -t hello-image:latest -f Dev/Dockerfile Dev
```

## Run the container (short runs)
Run and remove the container after it exits (prints HelloWorld output):
```powershell
docker run --rm hello-image:latest
```

## Run detached (background)
Start the container in the background:
```powershell
docker run --name hello-container -d hello-image:latest
```
Check logs and see containers:
```powershell
docker logs hello-container
docker ps -a
```

## Map a port (if your app listens, e.g. port 5000)
If you expose a port in the container, map it to the host:
```powershell
docker run --rm -p 5000:5000 hello-image:latest
```

## Notes
- Dev/Dockerfile copies HelloWorld.py which prints and exits; the container will stop immediately after the script finishes. To keep a container running, run a long‑lived process or modify the script/image.