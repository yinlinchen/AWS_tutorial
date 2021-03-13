# Basic AWS CLI usage

## EC2
* Start instance
    ```
    aws ec2 start-instances --instance-ids instanceId
    ```
* Stop instance
    ```
    aws ec2 stop-instances --instance-ids instanceId
    ```
* Check instance status
    ```
    aws ec2 describe-instances --instance-ids i-04941ac1e3a4f967f --filters Name=instance-state-name,Values=stopped,running --query "Reservations[*].Instances[*].[InstanceId, State.Name, PublicDnsName]" --output table
    ```
* Connect to the instance
    ```
    ssh -i "xxxx.pem" ec2-user@yyyyyy.compute-1.amazonaws.com
    ```


## Documentation
* [AWS CLI](https://aws.amazon.com/cli/)