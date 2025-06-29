# Project

“In this project, we followed a complete CI/CD pipeline integrated with DevOps best practices. Here's how the process works step by step:”

1. We begin by provisioning the required infrastructure using Terraform. This ensures our environment is version-controlled, and easily scalable.  (Infrastructure Provisioning)

2. Once the infrastructure is ready, the development team pushes the application code to a shared repository, ie; GitHub.   (Code Integration phase)

3. We then fetch the code and trigger a build process using a CI tool like Jenkins. During this stage, automated unit tests are executed to ensure code quality and functionality. (Build & Test Phase)

4. After the build, we integrate SonarQube to perform static code analysis and enforce quality gates. If the code passes all the quality checks, we move forward.  (Code Quality Analysis)

5. We then package the application into an artifact (like a .war or .jar file), which is stored securely in an S3 bucket for versioned storage and future deployments. (Artifact Creation & Storage)

6. So here comes the deployment phase,
   For deployment, we use a Tomcat server as the application server. The artifact is deployed to Tomcat automatically through pipeline configuration.

7. Finally, to ensure the health and performance of the application and infrastructure, we use Prometheus for monitoring and Grafana for visualizing metrics.  (Monitoring)
   This helps in proactive alerting and troubleshooting.

“This end-to-end workflow ensures a smooth and automated delivery process from code commit to deployment, with quality checks and monitoring integrated at every stage.”



















                   
