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

  - Step 1
  - Step 2
  - Step 3
  - Step 4
  

#### 2. Pipeline in Master Account to Deploy Pipeline in Production Account for Application Deployment
  
  - Step 1
  - Step 2
  - Step 3
  - Step 4
  

#### 3. Include Monitoring for Pipeline 

  - Step 1
  - Step 2
  - Step 3
  - Step 4
  

#### 4. Include Monitoring for Fargate Application 

  - Step 1
  - Step 2
  - Step 3
  - Step 4
  
