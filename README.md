# Setup

- `npm i`

# Dev operations

- `npm run dev`
- `npm run build`
- `npm run preview`

# Containerization and test

- Make `.env.test`
  ```
  NGINX_PORT=5173
  NGINX_PROXY=http://pf-backend:3000
  ```
- `docker compose --env-file ./.env.test up -d --force-recreate --build`

# Push to dockerhub

- `docker tag preflight-frontend [DOCKERHUB_ACCOUNT]/preflight-frontend:latest`
- `docker push [DOCKERHUB_ACCOUNT]/preflight-frontend:latest`
