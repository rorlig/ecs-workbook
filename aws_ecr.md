#### Amazon ECR
+ Private repo

#### get-login
```code
aws ecr get-login
```

+ then use the output docker login .. to login to registry ...


+ create a new repository

``` code
aws ecr create-repository
```

+ describe all repository
``` code
aws ecr list-repositories
```

+ list all images
``` code
aws ecr list-images --repository-name deepdive/nginx
```

### pull and image - get the nginx from the the amazon service
```code
docker pull nginx:1.9
```

### tag it
``` code
docker tag nginx:1.9 <<repository name>>
```

+ push it to ecr
``` code
docker push <<repository-url>>
```
