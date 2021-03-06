# RDS Aurora - Schedule Add / Delete Reader Node with Lambda Function and CloudWatch Event

## Attach the below policy to the Lambda function.

![GitHub Logo](https://github.com/mryutran/RDS-Aurora-Schedule-Add-Delete-Reader-Node/blob/main/Policy.png)

## Add Reader Node

### First step, create Lambda Function "Add-Node.py"

![GitHub Logo](https://github.com/mryutran/RDS-Aurora-Schedule-Add-Delete-Reader-Node/blob/main/Add-Node.png)

### Second step, add trigger with CloudWatch Event - Schedule expression: cron(17 7 * * ? *) 

This schedule will run lambda function at 7:17:00 GMT , (to VNT (GMT+7) at 14:17:00) to add reader node with instance identifier: My-RDS-Aurora-Lambda-Instance.


## Delete Reader Node

### First step, create Lambda Function "Delete-Node.py"

![GitHub Logo](https://github.com/mryutran/RDS-Aurora-Schedule-Add-Delete-Reader-Node/blob/main/Delete-Node.png)
    

### Second step, add trigger with CloudWatch Event - Schedule expression: cron(27 7 * * ? *) 

This schedule will run lambda function at 7:27:00 GMT , (to VNT (GMT+7) at 14:27:00) to delete reader node with instance identifier: My-RDS-Aurora-Lambda-Instance.
