# My Python Application

## Repository Structure

```bash
.
├── app.py               # Main application file
├── requirements.txt     # Python dependencies
├── test_app.py          # Unit tests for the application
├── Dockerfile           # Dockerfile to containerize the application
└── .github
    └── workflows
        └── ci.yml       # GitHub Actions CI pipeline configuration
```

## Instructions to Build and Run the Application

### Prerequisites
- Python 3.x installed
- Docker installed

### Build and Run Locally

1. Clone the repository:
   ```bash
   git clone https://github.com/yogurt98/PROG8860-midterm.git
   cd PROG8860-midterm
   ```

2. Install dependencies:
   ```bash
   python -m venv venv
   source venv/bin/activate  # On Windows, use `venv\Scripts\activate`
   pip install -r requirements.txt
   ```

3. Run the application:
   ```bash
   python app.py
   ```

### Build and Run with Docker

1. Build the Docker image:
   ```bash
   docker build -t jingxulan/my_repo:latest .
   ```

2. Run the Docker container:
   ```bash
   docker run --name container_name jingxulan/my_repo:latest
   ```

## Steps to Test the CI Pipeline

1. GitHub Actions will automatically run the CI pipeline when you push changes to the repository.
2. The CI pipeline:
   - Installs dependencies.
   - Runs the unit tests (`test_app.py`) using `pytest`.
3. You can view the status of your pipeline under the "Actions" tab of your GitHub repository.

### Running Tests Locally

To run the tests locally:
```bash
source venv/bin/activate  # If not activated already
pytest
```

## Instructions to Pull the Docker Image from the Registry

1. Ensure you have Docker installed and are logged into Docker Hub:
   ```bash
   docker login
   ```

2. Pull the Docker image from Docker Hub:
   ```bash
   docker pull jingxulan/my_repo:latest
   ```

3. Run the pulled image:
   ```bash
   docker run --name container_name jingxulan/my_repo:latest
   ```
