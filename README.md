# ta-dev-env


Check this out into directory containting

  1. travel-alerts-messaging-api
  2. travel-alerts-internal-tool
  3. travel-alerts-subscribe-app

Then go there:

    cd ta-dev-env 
    
and do something:

    docker compose up


Go over to travel-alerts-messaging-api/bin and run:

    ./create_lambda.sh

You'll see console output for queue creation (of not if fails)

Check localstack
If you have [awslocal](https://docs.localstack.cloud/user-guide/integrations/aws-cli/#localstack-aws-cli-awslocal) installed you run this:

     awslocal sqs list-queues

You should see something like this:
```
{
    "QueueUrls": [
      "http://sqs.eu-west-2.localstack:4566/000000000000/outbound-messages-dlq",
      "http://sqs.eu-west-2.localstack:4566/000000000000/outbound-messages",
      "http://sqs.eu-west-2.localstack:4566/000000000000/outbound-batching-dlq",
      "http://sqs.eu-west-2.localstack:4566/000000000000/outbound-batching"
    ]
}
```
    