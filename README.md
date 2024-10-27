**Steps**<br>
Open Git Bash on my local PC.<br>
Make a new directory and initialize it for version control<br>
  mkdir MarketPeak_Ecommerce<br>
  cd MarketPeak_Ecommerce<br>
  git init<br>
Proceeded to Tooplate and downloaded Waso ecommerce template.<br>
Extracted the template to 2130_waso_strategy and ready for to create a repository.<br>
  git add . <br>
  git config --global user.name adeoladevops <br>
  git config --global user.email iloriabdulqoyum@gmail.com <br>
  git commit -m "Initial commit with basic e-commerce site structure" <br>
Create new repository on Github MarketPeak_Ecommerce with a README.md.<br>
Push to git repository.<br>
  git remote add origin https://github.com/adeoladevops/MarketPeak_Ecommerce.git <br>
  git push -u origin master (main not working!) <br>
Set up EC2 instance on AWS.<br>
Set up public key for git.<br>
Add key to git.  <br>
Clone the git repo<br>
  git clone git@github.com:adeoladevops/MarketPeak_Ecommerce.git <br>
Install apache2 web server<br>
  sudo apt update <br>
  sudo apt install apache2 <br>
  sudo systemctl start apache2 <br>
  sudo systemctl enable apache2 <br>
Configure the web server <br>
	sudo rm -rf /var/www/html/* <br>
  sudo cp -r ~/MarketPeak_Ecommerce/* /var/www/html/ <br>
  sudo systemctl reload httpd <br>
Access the ecommerce website using the public IP of the EC2 instance <br>
Deploy New features <br>
  git branch development <br>
  git checkout development <br>
Add new update on the “about template”, email and foot note/signature <br>
  git add . <br>
  git commit -m “fixing bug1, about page and added new features “ <br>
	git push --set-upstream origin development <br>
Create Pull request on Github <br>
Pull the update to ASW web server <br>
  git pull origin master <br>
	sudo systemctl reload apache2 <br>
![image](https://github.com/user-attachments/assets/64f0df77-4306-4c34-aceb-e0f1d3095d58) <br>


Verify the change and development the README.md <br>
Push README.md to github <br>

**Troubleshoot and Challenges** <br>
  Origin main does not work, so I used origin master when setting up my github repository. <br>
  Since I was using Ubuntu, the right command  installation isn’t “yum” but “apt”. <br>
  httpd package isn’t available however “apache2” web server is available. <br>
  After updating and pulling my repository from github, I repplace my application document in the “/var/www/html” directory since my git initialization wasn’t done there. <br>
