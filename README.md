# FastAPI Calculator - IS601 Module 8

## Project Overview

This assignment is a web-based calculator built using Python and FastAPI for IS601 Module 8.

The application supports addition, subtraction, multiplication, and division through a browser interface and REST API.

The project demonstrates automated testing, logging, Docker containerization, and CI/CD using GitHub Actions.

## Technologies Used

- Python 3.12
- FastAPI
- pytest
- Playwright
- Docker and Docker Compose
- GitHub Actions
- Trivy Security Scanner
- Docker Hub

## Features

- Addition, subtraction, multiplication, and division
- Support for negative numbers and decimals
- Input validation and division-by-zero handling
- Logging of calculations and errors
- Automated unit, integration, and end-to-end tests
- Docker deployment and GitHub Actions CI/CD

## Running the Application

Clone the repository:

```bash
git clone https://github.com/fzheng04/assignment8.git
cd assignment8
```

Build and start the application with Docker:

```bash
docker compose up -d --build
```

Open the calculator at:

http://localhost:8000

View application logs:

```bash
docker compose logs -f web
```

Stop the application:

```bash
docker compose down
```

## Automated Testing

The project includes 74 automated test cases across three categories.

**Unit Tests:** Verify individual arithmetic functions, including negative numbers, decimals, and division by zero.

**Integration Tests:** Verify FastAPI endpoints, HTTP responses, input validation, and logging.

**End-to-End Tests:** Use Playwright to simulate browser interactions, including entering numbers, clicking buttons, and verifying results.

Run the tests after installing the dependencies:

```bash
pip install -r requirements.txt
python -m playwright install chromium

pytest tests/unit/
pytest tests/integration/
pytest tests/e2e/
```

Note: End-to-end tests start their own FastAPI server, so port 8000 should be available.

## GitHub Actions CI/CD

GitHub Actions automatically runs the following jobs:

1. **Test:** Runs unit, integration, and Playwright tests.
2. **Security:** Scans the Docker image using Trivy.
3. **Deploy:** Builds and pushes the Docker image to Docker Hub.

The workflow runs automatically on pushes to the main branch.

## Repository Links

**GitHub:** https://github.com/fzheng04/assignment8

**GitHub Actions:** https://github.com/fzheng04/assignment8/actions

**Docker Hub:** https://hub.docker.com/r/fzheng04/assignment8

## Acknowledgments

Based on the IS601 Module 8 FastAPI Calculator starter project:

https://github.com/kaw393939/module8_is601

Enhanced with additional testing, logging, and CI/CD improvements.

## Author

Feiyang Zheng

IS601 - Module 8