# Kong Gateway without database

A docker compose of Kong Gateway db-less and basic configuration. This can be useful since we don't have to manage the database. 

## Download

```bash
npx degit https://github.com/seanghay/kong-gateway-db-less.git
```

## Running

Start

```bash
docker-compose up
```

Stop

```bash
docker-compose down
```

## Testing

```bash
curl http://localhost:8000/placeholder/users/1
```