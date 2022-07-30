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


## Configuration

Configuration file is in [`./declarative/kong.yml`](./declarative/kong.yml)


```yml
_format_version: "1.1"
_transform: true

services:
  - name: json_placeholder
    url: "https://jsonplaceholder.typicode.com/"
    routes:
      - name: placeholder_route
        paths:
          - /placeholder         
        strip_path: true
```