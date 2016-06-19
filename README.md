# cloud-application-server
My version of Udacity's DevOps Nanodegree P1

## Technical section

* prerequisits: you need `packer` installed and an Amazon AWS account that has administrative rights
* copy `env.sh.in` to `env.sh` and fill in your Amazon AWS credentials in `env`
* **Never commit any cloud service provider credentials to git. Always make sure that any file containing credentials is listed in `.gitignore` **
* load the environment variables by sourcing the file with `. env.sh` or `source env.sh` in your terminal. (The variables will only be available in this terminal session, so whenever you open a new one you need to repeat this step)
* build the image with `packer build sonarqube-server.json`
* verify that an AMI (Amazon Machine Image) is created in the AWS web interface
* Launch a new AWS instance from the newly-built AMI
* Log in to the new AWS instance and verify that SonarQube can be installed by following the installation instructions on http://docs.sonarqube.org/display/SONAR/Installing+the+Server

## Analytical section

* please see [analytical section](Analytical_section.md)
