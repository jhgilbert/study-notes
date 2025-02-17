# Implementing microservices in AWS

## Deployment options

### EC2

Contrary to popular belief, you can run a microservice on EC2. Each service can run on its own EC2 instance behind an Elastic Load Balancer or Amazon API Gateway.

An Autoscaling Group can be used to create or terminate instances in order to meet demand.

### Lambda (serverless)

Each microservice can be a function. Lambda functions scale automatically, so no ASG is necessary.

### Containers

You can use EKS (Elastic Kubernetes Service) or ECS (Elastic Container Service), and use either one behind an Elastic Load Balancer or Amazon API Gateway. Each service would run in its its own container.

#### Example Kubernetes architecture

Behind Ingress ALB (Application Load Balancer), each endpoint can be its own service, each of which runs in a container inside a pod.

### Mix and match

There's no reason that each service has to be run on the same host. One service can be on Kubernetes while another is on EC2, with everything behind an ALB.
