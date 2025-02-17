# Load balancers: ALB, NLB

Without a load balancer, the user would have to access your application through a given instance's IP address. But what if the application scales, or one instance goes down? How will additional instances be discovered?

**Elastic Load Balancing** automatically distributes traffic across multiple instances (or pods, or lambda functions), tracking the health of all instances and only sending traffic to healthy instances. The ELB has a URL like yoursite.com, and forwards traffic from there, automatically discovering any new instances. It can also integrate with SSL, and is highly available, running in multiple availability zones.

## Exposing ELB via an existing website

ELB has its own DNS. But if your application should be accessed through a URL you already own, like mysite.com, you can use Amazon's Route 53 to set up an A record (alias record) and forward traffic for mysite.com to your ELB's DNS.

## Load balancer types

### ALB (Application Load Balancer) - OSI Layer 7

If you want to use a different backend for different URLs, like users/get vs users/post, you can use an ALB to use the path to forward traffic to different target groups of hosts (such as EC2s).

The backend of these target groups doesn't need to be the same, if one endpoint needs to be supported by EC2 and another needs to be supported by a Kubernetes pod.

ALBs can validate and terminate SSL.

### NLB (Network Load Balancer) - OSI Layer 4

The NLB routes traffic based on the protocol (such as TCP) and the port of the incoming traffic.

It can't distribute traffic to different backends.

Its default behavior is SSL passthrough: it won't validate SSL certificates. But it's possible to configure the NLB to terminate SSL certs.

### Which to use?

NLB handles spiky traffic better, and exposes a static IP address. NLB supports fewer backend target group types than ALB. It supports EC2 instances and IP addresses as backend target groups, not Lambda.

ALB can expose a static IP address, but it requires Global Accelerator. ALB supports EC2, IP address, and Lambda.
