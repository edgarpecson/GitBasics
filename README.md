# GitBasics

This document contains notes on git configurations:


1.  Configure ssh between Mac and github
2.    - on mac: cd ~
      - ssh-keygen
      - copy id_rsa.pub
      - In github settings, add/paste in new ssh keys or add new
  


<h2>It is better to create the Repository in Github and then clone it to you mac</h2>

1. Make an empty git respository on the Desktop
2.       - Initialize the directory:  git init
3.       - clone the respository from github:  git clone <ssh link>










From co-pilot
To set up Git on your Mac and connect it to GitHub, follow these steps:

Install Git:
Open the Terminal and install Git using Homebrew:

sh
brew install git
Configure Git:
Set your username and email for Git:

sh
git config --global user.name "Your Name"
git config --global user.email "your_email@example.com"
Generate SSH Key:
Generate an SSH key to securely connect with GitHub:

sh
ssh-keygen -t rsa -b 4096 -C "your_email@example.com"
Follow the prompts to save the key (default location is recommended).

Add SSH Key to GitHub:
Copy the SSH key to your clipboard:

sh
pbcopy < ~/.ssh/id_rsa.pub
Go to GitHub SSH keys settings and add a new SSH key, then paste the key from your clipboard.

Test SSH Connection:
Test if the connection to GitHub works:

sh
ssh -T git@github.com
You should see a success message.

Clone a Repository:
Clone a repository to your local machine:

sh
git clone git@github.com:username/repo.git

