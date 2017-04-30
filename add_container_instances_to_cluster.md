aws ec2 run-instances --image-id ami-275ffe31 --count 1 \
--instance-type t2.micro --iam-instance-profile Name=ecsInstanceRole \
--key-name gg-test-2 --security-group-ids sg-e9a65597  \
--user-data file://copy-ecs-config-to-s3
