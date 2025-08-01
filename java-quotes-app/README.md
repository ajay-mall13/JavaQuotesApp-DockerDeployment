# Java Motivational Quotes App

This project is a simple Java-based HTTP server that serves random motivational quotes via a REST API. The quotes are externalized to a `quotes.txt` file for easy customization.

## Features
- Serves random motivational quotes in JSON format.
- Uses an external `quotes.txt` file for configurable quotes.
- Lightweight HTTP server using `com.sun.net.httpserver.HttpServer`.
- Dockerized for easy deployment.

## Requirements
- Java 17+
- Maven (if building from source)
- Docker (optional, for containerized deployment)

## Setup and Usage

### Running Locally
1. Clone the repository:
   ```sh
   [git clone https://github.com/ajay-mall13/JavaQuotesApp-DockerDeployment.git
   cd java-quotes-app
   ```
2. Ensure `quotes.txt` exists in the project directory and contains quotes (one per line).
3. Compile and run the application:
   ```sh
   javac src/Main.java -d out
   java -cp out Main
   ```
4. The server will start on `http://localhost:8000/`.
5. Test the API using:
   ```sh
   curl http://localhost:8000/
   ```

### Running with Docker
1. Build the Docker image:
   ```sh
   docker build -t java-quotes:latest .
   ```

2. To check images
   ```sh
   docker images
   ```
3. Run the container:
   ```sh
   docker run -p 8000:8000 motivational-quotes-api
   ```
4. Access the API at `<public-ip>:8000/`.
![Screenshot (1019)](https://github.com/user-attachments/assets/f1c98af1-d632-4686-866d-389ca2489744)

## File Structure
```
project-root/
│── src/
│   └── Main.java
│── quotes.txt
│── Dockerfile
│── README.md
│── target/
│   └── myapp.jar (if using Maven build)
```

## Customizing Quotes
To customize the quotes, edit `quotes.txt` and restart the application. Each quote should be on a new line.

## License
This project is licensed under the MIT License.




