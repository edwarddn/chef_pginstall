# pginstall

 - Install chef
	- wget https://packages.chef.io/stable/ubuntu/12.04/chefdk_0.14.25-1_amd64.deb
	- sudo dpkg -i chefdk_0.14.25-1_amd64.deb

 - Create CHEF-REPO structure
	- chef generate repo chef-repo
	- cd chef-repo

 - Download REPO: 
	- git clone https://github.com/edwarddn/chef_pginstall.git -l cookbooks/pginstall

 - Create your json (json_postgres.json)
 	- nano json_postgres.json
	- Add line: 
		-  {   "run_list": [ "recipe[pginstall]" ] } 

 - Execute CHEF-CLIENT mode LOCAL
	- sudo chef-client --local-mode -j json_postgres.json


 - Execute:
	- # ps -ef | grep postgres
	- # su - postgres
	- $ psql

