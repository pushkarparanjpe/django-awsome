# django-awsome
Minimal django app, ready for deployment on AWS ElasticBeanstalk.  

### Pre-requisites
* Amazon account on AWS  

### Features
* Static assets  
* DB backend  
* django Admin  

### Quickstart

#### 1. Specify environment variables
* django details  
`DJANGO_SETTINGS_MODULE`  

* S3 Details  
`AWS_ACCESS_KEY_ID, AWS_SECRET_ACCESS_KEY, AWS_STORAGE_BUCKET_NAME`  

* Postgresql DB Details  
`DB_ENGINE, DB_HOST, DB_NAME, DB_PASSWORD, DB_PORT, DB_USER`  

* Admin details  
`SUPER_USER_EMAIL, SUPER_USER_NAME, SUPER_USER_PASSWORD`  

#### 2. Clone and deploy django-awsome to EBS


### AWS components
* ElasticBeanstalk  
* S3  
* RDS  

### Key concepts
* virtualenv
* Deployment using awsebcli
* Package dependencies
* Environment variables
* Container commands
* ssh access to ec2 instance  
* Storage and resolution of static assets   
* Database backend  
