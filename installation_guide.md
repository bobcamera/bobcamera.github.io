# BOB the Universal Object Tracker: Installation Guide

Below are the installation instructions for installing BOB
The application uses Docker and Docker Compose to run, at present we are still in a very early release phase so this the install process is not polished at all. We will endeavour to improve this over time to please bear with us.

*It is possible to run Bobcamera on Windows 10 or Windows 11 through WSL. Please refer to the [Windows setup instructions](WINDOWS_SETUP.md) to prep your machine before running the steps below.*

## The following steps will need to be performed in a linux terminal

- Ubuntu 23.10 has been tested
- Ubuntu 22.04 has been tested

### 1. Install dependencies
- Git
- Curl
```
sudo apt-get install git curl
```
### 2. Clone the github repo
```
git clone --recursive https://github.com/bobcamera/bobcamera.git
```
### 3. Change directory to bobcamera
```
cd bobcamera
```
### 4. Set the setup script as executable
```
chmod +x setup.sh
```
### 5. Run the setup script, this will install docker and docker compose
```
./setup.sh
```
### 6. Reboot the machine
```
sudo shutdown -r now
```
### 7. Navigate back to the bobcamera directory once rebooted
```
cd ~/bobcamera
```
### 8. Copy the .env.example file to .env and edit the file to set the right values for your camera

You can do this with your favorite file manager and text editor.

In this example, we use nano:
```
cp .env.example .env
nano .env
```

To save a file using nano, press CTRL + X, then Y, then ENTER

### 11. To start up BOB
```
docker compose up
```
### 12. Use your system browser and navigate to [http://127.0.0.1:8080](http://127.0.0.1:8080)

### 13. To shut BOB down, type CTRL + C in the terminal
