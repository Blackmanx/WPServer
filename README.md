# Instructions 

## Tested on Xubuntu 18

### Installation 
```
git clone https://github.com/WPServer/ && cd WPServer
```
### Content  
* ```Dockerfile``` (Instructs Docker to build the image)

* ```srcs/``` (contains configs and some bash scripts)

* ```srcs/build.sh``` (Build, run and enter a container)

* ```srcs/script.sh``` (Inits services and modifies some config files)

* ```index.sh``` (Changes autoindex while the container is running, then restarts nginx.)

* ```host.sh``` (If you open it in your xubuntu distro, it copies the mkcert to your computer so it works)

### Run Docker image
Open a Terminal in the Dockerfile directory, then run
```
bash srcs/build.sh
```
You will be prompted to (B)uild or (C)lean. C(lean) WILL remove all your docker images, be careful with that.
If you build, you'll be prompted to confirm if you want Autoindex On (Y)es or Off (N)o
Then go to https://localhost and Procceed to the page, it will probably prompt some error about the
SSL certificate, ignore it or else:

Go to srcs and edit host.sh, edit the /home/blackman/... paths to /home/your_username/..., then run
```
bash host.sh
```
in a terminal in your xubuntu/ubuntu distro. This will copy the MKCERT to your distro, and it will show as a
https web.


