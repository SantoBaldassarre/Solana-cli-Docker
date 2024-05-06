
# Solana Development Environment Docker Container

This Docker container is set up to provide a comprehensive Solana blockchain development environment. It includes all necessary dependencies for building and running Solana projects, along with tools like Rust, Node.js, Yarn, Anchor, and Metaboss.

## Features

- **Ubuntu 20.04**: Serves as the base image.
- **Rust**: Installed with cargo, rustfmt for code formatting.
- **Node.js and Yarn**: For managing project dependencies.
- **Solana**: Source code cloned directly from the official repository.
- **Anchor**: Framework for Solana's Sealevel runtime providing an easier experience for building projects.
- **Metaboss**: Command line tool suite for Metaplex metadata management on the Solana blockchain.

## Building the Container

To build this Docker container, you can use the following command:

```bash
docker build -t solana-anchor-metaboss.
```

This command builds the Docker image with the tag `solana-dev-env`, using the Dockerfile in the current directory.


## Running the Container

After building the image, run the container using:

```bash
docker run -it --name solana-anchor-metaboss solana-anchor-metaboss
```

This command starts a container named `my-solana-env` in interactive mode with a terminal, using the `solana-dev-env` image.


## Using the Development Environment

Once inside the container, you will have access to the full suite of development tools installed. Here are some things you can do:

* **Develop Solana Programs** : The Solana CLI tools are configured and ready.
* **Compile and Build Projects** : Utilize Rust and Cargo to build Solana programs.
* **Manage Smart Contract Metadata** : With Metaboss, you can manage metadata for Solana's Metaplex protocol.
