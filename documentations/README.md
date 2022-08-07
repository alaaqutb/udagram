### Dependencies

```
- Node v14.15.1 (LTS) or more recent. While older versions can work it is advisable to keep node to latest LTS version

- npm 6.14.8 (LTS) or more recent, Yarn can work but was not tested for this project

- AWS CLI v2, v1 can work but was not tested for this project

- A RDS database running Postgres.

- A S3 bucket for hosting files.

```

### Application Infrastructure

#### Elastic Beanstalk
AWS Elastic Beanstalk is an easy-to-use service for deploying and scaling web applications and services in where we deploy our server.
EB URL: ```udagram-api-dev.eba-mi2ybm28.us-east-1.elasticbeanstalk.com```

#### S3 Bucket
Amazon S3 is cloud object storage in where we deploy our static files.
S3 URL: ```http://alaas3.s3-website-us-east-1.amazonaws.com ```

#### RDS PostgreSQL
Amazon Relational Database Service (RDS) in where we deploy our database for storing and retrieving information.
DB EndPoint: ```database-2.cfncsdxn2phq.us-east-1.rds.amazonaws.com```


### Udagram Pipeline

1. Build job:
   - Scripts:
       - ```npm run frontend:install```
       - ```npm run api:install```
       - ```npm run frontend:build```
       - ```npm run api:build```
   
2. Deploy job:
   - Scripts:
       - ```npm run frontend:deploy```
       - ```npm run ebPass```
       - ```npm run api:deploy```
       
   