### Services
These are long running tasks -- 
#### Build service based on the web task definition
aws ecs create-service --cluster deepdive --service-name web --task-definition web --desired-count 1

#### Show all registered - service

aws ecs list-services --cluster deepdive

#### get the aws instances


#### Increase size
aws ecs update-service --cluster deepdive --service web \
--task-definition web --desired-count 2


#### Decrease size
aws ecs update-service --cluster deepdive --service web \
--task-definition web --desired-count 0
