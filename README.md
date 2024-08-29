# Go Calculator

This is a simple calculator application written in Go. The program performs basic arithmetic operations like addition, subtraction, multiplication, and division.

## Features

- Perform basic arithmetic operations (+, -, *, /).
- Exit the program by typing `exit`.
- Dockerized for easy deployment.

## How to Run

### Running Locally

1. Clone the repository:
    ```sh
    git clone https://github.com/your-username/go-calculator.git
    cd go-calculator
    ```

2. Build and run:
    ```sh
    go build -o calculator
    ./calculator
    ```

### Running with Docker

You can use either a simple Dockerfile or a multistage Dockerfile.

#### Dockerfile (Without Multistage)

1. Build the Docker image:
    ```sh
    docker build -t go-calculator .
    ```

2. Run the Docker container:
    ```sh
    docker run -it go-calculator
    ```

#### Dockerfile (With Multistage & Distroless)

Multistage builds help create smaller, more secure Docker images by separating the build environment from the runtime environment.

1. Build the Docker image:
    ```sh
    docker build -t go-calculator-multi -f Dockerfile.multistage .
    ```

2. Run the Docker container:
    ```sh
    docker run -it go-calculator-multi
    ```

**Distroless** images are used in the final stage to minimize the image size and improve security by including only the necessary runtime dependencies without any OS package managers or shells.
