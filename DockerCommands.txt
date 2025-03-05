### Basic Docker Commands
- `docker --version`  # Check Docker version
- `docker info`  # Show system information

### Container Management
- `docker run -d -p 8080:80 --name mycontainer nginx`  # Run a container
- `docker ps`  # List running containers
- `docker ps -a`  # List all containers (including stopped ones)
- `docker stop container_id`  # Stop a container
- `docker start container_id`  # Start a container
- `docker restart container_id`  # Restart a container
- `docker rm container_id`  # Remove a stopped container
- `docker container prune`  # Remove all stopped containers

### Image Management
- `docker images`  # List available images
- `docker pull nginx`  # Pull an image from Docker Hub
- `docker rmi image_id`  # Remove an image
- `docker image prune`  # Remove unused images
- `docker build -t myimage .`  # Build an image from a Dockerfile

### Volume & Network Management
- `docker volume ls`  # List volumes
- `docker volume create myvolume`  # Create a volume
- `docker volume rm myvolume`  # Remove a volume
- `docker network ls`  # List networks
- `docker network create mynetwork`  # Create a network
- `docker network connect mynetwork container_id`  # Connect a container to a network
- `docker network disconnect mynetwork container_id`  # Disconnect a container from a network

### Logs & Monitoring
- `docker logs container_id`  # View container logs
- `docker logs -f container_id`  # Follow logs in real-time
- `docker top container_id`  # View running processes in a container
- `docker stats`  # View resource usage

### Docker Compose
- `docker-compose up -d`  # Start services from a docker-compose.yml file
- `docker-compose down`  # Stop services
- `docker-compose restart`  # Restart services
