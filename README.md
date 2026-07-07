Basic CMD commands:

| Command         | Purpose                    | Example                    |
| --------------- | -------------------------- | -------------------------- |
| `dir`           | List files and folders     | `dir`                      |
| `cd`            | Change directory           | `cd Documents`             |
| `cd..`          | Move up one directory      | `cd..`                     |
| `md` or `mkdir` | Create a folder            | `mkdir TestFolder`         |
| `rd` or `rmdir` | Remove an empty folder     | `rmdir TestFolder`         |
| `copy`          | Copy files                 | `copy file1.txt file2.txt` |
| `move`          | Move files                 | `move file.txt C:\Backup`  |
| `ren`           | Rename a file              | `ren old.txt new.txt`      |
| `del`           | Delete a file              | `del file.txt`             |
| `type`          | Display file contents      | `type notes.txt`           |
| `cls`           | Clear the screen           | `cls`                      |
| `echo`          | Display text               | `echo Hello World`         |
| `find`          | Search for text in a file  | `find "error" log.txt`     |
| `tree`          | Show folder structure      | `tree`                     |
| `ipconfig`      | Show network configuration | `ipconfig`                 |
| `ping`          | Test network connectivity  | `ping google.com`          |
| `tracert`       | Trace network route        | `tracert google.com`       |
| `netstat`       | Show network connections   | `netstat -an`              |
| `tasklist`      | Show running processes     | `tasklist`                 |
| `taskkill`      | End a process              | `taskkill /PID 1234 /F`    |
| `systeminfo`    | Show system details        | `systeminfo`               |
| `hostname`      | Show computer name         | `hostname`                 |
| `whoami`        | Show current user          | `whoami`                   |
| `shutdown`      | Shut down or restart PC    | `shutdown /r /t 0`         |

### Useful Networking Commands

ipconfig
ipconfig /all
ping 8.8.8.8
nslookup google.com
tracert google.com

### Useful File Commands

dir
mkdir Projects
cd Projects
copy file.txt backup.txt
ren backup.txt backup_old.txt
del backup_old.txt

### Useful System Commands

systeminfo
tasklist
taskkill /IM notepad.exe /F
sfc /scannow

### Commands Commonly Used in IT Support

ipconfig /release
ipconfig /renew
ipconfig /flushdns
net user
net localgroup administrators
gpupdate /force

Basic Linux commands

| Command         | Purpose                    | Example                    |
| --------------- | -------------------------- | -------------------------- |
| `pwd`           | Show current directory     | `pwd`                      |
| `ls`            | List files/folders         | `ls -l`                    |
| `cd`            | Change directory           | `cd Documents`             |
| `mkdir`         | Create a directory         | `mkdir test`               |
| `rmdir`         | Remove empty directory     | `rmdir test`               |
| `touch`         | Create empty file          | `touch file.txt`           |
| `cp`            | Copy files/directories     | `cp a.txt b.txt`           |
| `mv`            | Move or rename files       | `mv old.txt new.txt`       |
| `rm`            | Delete files/directories   | `rm file.txt`              |
| `cat`           | View file contents         | `cat notes.txt`            |
| `nano` / `vim`  | Edit files                 | `nano file.txt`            |
| `clear`         | Clear terminal screen      | `clear`                    |
| `man`           | Show command manual        | `man ls`                   |
| `echo`          | Print text/output          | `echo Hello`               |
| `find`          | Search for files           | `find . -name file.txt`    |
| `grep`          | Search text in files       | `grep "word" file.txt`     |
| `chmod`         | Change file permissions    | `chmod +x script.sh`       |
| `chown`         | Change file ownership      | `sudo chown user file`     |
| `ps`            | Show running processes     | `ps aux`                   |
| `top`           | Monitor system processes   | `top`                      |
| `kill`          | Stop a process             | `kill 1234`                |
| `df`            | Show disk usage            | `df -h`                    |
| `du`            | Show folder/file size      | `du -sh folder`            |
| `free`          | Show memory usage          | `free -h`                  |
| `uname`         | System information         | `uname -a`                 |
| `whoami`        | Current username           | `whoami`                   |
| `history`       | Show command history       | `history`                  |
| `wget`          | Download files             | `wget url`                 |
| `curl`          | Transfer data from URLs    | `curl https://example.com` |
| `tar`           | Archive/extract files      | `tar -xvf file.tar`        |
| `zip` / `unzip` | Compress/extract zip files | `unzip file.zip`           |
| `sudo`          | Run command as admin       | `sudo apt update`          |
| `truncate -s `  | Change file size           |`truncate -s 0 filename.txt`|
| `touch -t`      | Change date/time           | `touch -t 202607061200 filename.txt `|

"git log --format='%H' -n5" | script displays ids of last 5 commits
"git check-ignore .* * |  existing files ignored by your Git repository

### Useful Shortcuts

* `Ctrl + C` → Stop current command
* `Ctrl + L` → Clear screen
* `Tab` → Auto-complete commands/files
* `↑ / ↓` → Browse command history

### Common Package Commands (Ubuntu/Debian)

```bash
sudo apt update
sudo apt install package-name
sudo apt upgrade
```

### Common Navigation Example

```bash
pwd
ls
cd Downloads
mkdir project
cd project
touch app.py
ls
```


download, extract, and install eksctl:
curl --silent --location "https://github.com/weaveworks/eksctl/releases/latest/download/eksctl_$(uname -s)_amd64.tar.gz" | tar xz -C /tmp
sudo mv -v /tmp/eksctl /usr/local/bin

Verify: 
eksctl version

Create an eks cluster:
eksctl create cluster \
  --name nextwork-eks-cluster \
  --nodegroup-name nextwork-nodegroup \
  --node-type t3.micro \
  --nodes 3 \
  --nodes-min 1 \
  --nodes-max 3 \
  --version 1.33 \
  --region your-region-code

Install Git:
sudo dnf update
sudo dnf install git -y

Verify Git Version:
git --version

Configure Git:
git config --global user.name "yourname"
git config --global user.email "email"

Clone Git:
git clone your-github-url

Install Docker:
sudo yum install -y docker

Start Docker:
sudo service docker start

Add ec2-user to the Docker group:
sudo usermod -a -G docker ec2-user

Make sure your ec2-user has been added to the Docker group:
groups ec2-user

Build a container image:
docker build -t your-backend-image-folder .

Create a new Amazon ECR repository:
aws ecr create-repository \
  --repository-name nextwork-flask-backend \
  --image-scanning-configuration scanOnPush=true \
