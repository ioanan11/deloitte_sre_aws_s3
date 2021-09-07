**AMAZON WEB SERVICES - S3**

Amazon S3 is a secure and redundant storage system that uses a flat object storage structure through a web interface. It is always good to have our files backed up. That is why we need S3, which can store data (also known as objects) in BUCKETS. 
We can have different storage classes depending on the need of the business. Choosing a class that facilitates the user will be cost saving. S3 standard costs more than Glacier, for exmple.


The following figure shows how S3 works:

![alt text](https://github.com/ioanan11/deloitte_sre_aws_s3/blob/main/Screenshot%202021-09-07%20165235.png)

Step 1: Launch EC2 instance on AWS 
Note: has to be connected to the internet and don't forget to allow port 22
 

Step 2: SSH into the machine


Step 3: Make sure everything is up to date

	sudo apt-get update
	sudo apt-get upgrade


Step 4: Install dependencies

	sudo apt-get install python
	sudo apt-get install python-pip
	alias python=python3

Check version and make sure it is at least 3.5

	python --version 
	sudo pip install awscli
	aws configure


Step 5: Using the access key

-Insert access key:
	*************

-Insert secret access key:
	*************

-Insert region:
	eu-west-1

-Insert output format:
	json

	
Step 6: Use command
	aws s3 ls

Step 7: Creating a bucket

	aws s3 mb s3://sreioana

**Commands that can be used with files and buckets**

Copy file to bucket:
	aws s3 cp README.md s3://sreioana

Delete file from bucket:
	aws s3 rm s3://sreioana/README.md

Delete bucket:
	aws s3 rb s3://sreioana

Copy file from bucket:
	aws s3 cp s3://sreioana/README.md README.md
