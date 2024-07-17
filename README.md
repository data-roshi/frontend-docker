# Getting Started

### Local Docker Build

```bash
docker build -f Dockerfile.dev .
```


### Docker Run 

```bash
docker run -p 3000:3000 <image-id>
```

### Docker Volume Without Compose
Directly pick up file changes on react files, by using current working dir as volume,
but excluding (bookmarking) node_modules
```bash
docker run -p 3000:3000 -v /app/node_modules -v ${pwd}:/app  <image-id>
```

### Docker Run Tests

```bash
docker run -it <image-id> npm run test
```

```bash
docker exec -it <container-id> npm run test 
```
