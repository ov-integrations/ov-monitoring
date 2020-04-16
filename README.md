# SqsIntegration

SQS integration is used to receive messages from Amazon Simple Queue Service (SQS). After receiving the message, integration removes it from the queue.

## Requirements
- Python 3
- Requests - [library for python](http://docs.python-requests.org/en/master/)
- boto3 - [Boto is the Amazon Web Services (AWS) SDK for Python](https://boto3.amazonaws.com/v1/documentation/api/latest/index.html)

## Usage
1. Install this integartion 
2. Create a new separate Queue
3. Send messages to the created Queue
4. Fill the settings file of the integartion
   - oneVizionUrl - OneVizion URL
   - oneVizionLogin - OneVizion Login
   - oneVizionPwd - OneVizion Password
   - trackorType - Tractor Type for adding received messages
   - awsAccessKeyId - AWS Access Key ID
   - awsSecretAccessKey - AWS Secret Access Key
   - awsRegion - AWS Region.
   - queueUrl - URL of created Queue
   - iterationMaxNum - Maximum number of attempts to receive messages from the Queue
   
5. Enable the integartion

Example of settings.json

```json
{
    "oneVizionUrl": "test.onevizion.com",
    "oneVizionLogin": "username",
    "oneVizionPwd": "*****",
    "trackorType" : "Trackor Type",

    "awsAccessKeyId": "*****",
    "awsSecretAccessKey": "*****",
    "awsRegion": "us-east-2",
    "queueUrl" : "https://sqs.us-east-2.amazonaws.com/788508682010/Test",

    "iterationMaxNum" : 100
}
```