# A Beginner's Guide to SSH Key Authentication for GitHub

<h3> Step1: Generate an SSH Key </h3>
Login to the terminal and generate SSH key using below command 

```
ssh-keygen -t rsa -b 4096 -c "your_email@address.com"
```
Follow the instructions to save the file(Defualt location also fine).
If passparse required for the key, provide it when prompted. If no passpharse is needed you can simply press Enter key.

<h3> Step2: Add the SSH key to SSH Agent </h3> 
once the Key is generated, you need to add it to the SSH agent. Follow these steps to attach the SSH Key to the SSH Agent.

<b>1.</b> Start SSH Agent
``` 
eval "$(ssh-agent -s)"
 ```
 <b>2.</b> Add your SSH Key to Agent

```
ssh-add ~/.ssh/id_rsa
```
<h3>Step3: Add SSH Key to you GitHub Account</h3>
Copy the SSH Key to you clipboard or Notepad.

```
cat ~/.ssh/id_rsa.pub
```
Login to GitHub Account, navigate to Account settings and select ```SSH and GPG Keys``` tab in left side pane.
Click on the New SSH Key Option, Give the title for the SSH Key indentification and paste the earlier copied Key into the Key field and save.

<h3>Step4: Set the Remote URL to use SSH</h3>

Run the  below command to set the remote URL in terminal.
```
git remote set-url origin git@github.com:GitHub_username/Devops_Learning.git
```

Using this method you can securely log in to your GitHub account directly from the terminal.