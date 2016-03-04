# django-awsome
It is a "Hello world" reference implementation of a basic django app with deployability on AWS ElasticBeanstalk in mind. It contains a django project named `one` and a django app named `hello`. Just configure your EBS enviroment, clone this repo and deploy!

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


#### 3. Visit the root URL
Visit `http://YOUR_ENV_CONTEXT.elasticbeanstalk.com/`
You should see the happy django message:
> It worked!  
> Congratulations on your first Django-powered page.  
> ...  


#### 4. Visit the admin login page
You should be able to see the pretty contrib admin login interface (CSS + JS should have loaded smoothly via S3).
You should be able to login using the SUPER_USER credentials that your specified in the EBS environmet configuration.  

That's all folks!  
Now go make awesome things, at scale. ^-^


