#Nginx Dynamic Domain and Subdomin configuration
Very useful when creating dynamic domain and subdomain. Just create a directory and it'll automatically start pointing there.


#Directory structure
    /home/user
	|
	|
	website1.com
		|
		www
		subd1
		subd2
		subx.suby
	|
	|
	website2.com
		|
		www
		subd1  

**conf file will redirect non-www domain to www domain. It will then point to respective directory.**  
For eg:  
	www.website.com => /home/user/website1.com/www  
	subd1.website.com => /home/user/website1.com/subd1  
	subx.suby.website.com => /home/user/website1.com/subx.suby  

#How it works
1. Extract the domain and subdomain from the host.
2. Points it to pre-defined directory structure.