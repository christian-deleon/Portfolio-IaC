<div align="center">
  <a href="https://christiandeleon.me/">
    <img src="images/logo192.png" alt="Logo" height="80">
  </a>

   <h1 align="center">My Personal Portfolio Infrastructure</h1>
   <a href="https://github.com/othneildrew/Best-README-Template"><strong>Visit my Portfolio Website</strong></a>

</div>

## About this Project

With the idea of showing off my skills, I have created this repository to list all of the ways I have designed infrastructures that run my portfolio using different IaC and cloud resources.

The front end was designed and developed by me using React.Js, Javascript, HTML, and CSS.

Frontend Repository: https://github.com/christian-deleon/portfolio

## Infrastructures

### AWS CDK - Serverless Architecture ( The active infrastructure )

Repository: https://github.com/christian-deleon/portfolio-iac-aws-cdk

Using AWS CDK ( Cloud Development Kit ) with a serverless architecture I have created a very simple application that consists of the following AWS resources:

- `AWS S3` as the backend server
- `AWS CloudFront` as the CDN ( Content Delivery Network )
- `AWS Route 53` for the domain name services
- `AWS CodePipeline` for the CI/CD ( Continuous Integration and Continuous Delivery )
- `AWS CodeBuild` which takes changes from the respective GitHub repository and builds the React application
- `AWS CodeDeploy` to deploy the application to the AWS S3 bucket running as the application backend

### AWS CDK - Using ECS Fargate

Repository: https://github.com/christian-deleon/portfolio-iac-aws-cdk-ecs

Using AWS CDK ( Cloud Development Kit ) with AWS ECS Fargate running the web servers, I have created an application which uses `Docker` to containerize the `Node.Js` server and consists of the following AWS resources:

- `AWS ECS` ( Elastic Container Service ) as the container service for the web servers
- `AWS Route 53` for the domain name services and creates a hosted zone in each AWS region that has been specified
- `AWS Certificate Manager` which provides the SSL certificate for secure connection from the client to the load balancers
- `AWS ELB` ( Elastic Load Balancing ) which balance all HTTPS to the web servers
- `AWS ASG` ( Auto Scaling Groups ) which auto scales the Fargate web servers running on ECS based on CPU usage
- `AWS CodePipeline` for the CI/CD ( Continuous Integration and Continuous Delivery )
- `AWS CodeBuild` which takes changes from the respective GitHub repository and builds the React application image using Docker and updates or stores it in `AWS ECR`
- `AWS Lambda` that updates the AWS ECS cluster service with the updated Docker image from ECR
- `AWS EventBridge` which triggers the above Lambda function when a successful push has been made to the main region ECR repository

## Upcoming infrastructures

- Terraform - Serverless Architecture
- Terraform - Using ECS Fargate
