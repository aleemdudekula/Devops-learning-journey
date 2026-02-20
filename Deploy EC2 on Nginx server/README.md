# Hello frd,
Today i learnt Deploy-EC2instance-on-nginx 

## 1. Create EC2 on AWS 
   
   login AWS console login page then go to EC2 instance 

   click instance and configure u r requirements (OS, ram, cpu, memory)..,
   
   create security key file and download either pem file / ppk file 
   
   Then launch instance (remeber u r IP later we can use)
   
## 2. EC2 Configure on my Local system through WSL on windows

   copy that file on WSL files 
   
   --> cp /mnt/c/program\ Files/WSL\pemfile
   
   configure Ec2 on WSL
   
   --> sudo ssh -i pemfile machine@ip(ec2-instance-ip)
   
   sudo apt update && upgrade -y this update u r machine
   
## 3. Now move to advance 

   Ec2 instance connect through on web page(like http-port(80)
   
   before that u can check inbound rules in security group where u can add rule 

   Otherwise you can face an error on webpage
   
   --> http - 80 - 0.0.0.0/0(Anywhere IPV4)
   
## 4. Install Nginx inside u r EC2 instance

   --> sudo apt install nginx -y
   
   --> sudo systemctl start nginx
   
## 5. open web browser type: ```http://ec2-ip-add/```


## 6. we can find out welcome ngnix 

   "Boom u r first Ec2 Instance server" deployed"
   
## 7. do practice cmds like 

   --> sudo systemctl restart nginx
   
   --> sudo systemctl stop nginx
   
   --> sudo systemctl start nginx
   
   --> sudo systemctl status nginx
   
## 8. Go to directory /var/ww/html/ u can modified the file index.html

   here changes happen in index.html file 

   vi index.html

## 9. Go to directiry /var/log/nginx u can access file like error.log & access.log file

   cat error.log 

   cat access.log

## Bonus tip

WSL is far more reliable than GUI tools like MobaXterm for SSH —

 less abstraction, fewer hidden issues.
