## Miscellaneous notes and references for CI/CD

 [Course at LinkedIn](https://www.linkedin.com/learning/build-a-ci-cd-pipeline/)

 ```
 - what kind of problems are we trying to solve
 - write easily to maintain code
 ```

 - never use tabs in YAM:
 - 2 spaces, then -, then  1 space
 - use | for formatted text, but > for not-formatted human readable text

 ### Github actions:
 [Quickstart for GitHub Actions - GitHub Docs](https://docs.github.com/en/actions/writing-workflows/quickstart)

 ### DORA
 - DORA - metrics for ci/cd testing
 - https://cloud.google.com/blog/products/devops-sre/using-the-four-keys-to-measure-your-devops-performance
 - use lint in the pipelibe so that code is checked throughout
 - Quality checking, CodeL from GitHub
 - [CodeQL](https://codeql.github.com/)
 - [DORA](https://cloud.google.com/blog/products/devops-sre/using-the-four-keys-to-measure-your-devops-performance)
 - [DORA | DORA’s software delivery metrics: the four keys](https://dora.dev/guides/dora-metrics-four-keys/)

 ### YAML
 [YAML Glossary](https://yaml.com/doc/glossary/)

### ELASTIC BEANSTALK
made by AWS, for deploying applications, maybe as a alternative to EC2

### Various comments
- watch out for manual deployments in which one person has access to a specific machine, rather than being about a widely accessible standard deployment model that more than one person can check and trigger or troubleshoot
- also, learning...do not do deployments or manual deployments on Friday afternoons
- Good to have high deployment frequency, a good metric reveals confidence in the deployment process and also plans and methods for those deployments.
- question to ask: what is your app availability? How close to 100% is it?

### Deployment strategies
- there is a place to turn off the current working deplopyment and turn on the new one or the dev change
- there is also rolling deployments, turning on a new instancce and turning off the old ones
-- the app then needs to be able to work with older and newer instances at the same time
- Canary deployments, where a small percentage of users are directed to the new deployment, allowing for testing before general deployment
- A/B deployments, adding feature flags to the app to allow for testing of new features before general deployment
- Shadow deployments (dark deployments), where the new deployment is tested in the background, without affecting the current deployment
- Blue-green deployments, where the new deployment is tested in a separate environment, then switched to the main environment when ready (like a classic staging ENV)
__ think about all these options for deployment strategies

### Selecting the correct strategy
- [Six Strategies or Application development](https://thenewstack.io/deployment-strategies/)
- blue/green deployments are good for high availability
- but they cost more because there are more machines running than there would be in production
- There also needs to be an Approval process
- There has to be a rollback plan in all the deployment strategies

### Terraform
- also, Pulumi is an option
- Terraform is a tool for building, changing, and versioning infrastructure safely and efficiently
- define infrastructure as code
- Terraform can manage existing and popular service providers as well as custom in-house solutions
- Terraform can manage the front end and the back end
- The region is the location of the data center
- The Terraform state will have to be stored someplace, often in an S3 bucket
- We will use an AMI to create an EC2 instance that tells Terraform what type and flavor the VM will be
- Terraform will create a security group, which is a firewall rule
-
