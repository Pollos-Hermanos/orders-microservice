# Orders Microservice

## Dev

1. Clonar el repositorio
2. Instalar dependencias
3. Crear un archivo `.env` basado en el `.env.template`
4. Levantar la base de datos con `docker compose up -d`
5. Ejecutar migración de prisma `npx prisma migrate dev`
6. Levantar el servidor de nats
```
docker run -d --name nats-server -p 4222:4222 -p 8222:8222 nats 
```
7. Ejecutar `npm run start:dev`

# Prod

1. Clonar el repositorio
2. Crear el `.env` basado en el `.env.template`
3. Ejecutar el comando
```
docker compose -f docker-compose.prod.yml build
```