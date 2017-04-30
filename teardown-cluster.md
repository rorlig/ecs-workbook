
+ Terminate the instances
```code
aws ec2 terminate-instances --instance-ids <<instance_id>>
```

+ Remove the s3 config files
```code
aws s3 rm <<bucket_name>> --recursive
```

+ Buckets
```code
aws s3api delete-bucket --bucket <<bucket_name>>
```

+ Delete repository
```code
aws ecr delete-repository --repository-name deepdive/nginx --force
```

+ Tear down cluster 
```code
aws ecs delete-cluster --cluster deepdive
```
