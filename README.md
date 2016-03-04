# django-awsome
Minimal django app, ready for deployment on AWS ElasticBeanstalk.  
It is a "Hello world" example for django + AWS deployments. It contains a django project named `one` and a django app named `hello`.

### Features
* Static assets  
* DB backend  
* django Admin  

### Quickstart

#### 1. Specify environment variables
* django details  
`DJANGO_SETTINGS_MODULE`  
Specify the value as `one.settings`.

* S3 Details  
`AWS_ACCESS_KEY_ID, AWS_SECRET_ACCESS_KEY, AWS_STORAGE_BUCKET_NAME`  

* Postgresql DB Details  
`DB_ENGINE, DB_HOST, DB_NAME, DB_PASSWORD, DB_PORT, DB_USER`  

* Admin details  
`SUPER_USER_EMAIL, SUPER_USER_NAME, SUPER_USER_PASSWORD`  

#### 2. Clone and deploy django-awsome to EBS
`git clone https://github.com/pushkarparanjpe/django-awsome.git`  
`cd django-awsome/`  
`eb init`  
`eb deploy`  



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
