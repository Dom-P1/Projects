# Notes: IAM and Configuration

## IAM Roles and Policies
- Role: `CatProcessorLambdaRole`
  - Trust policy: Lambda service
  - Inline policy: Allow Rekognition, DynamoDB PutItem, S3 GetObject

## S3 Bucket
- Public access: Blocked
- Event trigger: Lambda function on `ObjectCreated`

## VPC Configuration
- Not used in this demo, but Lambda could be attached to VPC for tighter control.

## API Gateway (Optional)
- Method: POST
- Integration: Lambda Proxy
