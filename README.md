# cloud-application-server
My version of Udacity's DevOps Nanodegree P1

## Technical part

* prerequisits: you need `packer` installed and an Amazon AWS account that has administrative rights
* copy `env.in` to `env` and fill in your Amazon AWS credentials in `env`
* load the environment variables by sourcing the file with `. env` or `source env` in your terminal. (The variables will only be available in this terminal session, so whenever you open a new one you need to repeat this step)
* build the image with `packer build sonarqube-server.json`
