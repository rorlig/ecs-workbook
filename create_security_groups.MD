#### Create the Security group
+ Create the key
```code
aws ec2 create-security-group --group-name gg_SG_useast1 --description "Security Group for gg-test on us-east1"
```
+ Check the key
``` code
aws ec2 describe-security-groups --group-id <<security-group-id>
```
+ Add Securiy Groups

``` code
aws ec2 authorize-security-group-ingress --group-id <<security-group-id> --protocol tcp --port 22 --cidr 0.0.0.0/0

```
+ Add the ingress & egress groups.
``` code
aws ec2 authorize-security-group-ingress --group-id <<security-group-id> --protocol tcp --port 80 --cidr 0.0.0.0/0
```
```code
aws ec2 authorize-security-group-ingress --group-id <<security-group-id>> --protocol tcp --port 5432 --cidr 0.0.0.0/0 --source-group <<security-group-id>
```

```code
aws ec2 authorize-security-group-ingress --group-id <<security-group-id>> --protocol tcp --port 6379 --cidr 0.0.0.0/0 --source-group <<security-group-id>
```
