# Jupyter Docker Compose

A quick and easy setup for running Jupyter notebooks in a Dockerized environment, managed using [Docker Compose](https://docs.docker.com/compose/). This setup makes it simple to get up and running with Jupyter, share notebooks across multiple team members, and maintain consistent environments. It is also compatible with GitHub Code Spaces for remote development.

## Features

- GitHub Template repository for easy reuse.
- Dockerized Jupyter environment for consistent, reproducible notebook runs.
- Simplified sharing of notebooks using the `work` directory.
- Compatibility with GitHub Code Spaces for seamless remote development.

## Getting Started

Clone this repository to your local machine:

```bash
git clone https://github.com/nezhar/jupyter-docker-compose.git
```

Navigate to the project root directory:

```bash
cd jupyter-docker-compose
```

Build the the image for the Jupyter Notebook server:

```bash
docker compose build
```

Start the Jupyter Notebook server:

```bash
docker compose up
```

After running this command, the Jupyter Notebook server should be accessible at `http://localhost:8888`.

## Using GitHub Code Spaces

This setup can also be used with GitHub Code Spaces. All the necessary configuration is provided in the `devcontainer.json` file. Just open this repository in a new code space, and the environment will be ready to go.

## Directory Structure

- `./work`: This is the directory where you can add your Jupyter notebooks. It's mounted as a volume in the Docker container, so notebooks created and saved in the Jupyter Notebook IDE will persist here.

## Notes

The `requirements.txt` file is copied to the Docker container during the build process, and the Python dependencies listed within are installed. To add or update dependencies, modify this file, then rebuild the Docker image.

## Contributions

Contributions to this project are welcome! Please create an issue or submit a pull request.

## License

This project is licensed under the MIT License - see the LICENSE file for details.
