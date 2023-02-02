# dbt-aws-ecs

dbt on AWS ECS

## Requirements

- Python3
- Docker
- AWS Account

## Getting Started

### Setup AWS Account

### Install AWS Copilot CLI

- https://docs.aws.amazon.com/AmazonECS/latest/developerguide/getting-started-aws-copilot-cli.html

```bash
brew install aws/tap/copilot-cli
```

### Setup Python Environment

```bash
python3 -m venv venv
source venv/bin/activate
pip install -r requirements.txt
```

### Setup Local Database

```bash
docker-compose up -d
```

### Useful commands

```bash
docker rmi $(docker images | grep 'dbt')
docker rmi $(docker images | grep '<none>')
```