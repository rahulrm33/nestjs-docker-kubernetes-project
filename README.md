# nestjs-docker-kubernetes-project

> DON'T commit .env files into version control, add `.env` to `.gitignore`. `.env` files are added here as an example.

Develop the Nest application

```bash
npm install

npx prisma generate

npm run start:dev
```

## Docker File

#Get started by running
##Determine which env file should configured (dev,qas,prod) and set them to NODE_ENV in Dockerfile

```bash
docker build -t nest-api .

docker run -p 8001:8001 --env-file .env -d nest-api
```

## Docker Compose

```bash
docker-compose up
# or detached
docker-compose up -d
```
## Kubernetes 
```bash
cd k8s
kubectl apply -f ./

