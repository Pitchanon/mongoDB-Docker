# mongoDB-Docker
MongoDB in a Docker container with Authentication

```
$ docker run -it --rm \
-e MONGODB_ADMIN_USER=admin \
-e MONGODB_ADMIN_PASS=adminpass \
-e MONGODB_APPLICATION_DATABASE=mytestdatabase \
-e MONGODB_APPLICATION_USER=testuser \
-e MONGODB_APPLICATION_PASS=testpass \
-v $PWD/mongoData:/data/db \
-p 27017:27017 --name mongodb_auth pitchanon/mongodb-docker
```

Run container in background
```
$ docker run -it -d \
-e MONGODB_ADMIN_USER=admin \
-e MONGODB_ADMIN_PASS=adminpass \
-e MONGODB_APPLICATION_DATABASE=mytestdatabase \
-e MONGODB_APPLICATION_USER=testuser \
-e MONGODB_APPLICATION_PASS=testpass \
-v $PWD/mongoData:/data/db \
-p 27017:27017 --name mongodb_auth pitchanon/mongodb-docker
```

___

Thank you: [Alex's Blog](http://blog.bejanalex.com/2017/03/running-mongodb-in-a-docker-container-with-authentication/) 
