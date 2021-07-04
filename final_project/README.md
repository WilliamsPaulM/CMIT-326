# cloudformation.json is used to create the final project from UMGC's CMIT-326

Note: This template will create infrastructure that will cost you money to run:  
* 1 VPC  
* 2 Private Subnets  
* 2 Public Subnets  
* 2 Route Tables (Private and Public)  
* 1 IGW  
* 1 NAT Gateway  
* 1 EIP  
* 1 Security Group  
* 1 t2.micro EC2 Server  

If you choose to run this template take special note of the mappings section...I added comments there (I know that was bad) pointing out the location of the lab files, the name of the key used for the ec2 instance, and the latest Amazon Linux 2 AMI at the time of writing. 

```
"Mappings": {
    "Environment": {
      "Lab": {
        "FileLocationComment": "Provided by Vocareum - Lab 2: Build your VPC and Launch a Web Server", 
        "FileLocation": "https://aws-tc-largeobjects.s3.amazonaws.com/AWS-TC-AcademyACF/acf-lab3-vpc/lab-app.zip",
        "KeyNameComment": "Matches the lab environment provided by Vocareum; adjust to your needs",
        "KeyName": "vockey",
        "AMIComment": "Latest available Amazon Linux 2 at the time of writing",
        "AMI": "ami-0ab4d1e9cf9a1215a"
      }
    }
  }
```
