## Analytical section

ChalkFull wants to launch a new product: a way to build lesson plans quickly. This product is a separate app that can be run on standalone servers without a connection to the existing environment and is planned to be hosted with a major cloud provider.

For the first phase, the friendly-user test, only a selected group of current users will have access to the new product. This means that the full functionality of the product must be implemented, but the resources needed from the cloud provider are for this stage are less than for the full launch that will happen later.

One of the reasons for the friendly-user test phase is that the operations team needs to gather real-world experience and performance with the cloud platform that will be used.

### Platform

The product consists of a single-page web app written in JavaScript and a RESTful API written in python and backed by a MongoDB database. The team is comfortable with running the software on debian-based linux distributions (Debian itself or Ubuntu) and prefers having virtual machines provided by the cloud provider over distributed computing solutions like Google App Engine or Amazon AWS Elastic Beanstalk.

### Setup

For the friendly-user testing phase, all components will be installed on a single virtual machine instance:

- MongoDB
- Apache httpd web server with mod_wsgi
- Python 2.7

### Price comparison Amazon AWS vs. Google Compute Engine

The team assumes that there will be considerable spikes in the load the system has to handle, as teachers tend to work on their lesson plans during the summer holidays and on weekends. Therefore, the virtual machine instance types chosen from the cloud provider should handle variable load and scale up and down according to the actual load without intervention from the ChalkFull operations team. For Amazon AWS, the best instance type for these requirements are the General Purpose T2 Burstable Performance Instances (see https://aws.amazon.com/ec2/instance-types/). Even if only a limited number of users will access the system during friendly-user testing, the team is worried about the RAM requirements of MongoDB and selected the 't2.large' variant with 8GB or RAM. Storage on Amazon EBS (Elastic Block Store) is included. This instance type costs $0.104 per Hour, i.e. about $80 per month.

The comparable offering from Google Compute Engine uses the n1-standard-2 instance type, 7.5 GB RAM and 128GB of persistant storage. The estimated cost is the same, but this instance type does not support on-demand transparent scaling. Therefore, the team would prefer to use Amazon AWS.


