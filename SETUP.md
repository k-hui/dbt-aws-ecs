### Install libraries

```bash
pip install fastapi
pip install "uvicorn[standard]"
pip install pydantic
pip install SQLAlchemy
pip install dbt-core
pip install dbt-postgres
pip freeze > requirements.txt
```

```bash
copilot init

copilot deploy
copilot deploy --app dbt

copilot app ls
copilot app delete

copilot env ls
copilot env show --resources

copilot svc show
copilot svc logs
copilot svc logs --env dev --since 5m | grep -v INFO
copilot svc status
```