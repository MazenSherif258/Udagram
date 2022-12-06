# Pipleline Process

- ### After Pushing The Code To Github ( `main` branch ) 
- ### `CI/CD` App in our case `CircleCI` Detects the push then proceeds to do the steps written in its config file which consists of 
    - ##### Setting Up Enviroment And Installing Dependencies
    - ##### Buildng and testing the app to ensure that we are deploying good code
    - ##### Deploying our app to `AWS`

### - build job that contains several steps : 
    1. Installing node
    2. checkout step (git clone)
    3. Installing Front-end and Back-end dependencies
    4. Linting and building Front-end
    5. Building Back-end
### - Then deploy job will run only after a manual approval from `CircleCI` : 
    1. Installing node
    2. Installing and configuring AWS & EB CLI  
    3. checkout step (git clone)
    4. Deploying Back-end On ElasticBeanstalk
    5. Deploying Front-end On a S3 Bucket Configured for static web hosting

### Then Our Code Will Be Deployed So Users Can Now Access It and Use Our App.
