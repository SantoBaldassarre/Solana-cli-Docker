# Solana and Seahorse Development Environment Docker Container

This Docker container is tailored to support development on the Solana blockchain, equipped with the Seahorse language tools for a streamlined experience.

## Features

- **Ubuntu 20.04**: Used as the base image.
- **Rust**: Installed with cargo and rustfmt for code formatting.
- **Node.js and Yarn**: For managing project dependencies.
- **Solana**: Source code is directly cloned from the official Solana repository.

## Building the Container

To build this Docker container, use the following command:

```bash
docker build -t solana-seahorse-dev .
```


This command creates the Docker image with the tag `solana-seahorse-dev`, referencing the Dockerfile in the current directory.

## Running the Container

Run the container with:

```bash
docker run -it --name solana-seahorse-dev solana-seahorse-dev
```


This starts the container named `solana-seahorse-dev` in interactive mode with a terminal, using the built image.

## Using the Development Environment

Inside the container, you have access to a suite of development tools for Solana. These include:

* **Developing on Solana** : Utilize the CLI tools configured within the container.
* **Building Projects** : Use Rust and Cargo to compile and build Solana projects.
* **Seahorse Language Support** : Develop smart contracts using the Seahorse language specifically designed for Solana.
