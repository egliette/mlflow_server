# MLflow Server Setup

This directory contains a Docker-based MLflow tracking server setup with PostgreSQL backend and S3-compatible artifact storage.

## Quick Start

### 1. Setup Configuration

```bash
# Copy environment configuration
cp sample.env .env
# Edit .env file with your specific configuration values
```

### 2. Start Services

```bash
docker-compose up -d
```

This starts PostgreSQL database and MLflow tracking server.

### 3. Access MLflow UI

The MLflow tracking dashboard is accessible at:

```
http://localhost:5000
```

**Note**: If you want to access the dashboard from your local machine, you need to expose port 5000 in the docker-compose.yaml file.

## Services

- **PostgreSQL Database**: Backend store for MLflow metadata
- **MLflow Tracking Server**: Runs on port 5000 with experiment tracking and model registry

## Usage

```bash
docker-compose up -d
```

## Network Requirements

The setup requires an external Docker network called `nginx-network`. Create it if it doesn't exist:

```bash
docker network create nginx-network
```
