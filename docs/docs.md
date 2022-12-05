# 1. Pipleline Process
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

# 2. App Dependencies
 - `Node v14.15.1` (LTS) or more recent version.

- `npm 6.14.8` (LTS) or more recent version.

- `AWS CLI` v2.

- A `RDS` database running Postgres.

- A `S3` bucket for hosting uploaded pictures.

- A `S3` bucket for hosting Application's Backend Front-end

- An `Elasting BeanStalk` Enviroment for hosting Application's Back-end

# 3. Infrastructure description

## Secrets
- `AWS_ACCESS_KEY_ID` Access id
- `AWS_BUCKET` name of media bucket
- `AWS_REGION` aws region
- `AWS_PROFILE` it's set to `default` by default
- `AWS_SECRET_ACCESS_KEY` AWS secret key
- `JWT_SECRET` jwt secret key

#### Secrets are Passed From CircleCI Pipeline to Our Application's Backend Which are then consumed in our code to make it work
