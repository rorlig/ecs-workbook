### Run task
#### - it will get distributed on the cluster randomly anywhere on the cluster
aws ecs run-task --cluster deepdive --task-definition web --count 1

#### List tasks
aws ecs list-tasks --cluster deepdive

#### stop tasks
aws ecs stop-tasks --cluster deepdive --task <task-arn>


#### list containers

aws ecs list-container-instances --cluster deepdive
#### start tasks

aws ecs start-task --cluster deepdive --task-definition web --container-instances arn:aws:ecs:us-east-1:909603365907:container-instance/c0bbfa31-2570-49ff-a84c-33ab3dfec2c3

### stop-task 
