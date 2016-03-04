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
Where `AWS_ACCESS_KEY_ID, AWS_SECRET_ACCESS_KEY` are your IAM User's key-pair credentials. And `AWS_STORAGE_BUCKET_NAME` is the name of your S3 bucket.

* Postgresql DB Details  
`DB_ENGINE, DB_HOST, DB_NAME, DB_PASSWORD, DB_PORT, DB_USER`  
Since we are using Postgresql DB as backend, specify the `DB_ENGINE` as `django.db.backends.postgresql_psycopg2`
Get the value for `DB_HOST, DB_NAME, DB_PASSWORD, DB_PORT, DB_USER` from the RDS console.

* Admin details  
`SUPER_USER_EMAIL, SUPER_USER_NAME, SUPER_USER_PASSWORD`  
Specify these so that a superuser will get created and you will be able to access the dango admin using these credentials.


#### 2. Clone and deploy django-awsome to EBS
`git clone https://github.com/pushkarparanjpe/django-awsome.git`  
`cd django-awsome/`  
`eb init`  
`eb deploy`  



