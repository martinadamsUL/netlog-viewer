# NetLog Viewer Docker Container

This repository contains a Docker setup for serving the NetLog Viewer webapp locally. The NetLog Viewer allows you to load and analyze NetLog dumps exported from Chrome. This setup uses an Ubuntu base image and Python's SimpleHTTPServer to serve the webapp.

## Table of Contents

- [Getting Started](#getting-started)
- [Prerequisites](#prerequisites)
- [Building the Docker Image](#building-the-docker-image)
- [Running the Docker Container](#running-the-docker-container)
- [Accessing the Webapp](#accessing-the-webapp)
- [Usage](#usage)
- [Contributing](#contributing)
- [License](#license)

## Getting Started

These instructions will help you set up and run the NetLog Viewer webapp using Docker.

### Prerequisites

- Docker installed on your machine. You can download Docker from [here](https://www.docker.com/products/docker-desktop).

### Building the Docker Image

1. Clone this repository:

   ```bash
   git clone https://github.com/your-username/netlogviewer-docker.git
   cd netlogviewer-docker
   ```

2. Build the Docker image:

   ```bash
   docker build -t netlogviewer .
   ```

### Running the Docker Container

Run the Docker container using the following command:

```bash
docker run -d -p 8080:8080 netlogviewer
```

This will start the container in detached mode and map port 8080 of the container to port 8080 on your host machine.

### Accessing the Webapp

Open your web browser and navigate to:

`http://localhost:8080/index.html`

You should see the NetLog Viewer webapp interface.

## Usage

1. Export a NetLog dump from Chrome by navigating to `chrome://net-export`.
2. Click on "Choose File" in the webapp interface and select your exported NetLog dump file.
3. Analyze your NetLog data using the available tabs (Import, Events, Proxy, Timeline, DNS, Sockets, Cache).

## Contributing

Contributions are welcome! Please open an issue or submit a pull request with your changes.

### Steps to Contribute

1. Fork the repository
2. Create a new branch (`git checkout -b feature-branch`)
3. Make your changes
4. Commit your changes (`git commit -am 'Add new feature'`)
5. Push to the branch (`git push origin feature-branch`)
6. Open a Pull Request

## License

This project is licensed under the MIT License - see the [https://www.mit.edu/~amini/LICENSE.md](LICENSE) file for details.
