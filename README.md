Deploying the Swiggy clone app with Terraform, Kubernetes, and Jenkins CICD.
Test100
This Proof of concepts is given as a minor assignment in-order to gain understanding of AWS
resources and services and their real time requirement. This Proof of Concept is given to me
as an architecture. For the given architecture, the main goals is to develop infrastructure using
terraform.
Components:
Main components of this proof of concept include:
 EC2 instance: There are two EC2 instances here, one which has VerneMQ
and other which has Grafana for monitoring
 API Gateway: API Gateway is used to create an API is used to expose data from
PostgreSQL
 Lambda Function: used to store data into PostgreSQL table and are triggered each
minute and each hour to do data analysis and then store the data in the table.
 PostgreSQL: stores the data coming from the iot devices and also the data that has
the analysis done is also stored in this PostgreSQL table.
 IAM Roles: IAM roles and permissions are given to lambda functions and
permissions for users to access the monitored data through Grafana instance.
 S3 Bucket: for storing items like for the websites UI, the required files are stored in
here.
 Terraform
Architecture:
This proof of concept has two instances, one for VerneMQ and the other for Grafana for
monitoring, two lambda functions for posting, deleting or updating data, to PostgreSQL, an
API Gateway, S3 bucket, IAM roles, and PostgreSQL.





