# docker dev stack

Tested on windows with WSL

Start postgres & pgadmin with

```cmd
cd postgres && docker-compose up -d
```

## Add GraphQL

Add your database name to the command and run for graphql at 'localhost:5000/graphiql' and 'localhost:5000/graphql'

```cmd
docker run --name pgql -p 5000:5000 --network=postgres_postgres -d graphile/postgraphile --connection postgres://postgres:changeme@172.18.0.2:5432/$db_name --schema public --watch
```
