# eShopOnContainers Fork
This project is a fork of the [eShopOnContainers .NET Microservices Sample Reference Application](https://github.com/dotnet-architecture/eShopOnContainers).

My goal was to use the reference app as a learning environment to try different cloud-native and DevOps concepts. I wanted to go beyond the basic Hello Worlds available for the different tools out-there. This project was the perfect starting point. Complex enough to show case some real-world use cases, but still simple enough to make it easy to master and deploy.

I documented each experiment in an article and kept and specific branch isolating the specific experiment. The main `dev` branch aims to integrate most of the experiments in a global reference app closer to a real-world enterprise scenario. The different experiment branches typically reflect the work done at the time of the experiment, so they may not all share the same base depending on when I did them.

## Banches and experiments

### Fully automated deployment
Goal: Consolidate in a single walkthrough all the steps needed to deploy the app to AKS with a fully automated CI/CD pipeline with GitHub Actions
Article: [Walkthrough of eShop setup on Azure Kubernetes Services with GitHub Actions](https://faun.pub/walkthrough-of-eshop-setup-on-azure-kubernetes-services-and-github-actions-7fa74d6496c3)
Branch: [experiment/aks-github-cicd)](https://github.com/oliviergaumond/eShopOnContainers/tree/experiment/aks-github-cicd)

### Image scanning
Goal: Add a step in the CI pipeline to automatically scan images for vulnerabilities and fail the build if vulnerabilities are found
Article: In-Progress
Branch (in-progress): [experiment/trivy-scan](https://github.com/oliviergaumond/eShopOnContainers/tree/experiment/trivy-scan)


## Roadmap
Here are some future concepts I would like to explore and implement on the eShopOnContainers reference app.
- Image signing and signature validation with an Admission Controller
- Implement PodSecurityPolicy (or an alternative) to enforce securit best practices in the containers
- Implement Network Policy to limit which pods can talk to each other
- Use a GitOps tool such as Flux or ArgoCD instead of deploying the images using GitHub Actions
- Configure observability with a tool such as Prometheus
- Configure auto-scaling of resources and test it by simulating ariable degree of traffic
- Use Azure KeyVault for secrets management
- Configure minimal RBAC access that would enable a dev team to deploy the eSHop app on a dedicated namespace on a Kubernetes cluster without full cluster admin access
- 

