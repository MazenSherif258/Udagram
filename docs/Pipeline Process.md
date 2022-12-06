# Pipleline Process
## - build_test job that contains several steps : 
    1. Installing node
    2. checkout step (git clone)
    3. Installing Front-end and Back-end dependencies
    4. Linting and building Front-end
    5. Building Back-end
    6. Testing Front-end (Unit tests & e2e tests)
## - deploy job will run only after a manual approval from cricle ci : 
    1. Installing node
    2. Installing and configuring AWS & EB CLI  
    3. checkout step (git clone)
    4. Deploying Both Back-end and Front-end
