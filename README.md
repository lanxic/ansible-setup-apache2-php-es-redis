Ansible Provision for AWS EC2
-----------------------------

### Preparation

-	create your key for ec2 instance.
-	Installing Ansible for your local.
-	Rename all.sample to all in group_vars directory.
-	follow variable with your config and key.

### How to run

-	Build EC2 instance.

	```
	alex@Alex-Laptop:~$ sudo ansible-playbook -i hosts.ini buildAWS.yml --extra-vars "aws_access_key=YOUR_ACCESS_KEY aws_secret_key=YOUR_SECRET_KEY"
	```

-	Terminate EC2 instance

	```
	alex@Alex-Laptop:~$ sudo ansible-playbook -i hosts.ini terminateAWS.yml --extra-vars "aws_access_key=YOUR_ACCESS_KEY aws_secret_key=YOUR_SECRET_KEY"
	```
