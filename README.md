# ansible playbook for mac based development

this playbook installs and configures most of the software needed to quickly begin development on a mac. make sure you follow the documentation as some items cannot fully be automated.

--- 

## installation 

1. ensure apples command line tools are installed
```
xcode-select --install
```
2. install ansible
	i. run the following command to add python3 to your $PATH: 
	```
	export PATH="$HOME/Library/Python/3.9/bin:/opt/homebrew/bin:$PATH"
	```
	ii. upgrade pip:
	```
	sudo pip3 install --upgrade pip
	```
	iii. install ansible:
	```
	pip3 install ansible
	```
3. clone this repo to your local drive
4. inside this repository on your local drive, run:
```
ansible-galaxy install -r requirements.yml
```
5. followed by:
```
ansible-playbook main.yml --ask-become-pass
```
make sure you enter your macOS account pwd when prompted for the "BECOME" pwd

If for some reason your homebrew commands fail, make sure you have agreed to xcodes license with:
```
sudo xcodebuild -license
```
or fix some other brew issue with the following cmd:
```
brew doctor
```

