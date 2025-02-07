## Bug found
First deployment of production pipeline works as the cloudformation is created in that run.Subsequent run fails as there is no change in the template. 

``` An error occurred (ValidationError) when calling the UpdateStack operation: No updates are to be performed. ```


To avoid this instead of using $latest tag, use different tag for each repo
Will update the same early tomorrow and test it

## DevOps Enabled Deployment Of Fargate Application 

The solution will be created in the following steps: 

1. Deployment Pipeline in Master Account to Deploy Fargate Application to Production Account
2. Deployment Pipeline in Master to Deploy a Pipeline which create pipeline in Production Account for application deployment
3. Include cloudwatch alerts for various pipeline level monitoring
4. Include cloudwatch alerts for application monitoring

### Master Account  
Infrastucture will be deployed from Master Account which has Cross Account access to Production Account. 
It can be achived by the following ways

1. SSM Parameters - AWS Access and Secret key stored in encrypted secret as SSM parameters 
2. Cross Account Access - Cross Account access via access role and STS

Chose to use the 2nd Option in this case as its AWS best practice.Used Mastar Account and a pipeline to create the infrastructure in Production Account. 

### Production Account  
Supplied by Contrast Security as a deploying medium

#### 1. Deployment Pipeline in Master Account to Deploy Fargate Application to Production Account 

- Created static pipeline in master account to check the permission is working
- Once complete deployed the same in production account


#### 2. Pipeline in Master Account to Deploy Pipeline in Production Account for Application Deployment
  
- Tested production pipeline in production account
- Tested production pipeline deployed from master account

#### 3. Include Monitoring for Pipeline   

#### 4. Include Monitoring for Fargate Application 

## Improvements in progress
- Use of nested cloudformation templates by uploading the sub templates in dynamic S3 
- Check VPC details for security 
- Check Security Groups for security
- Work on s3 pull for the application


