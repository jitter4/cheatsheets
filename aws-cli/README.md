aws logs get-log-events --log-group-name <log_group_name> --log-stream-name <log_stream_name>
# aws logs get-log-events --log-group-name my-logs --log-stream-name 20150601


## igw
### attach igw to vpc
aws ec2 attach-internet-gateway --vpc-id "vpc-042d9b8e247f10a5c" --internet-gateway-id "igw-08ba74070f240169f" --region ap-south-1