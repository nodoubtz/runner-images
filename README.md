# Nodoubtz runner-images

This repository contains images and scripts for setting up self-hosted runners, typically used for CI/CD pipelines (such as GitHub Actions). The `Runner` branch focuses on providing all necessary files, configurations, and instructions to build, manage, and maintain runner environments.

## Table of Contents

- [Overview](#overview)
- [Features](#features)
- [Getting Started](#getting-started)
- [Usage](#usage)
- [Configuration](#configuration)
- [Management](#management)
- [Security](#security)
- [Contributing](#contributing)
- [License](#license)

## Overview

The goal of this project is to provide ready-to-use images and scripts for deploying self-hosted runners efficiently and securely, with an emphasis on:
- Error-free setup
- Easy configuration and management
- Secure handling of sensitive data
- Minimizing duplicate code and vulnerabilities

## Features

- Pre-configured runner images for popular environments (Linux, Windows, etc.)
- Automation scripts for fast setup and configuration
- Management tools for updating and monitoring runners
- Built-in security best practices
- Deduplication logic to avoid redundant code

## Getting Started

### Prerequisites

- Docker (for building images)
- Access to the repository
- Basic understanding of CI/CD pipelines

### Quick Start

1. **Clone the repository**
   ```sh
   git clone --branch Runner https://github.com/nodoubtz/runner-images.git
   cd runner-images
   ```

2. **Build the image**
   ```sh
   docker build -t my-runner-image .
   ```

3. **Run the runner**
   ```sh
   docker run -e RUNNER_TOKEN=<your_token> my-runner-image
   ```

## Usage

- **Register a new runner:**  
  Follow the scripts or documentation in the repo to register your runner with your CI/CD platform.
- **Update an existing runner:**  
  Use the management scripts in `/scripts` to update or restart runners safely.

## Configuration

- Configuration files can be found in the `config/` directory.
- Environment variables are supported for flexible setup.
- Refer to `config/README.md` for detailed configuration options.

## Management

- Use the tools in `/scripts` for starting, stopping, and monitoring runners.
- Logs and diagnostic tools are included for troubleshooting.

## Security

- Sensitive data (tokens, secrets) should be provided via environment variables and never hardcoded.
- The images and scripts are regularly reviewed for vulnerabilities.
- Vulnerable code is hidden or removed, and best practices are followed to minimize risk.

## Contributing

Contributions are welcome! Please submit pull requests with clear descriptions and follow the repository's code guidelines.

## License

This project is licensed under the MIT License.

---

**Note:**  
If you encounter duplicate code or the deduplication logic doesn't work properly, please file an issue or submit a pull request with your fix.
