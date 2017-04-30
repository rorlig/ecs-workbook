### Services
These are long running tasks --
#### Build service based on the web task definition
```code
aws ecs create-service --cluster deepdive --service-name web --task-definition web --desired-count 1
```

#### Show all registered - service
```code
aws ecs list-services --cluster deepdive
```

#### get the aws instances


#### Increase size
```code
aws ecs update-service --cluster deepdive --service web \
--task-definition web --desired-count 2
```

#### Decrease size
```code
aws ecs update-service --cluster deepdive --service web \
--task-definition web --desired-count 0
```
