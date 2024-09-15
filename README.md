# fast-in-termux
Here's I'm telling about how to install Fast cli tool in termux without root device.

## What is Fast?
Fast is ⚡ A Smarter and More Efficient Way to Develop MIT App Inventor 2 Extensions. By minimizing boilerplate code, it enhances the developer experience and brings extension development closer to the feel of native Android app creation. [Read More](https://github.com/jewelshkjony/fast-cli).

## Video Tutorial
https://youtu.be/I7o48XLKGpY

## Commands 
1st step is we need install ubuntu in termux for it we can use ubuntu-in-termux tool provided by [MFDGaming](https://github.com/MFDGaming/ubuntu-in-termux)

##### Update and Upgrade Termux
```shell
apt-get update && apt-get upgrade -y
```

##### Install wget
```shell
apt-get install wget -y
```

##### Install proot
```shell
apt-get install proot -y
```

##### Install git
```shell
apt-get install git -y
```

##### Go to Termux HOME Directory.
```shell
cd ~
```

##### Clone ubuntu-in-termux repository.
```shell
git clone https://github.com/MFDGaming/ubuntu-in-termux.git
```

##### Go to Script Directory.
```shell
cd ubuntu-in-termux
```

##### Give execution permission.
```shell
chmod +x ubuntu.sh
```

##### Run the script.
```shell
./ubuntu.sh -y
```

##### Now just start ubuntu.
```shell
./startubuntu.sh
```

##### Exit from ubuntu.
```shell
exit
```

### Making short command to start ubuntu

##### Open .bashrc file
```shell
nano ~/.bashrc
```

##### Paste in .bashrc file then CTRL + X then Y to save changes.
```shell
start() {
    if [ "$1" == "ubuntu" ]; then
        bash /data/data/com.termux/files/home/ubuntu-in-termux/startubuntu.sh
    else
        echo "Unknown command: $1"
    fi
}
```

##### Reload .bashrc file
```shell
source ~/.bashrc
```

##### Start ubuntu
```shell
start ubuntu
```

##### Update ubuntu
```shell
apt-get update -y
```

##### Upgrade ubuntu
```shell
apt-get upgrade -y
```

##### Install sudo package in ubuntu
```shell
apt-get install sudo -y
```

##### Update ubuntu using sudo
```shell
sudo apt-get update
```

##### Upgrade ubuntu using sudo
```shell
sudo apt-get upgrade
```

##### Install curl
```shell
sudo apt-get install curl
```

##### Install unzip
```shell
sudo apt-get install unzip
```

### Install Openjdk-8
```shell
sudo apt-get install openjdk-8-jdk
```

### Install Fast
```shell
curl https://raw.githubusercontent.com/jewelshkjony/fast-cli/main/scripts/install/install.sh -fsSL | sh
```

After installing Fast. open a termux, enter `start ubuntu`, navigate to the directory where you want to create your extension, and run `fast create <extension_name>`. Simply follow the prompts, and voilà, your brand-new Fast project is ready to go! 🎉

Next, navigate to the newly created directory by running cd <extension_name>, then execute `fast build`. Once the build process finishes, your extension will be available in the out directory. Congratulations! You've just built your first Fast extension. [Read More](https://github.com/jewelshkjony/fast-cli/wiki)
