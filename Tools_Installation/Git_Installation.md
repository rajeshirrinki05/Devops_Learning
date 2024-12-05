# Below steps will explain How to Install Git on a Linux System.

**Step 1: Identify Your Operating System**

First, determine which operating system you are using by running the following command:
 ```bash 
 cat /etc/os-release
```

**Example Output :**
```
NAME="Ubuntu"
VERSION="18.04.4 LTS (Bionic Beaver)"
ID=ubuntu
ID_LIKE=debian
PRETTY_NAME="Ubuntu 18.04.4 LTS"
VERSION_ID="18.04"
HOME_URL="https://www.ubuntu.com/"
SUPPORT_URL="https://help.ubuntu.com/"
BUG_REPORT_URL="https://bugs.launchpad.net/ubuntu/"
PRIVACY_POLICY_URL="https://www.ubuntu.com/legal/terms-and-policies/privacy-policy"
VERSION_CODENAME=bionic
UBUNTU_CODENAME=bionic
```

**Step 2: Verify Git Installation**

Check if Git is already installed on your server by running:

  ```sudo git --version```
  
If Git is installed, this command will return the version number.

**Step 3: Update Your Package Index**

 Before installing Git, update your package index to ensure you have the latest information about available packages:

 ```sudo apt update```
  
**Step 4: Install Git**

Install Git using the following command:

  ```sudo apt install git```

**Step 5: Verify the Installation**

After installation, verify that Git is installed correctly by checking its version:
  
  ```sudo git --version```
  
**Step 6: Install Git Man Pages**

To install the manual pages for Git, use:

```sudo apt-get install git-man```
