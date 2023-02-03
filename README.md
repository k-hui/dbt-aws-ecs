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

if no brew

- https://brew.sh/

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

### Local development

```bash
uvicorn main:app --host 0.0.0.0 --port 8080
```

### Useful commands

```bash
docker rmi $(docker images | grep 'dbt')
docker rmi $(docker images | grep '<none>')
```

## Deployment

### Prepare environment

```bash
cp exmaple.env api.env
# type your database connection
```

```bash
copilot init
```

- follow the instructions

```bash
# create your environment
copilot env init
# deploy your environment.
copilot env deploy --name dev
# deploy your service
copilot deploy
# delete app
copilot app delete
```
