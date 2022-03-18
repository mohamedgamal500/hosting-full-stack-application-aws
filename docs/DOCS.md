## Infrastructure

#### S3 Bucket

using AWS S3 Bucket for deploying The udagram-frontend application

URL: `my-udgram-bucket.s3-website-us-east-1.amazonaws.com/home`

#### Elastic Beanstalk

using AWS Elastic Beanstalk (eb) for deploying the udagram-api

URL: `http://udgram-api-dev.eba-e9pxbpzm.us-east-1.elasticbeanstalk.com/api/v0`

#### RDS Postgres

using AWS RDS Postgres as a database

DB: `database-1.cxx8pogutrsl.us-east-1.rds.amazonaws.com`

## Dependencies

- Node.js
- A RDS database running Postgres.
- AWS CLI v1.
- A S3 bucket.

## Pipeline

connect github repo to circleci which detecting changes each time pushing to the main branch.

create `.circleci/config.yml` which will be readed by circleci and excute jobs

- 1st job udagram-frontend : build the frontend then deploy to s3 via AWS CLI.
- 2nd job udagram-backend :"build the backend then init the eb cli to deploy on created enviroment.
