

# Solana Development Environment with Docker

This guide will help you set up a Solana development environment using Docker. It will install Solana, Anchor, Metaboss, Metaplex, and the spl-token library. Additionally, it will mount a local directory inside the container to allow you to develop your project.

## Prerequisites

- Docker installed on your system

## Build the Docker Image

1. Clone this repository or copy the contents of the Dockerfile into your working directory.
2. Open a terminal in the working directory and build the Docker image by running the following command:

```
docker build -t solana-dev-env .
```

## Run the Docker Container

1. Create a directory on your local computer where you want to store your Solana project. For example, `/path/to/your/project/directory`.
2. Run the following command to start the Docker container and mount your local directory:

```
docker run -it --name solana-dev -v "/path/to/your/project/directory:/app" solana-dev-env
```

Replace `/path/to/your/project/directory` with the absolute path to your local directory.

This command will mount the `/path/to/your/project/directory` on your local machine inside the container at `/app`.

## Using the Solana Development Environment

After running the previous command, you'll be inside the Docker container. You can verify that everything is installed correctly by running the following commands:

- `solana --version`
- `anchor --version`
- `metaboss --version`
- `metaplex-cli --version`

Now you can start working on your Solana project. Any changes you make to files in the `/app` directory inside the container will be persistent in the `/path/to/your/project/directory` on your local machine.

## Managing the Docker Container

- To stop the container, run the following command in another terminal window:

```
docker stop solana-dev
```

- To restart the container, run:

```
docker start solana-dev
```

- To attach to the container in interactive mode, run:

```
docker attach solana-dev
```

- To permanently remove the container, run:

```
docker rm solana-dev
```

Note that removing the container will cause you to lose all data and changes made inside the container unless you've saved them to the mounted local directory.

Congratulations! You now have a fully configured and isolated Solana development environment using Docker, with the ability to work on your local project.
