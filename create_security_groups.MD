#### Create the Security group
+ Create the key
```code
aws ec2 create-security-group --group-name gg_SG_useast1 --description "Security Group for gg-test on us-east1"
```
+ Check the key
``` code
aws ec2 describe-security-groups --group-id sg-e9a65597
```
+ Add Securiy Groups

``` code
aws ec2 authorize-security-group-ingress --group-id sg-e9a65597 --protocol tcp --port 22 --cidr 0.0.0.0/0

```
+ Add the ingress & egress groups.
``` code
aws ec2 authorize-security-group-ingress --group-id sg-e9a65597 --protocol tcp --port 80 --cidr 0.0.0.0/0
```
aws ec2 authorize-security-group-ingress --group-id sg-e9a65597 --protocol tcp --port 5432 --cidr 0.0.0.0/0 --source-group sg-e9a65597
aws ec2 authorize-security-group-ingress --group-id sg-e9a65597 --protocol tcp --port 6379 --cidr 0.0.0.0/0 --source-group sg-e9a65597
