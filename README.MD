## We need to setup OIDC first and it's a one time setup

[OIDC SETUP LINK ](https://github.com/harshatejaadduri/OIDC.git)

# Create two Docker Images and push it to Docker Hub
# Create manifestfile and kinds of Deployment, Service and Ingress
# Examples for Deployment, Service and Ingress links

[Deployment](https://kubernetes.io/docs/concepts/workloads/controllers/deployment/)
[Deployment example](https://github.com/harshatejaadduri/k8-resources/blob/main/16-deployment.yaml)

[Service](https://kubernetes.io/docs/concepts/services-networking/service/)
[Service example](https://github.com/harshatejaadduri/k8-resources/blob/main/12-service.yaml)

[Ingress](https://kubernetes.io/docs/concepts/services-networking/ingress/)
[Annotations for Ingress Controller](https://geoffcline.github.io/aws-load-balancer-controller/guide/ingress/annotations/)

Here we used annotions like
```
 alb.ingress.kubernetes.io/listen-ports:  '[{"HTTP": 80}]' or  '[{"HTTPS": 443}]'
alb.ingress.kubernetes.io/group.name: # any name this creates only one dns for all target groups
alb.ingress.kubernetes.io/certificate-arn:  # give your certificate arn no after creating in AWS ACM
alb.ingress.kubernetes.io/scheme: internet-facing
alb.ingress.kubernetes.io/target-type: ip

```