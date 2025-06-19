## Manual installation
 - Install nodejs locally ()
 - Clone the repo
 - Install dependencies (npm install)
 - Start the DB locally
    - docker run -e POSTGRES_PASSWORD=mysecretpassword -d -p 5432:5432 postgres
    - Go to neon.tech and get yourself a new DB
 - Change the .env file and update your DB credentials
 - npx prisma migrate
 - npx prisma generate
 - npm run build
 - npm run start

 ## Docker installation
 - Install docker
 - Create a network - docker network create user_project
 - Start postgres
    -  docker run --network user_project --name postgres -e POSTGRES_PASSWORD=mysecretpassword -d -p 5432:5432 postgres
 - Build the image - `docker build --network=host -t user-project .`
 - Start the image - `docker run -e DATABASE_URL=postgresql://neondb_owner:npg_Gcw1XJ9KUWDE@ep-bitter-fog-a8kl4ox2-pooler.eastus2.azure.neon.tech/neondb?sslmode=require`

 ## Docker Compose installation steps
 - Install docker, docker-compose
 - Run `docker-compose up`