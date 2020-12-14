
Build  Machine Images for Jenkins, R1soft and Wordpress using Packer
===========
Packer 


[![CI](https://travis-ci.org/sadsfae/ansible-elk.svg?branch=master)](https://travis-ci.org/sadsfae/ansible-elk)
## Steps to create AMI's

To create Jenkins AMI:


#### - Choose region from jenkins_region folder 

#### - Pick Jenkins.json from tools folder

#### Example:

 ```
   packer build -var-file  jenkins_regions/virginia.json  tools/jenkins.json
```   
 
Used variables
```
    "region": "us-east-1",
    "instance_type" : "t2.micro",
    "java_version": "1.8.0",
    "jenkins_version": "2.235.5-1.1"
```  

#### For R1soft and Wordpress similar steps




## What does it do?
Building AWS Mashine image for Jenkins, R1soft and Wordpress 

![packer](/image/uses.png?raw=true "Click Discover")


## Copy and paste commands 
* To run Jenkins:
```
   packer build -var-file  jenkins_regions/virginia.json  tools/jenkins.json
```   
* To run r1soft:
```
   packer build -var-file  r1soft_regions/virginia.json  tools/r1soft.json
```
* To run Wordpress:
```
   packer build -var-file  wordpress_regions/virginia.json  tools/wordpress.json 
```


