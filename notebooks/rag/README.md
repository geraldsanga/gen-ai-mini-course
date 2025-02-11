
### To run the pgvector docker container follow these steps below

```bash
# Start a docker container pgvector instance 
docker compose up
```

```bash
# Create a pg vector extension
docker exec -it postgres-pgvector psql -U postgres -c "CREATE EXTENSION vector"
```



