## 📝 Prerequisites
  - Have an active AWS account
  - Existing Lambda Function


## 🛠 Set up


### 1. Navigate to API Gateway on AWS
![image](https://github.com/tunabearfish/AWS-EC2/assets/65553627/f038cf3e-3165-428f-b46f-24090cce7c9f)


### 2. Choose an API Type
![image](https://github.com/tunabearfish/AWS-EC2/assets/65553627/8675d9a8-22f4-4b2e-a9bf-18cc25a755fc)

For this example: we will build a REST API

### 3. Create a New API
![image](https://github.com/tunabearfish/AWS-API-Gateway/assets/65553627/c64d3fe9-02ff-48c4-80d9-7eef59895e45)


  Give your API a name and description
  Choose Endpoint Type. For public access, Select "Regional" for private access within your VPC, choose "Private"
  Click Create API 

  For this example: I will call my API -"MyFirstAPI" and I will choose Endpoint Type "Regional"

### 4. Create Methods  
![image](https://github.com/tunabearfish/AWS-API-Gateway/assets/65553627/317bb4d0-26ab-4773-a8c9-66945e42fa56)


In the API Gateway console, you'll see a tree-like structure. Create resources that represent the URL paths of your API.
For each resource, create HTTP methods (GET, POST, PUT, DELETE, etc.) to define what actions are allowed on that resource

Click on Actions and for this example we will use GET


### 6. Define Integration
![image](https://github.com/tunabearfish/AWS-API-Gateway/assets/65553627/6182450c-9453-4f8d-9684-b6c46b993856)
For each method, configure the integration with your backend service. This can be Lambda functions, EC2 instances, or other AWS services.

For this example: My integration type is " Lambda Function" I will be using Lambda Proxy Integration, My Region is "us-east-1" and I have made a Lambda Function " lambda-api-gateway-proxy-root-get" and I will be using the default Timeout(29 seconds)

Then hit save



### 7. Ensure your Lambda Permissions are correct
Go to your Lambda Function and select Permissions and scroll down then you can see if you have the apigateway.amazonaws.com principal
![image](https://github.com/tunabearfish/AWS-API-Gateway/assets/65553627/3c9c45b4-2990-42be-943f-fc91e432508e)

### 8. Test your API
In your API you can click on TEST to test your API out
![image](https://github.com/tunabearfish/AWS-API-Gateway/assets/65553627/3ab34e56-0eb7-4125-b5af-f1688fea52de)

You will see your Response Body, Response Header along with logs
![image](https://github.com/tunabearfish/AWS-API-Gateway/assets/65553627/1e7b979b-edfc-4a67-8aa9-ce38158db9c0)



### 9. 



### 10



### 11. Deploy your API
![image](https://github.com/tunabearfish/AWS-API-Gateway/assets/65553627/67df6e2b-508b-466d-b7a6-519681226401)

Click on Actions

Deploy API

Select Deploy API

Choose a stage
![image](https://github.com/tunabearfish/AWS-API-Gateway/assets/65553627/72d715fe-a0f2-4049-9311-4f0d9ad6119c)


For this example: I chose dev as my stage

Congrats you just deployed your first REST API on API Gateway 




## 🚫 Troubleshooting

Encountered an issue? Consult the Troubleshooting Guide in this repository for guidance.

