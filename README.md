# About

Jenkins CodeBuild & CodeDeploy integration.

# Procedure

* Allow EC2 instance to access S3 bucket using IAM role. Assuming that your codepipeline config `appspec.yml` and dependencies are stored in S3 bucket.
* Make sure that EC2 instance have CodeDeploy agent installed. Install the agent during instance bootstrapping.
* Create another IAM role for CodeDeploy with `AWSCodeDeployRole` policy attached. Use this role in CodeDeploy configuration.
