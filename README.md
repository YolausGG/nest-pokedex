<p align="center">
  <a href="http://nestjs.com/" target="blank"><img src="https://nestjs.com/img/logo-small.svg" width="120" alt="Nest Logo" /></a>
</p>


# Run in development

1. Clone repository
2. Run

```
npm install
```
---
3. Have Nest CLI installed

```
npm i -g @nestjs/cli
```
---
4. build the database
```
docker-compose up -d
```
---
5. Clone the __.env.template__ file and rename the copy to __.env__ file
---
6. Fill in the environment variables defined in the __.env__ file
---
7. Run the application in developer mode:
```
npm start:dev
```
---
8. Rebuild the database from the seed
```
http://localhost:3000/api/v2/seed
```



## Stack used
* MongoDB
* Nest


# Production Build 
1. Create the ```.env.prod``` file
2. Fill the environment for prod
3. Create the new image
```
docker-compose -f docker-compose.prod.yaml --env-file .env.prod up --build
```


# Notes
Heroku redeploy no changes:
```
gti commit --allow-empty -m "Tigger Heroku deploy"
git push heroku <master|main>
```

