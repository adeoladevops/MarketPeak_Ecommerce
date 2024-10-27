**Steps**
Open Git Bash on my local PC.
Make a new directory and initialize it for version control
  mkdir MarketPeak_Ecommerce
  cd MarketPeak_Ecommerce
  git init
Proceeded to Tooplate and downloaded Waso ecommerce template
Extracted the template to 2130_waso_strategy and ready for to create a repository.
  git add .
  git config --global user.name adeoladevops
  git config --global user.email iloriabdulqoyum@gmail.com
  git commit -m "Initial commit with basic e-commerce site structure"
Create new repository on Github MarketPeak_Ecommerce with a README.md
Push to git repository.
  git remote add origin https://github.com/adeoladevops/MarketPeak_Ecommerce.git
  git push -u origin master (main not working!)
Set up EC2 instance on AWS.
Set up public key for git.
Add key to git.
Clone the git repo
  git clone git@github.com:adeoladevops/MarketPeak_Ecommerce.git
Install apache2 web server
  sudo apt update
  sudo apt install apache2
  sudo systemctl start apache2
  sudo systemctl enable apache2
Configure the web server
	sudo rm -rf /var/www/html/*
  sudo cp -r ~/MarketPeak_Ecommerce/* /var/www/html/
  sudo systemctl reload httpd
Access the ecommerce website using the public IP of the EC2 instance
Deploy New features
  git branch development
  git checkout development
Add new update on the “about template”, email and foot note/signature
  git add .
  git commit -m “fixing bug1, about page and added new features “
	git push --set-upstream origin development
Create Pull request on Github
Pull the update to ASW web server
  git pull origin master
	sudo systemctl reload apache2
![image](https://github.com/user-attachments/assets/64f0df77-4306-4c34-aceb-e0f1d3095d58)


Verify the change and development the README.md
Push README.md to github

**Troubleshoot and Challenges**
  Origin main does not work, so I used origin master when setting up my github repository.
  Since I was using Ubuntu, the right command  installation isn’t “yum” but “apt”.
  httpd package isn’t available however “apache2” web server is available.
  After updating and pulling my repository from github, I repplace my application document in the “/var/www/html” directory since my git initialization wasn’t done there.
