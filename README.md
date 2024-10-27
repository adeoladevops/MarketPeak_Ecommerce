**Steps**<br>
1. Open Git Bash on my local PC.<br>
2. Make a new directory and initialize it for version control<br>
  	mkdir MarketPeak_Ecommerce<br>
  	cd MarketPeak_Ecommerce<br>
 	git init<br>
3. Proceeded to Tooplate and downloaded Waso ecommerce template.<br>
4. Extracted the template to 2130_waso_strategy and ready for to create a repository.<br>
  	git add . <br>
  	git config --global user.name adeoladevops <br>
  	git config --global user.email iloriabdulqoyum@gmail.com <br>
  	git commit -m "Initial commit with basic e-commerce site structure" <br>
5. Create new repository on Github MarketPeak_Ecommerce with a README.md.<br>
6. Push to git repository.<br>
  	git remote add origin https://github.com/adeoladevops/MarketPeak_Ecommerce.git <br>
  	git push -u origin master (main not working!) <br>
7. Set up EC2 instance on AWS.<br>
8. Set up public key for git.<br>
9. Add key to git.  <br>
10. Clone the git repo<br>
  	git clone git@github.com:adeoladevops/MarketPeak_Ecommerce.git <br>
11. Install apache2 web server<br>
  	sudo apt update <br>
  	sudo apt install apache2 <br>
  	sudo systemctl start apache2 <br>
  	sudo systemctl enable apache2 <br>
12. Configure the web server <br>
	sudo rm -rf /var/www/html/* <br>
  	sudo cp -r ~/MarketPeak_Ecommerce/* /var/www/html/ <br>
  	sudo systemctl reload httpd <br>
13. Access the ecommerce website using the public IP of the EC2 instance <br>
14. Deploy New features <br>
  	git branch development <br>
  	git checkout development <br>
15. Add new update on the “about template”, email and foot note/signature <br>
  	git add . <br>
  	git commit -m “fixing bug1, about page and added new features “ <br>
	git push --set-upstream origin development <br>
16. Create Pull request on Github <br>
17. Pull the update to ASW web server <br>
  	git pull origin master <br>
	sudo systemctl reload apache2 <br>
![image](https://github.com/user-attachments/assets/64f0df77-4306-4c34-aceb-e0f1d3095d58) <br>


18. Verify the change and development the README.md <br>
19. Added README.md on github <br>

**Troubleshoot and Challenges** <br>
1.	Origin main does not work, so I used origin master when setting up my github repository. <br>
2.	Since I was using Ubuntu, the right command  installation isn’t “yum” but “apt”. <br>
3.	httpd package isn’t available however “apache2” web server is available. <br>
4.	After updating and pulling my repository from github, I repplace my application document in the “/var/www/html” directory since my git initialization wasn’t done there. <br>
