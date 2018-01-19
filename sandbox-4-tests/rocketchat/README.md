
```
docker run --name db -d mongo:3.2 mongod --smallfiles
docker run --name rocketchat -p 80:3000 --env ROOT_URL=http://localhost --link db:db -d rocket.chat
```
