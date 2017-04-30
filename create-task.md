### Run task
#### - it will get distributed on the cluster randomly anywhere on the cluster
```code
aws ecs run-task --cluster deepdive --task-definition web --count 1
```
#### List tasks
```code
aws ecs list-tasks --cluster deepdive
```
#### stop tasks
```code
aws ecs stop-task --cluster deepdive --task <<task-arn>>>
```

#### list containers
```code
aws ecs list-container-instances --cluster deepdive
```
#### start tasks
```code
aws ecs start-task --cluster deepdive --task-definition web --container-instances <<instance-arn>>
```
### stop-task
