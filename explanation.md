## Base images 
## Backend And Client Base Image
The Alpine base image, used in the form of `node:13.12.0-alpine`, offers a significantly smaller footprint compared to many other distribution base images, resulting in notably leaner and more compact images overall.

## Database
  mongo - The only available image for Mongo DB.

## Dockerfile directives 

| Directive | what-it-does    | 
| :-----: | :---: | 
| FROM | This is used to specify the parent image of our custom Docker image   | 
|WORKDIR |     The WORKDIR instruction sets the working directory for any RUN, CMD, ENTRYPOINT, COPY and ADD instructions that follow it in the Dockerfile |
|RUN |         used to execute commands during the image build time |
|COPY|         The COPY instruction copies new files or directories from <src> and adds them to the filesystem of the container at the path <dest> |
|EXPOSE |      informs Docker that the container listens on the specified network ports at runtime|
|CMD    |      used to provide this default initialization command that will be executed when a container is created from the Docker image |

## Docker-compose Networking

Implemented separate networks for both the frontend and backend tiers to achieve isolation and enhance security. This setup facilitates communication between the frontend and backend, as well as between the backend and the database, through distinct networks.
```
networks:
  networks:
      yolo-network:
        ipv4_address: 172.18.0.5
  yolo-network:
  networks:
      yolo-network:
        ipv4_address: 172.18.0.3
```

## Running the Service successfully
I successfully executed the services on Docker, as depicted in the images below.

Running containers

![Alt text](./images/Screenshot%202023-08-18%20at%2019.40.58.png?raw=true "Running Container")

Frontend 
![Alt text](./images/Screenshot%202023-08-18%20at%2019.52.29.png?raw=true "Web app")

Backend API Call

![Alt text](./images/Screenshot%202023-08-18%20at%2019.55.22.png?raw=true "Backend Api Access")


## Naming images and containers

Named the images and containers to make them easy to indentify as below

![Alt text](./images/Screenshot%202023-08-18%20at%2019.19.27.png?raw=true "Named and versioned Images")

## Link to Docker Hub
[Docker-Hub](https://hub.docker.com/u/gloriamutie)

