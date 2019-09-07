AWS Lambda is the Ultimate Abstraction Layer.

- Data Centers.
- Hardware
- Assembly Code/ Protocols
- High level languages
  - Operating Systems
  - Application Layer/ AWS APIs
  - AWS Lambda

Building a serverless webpage.

User - Route53 - User - Web page (Index.html) - User (Dynamic Content) - API Gateway - Lambda Function

Step 1. Hit `Create a Function`.
Step 2. Choose `python 3.7` for the runtime and create a new role name.
Step 3. Choose `Simple microservice permissions` as a policy on the `role`.
Step 4. Create the Function.
Step 5. Import the course files.
Step 6. Add the course files.
Step 7. Add a api gateway into the lambda function.
Step 8. Choose AWS IAM as security group.
Step 9. You will be missing a api gateway token so go to api gateway api on your first lambda function.
Step 10. Make a new `GET` request and click Lambda Function Integration and Proxy Integration and Choose the correct lambda function in the AWS Lambda.
Step 11. After creating your get request go ahead and redeploy your endpoint.
Step 12. Add a New S3 Bucket!
Step 13. Make it public and enable static website hosting!
Step 14. Add you index.html and error.html
