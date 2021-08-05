# Docker based Ubuntu dev environment with Shiftleft
# Based on https://github.com/maliksahil/docker-ubuntu-sahil

I built this because I wanted to be able to spin up a clean unix environment to run Shiftleft scans with.

Here is what it gives me,
1. Basic commands like sudo, curl, nano
2. Installs latest version of node on start
3. Git support
4. ShiftLeft NG SAST scanner and Python3.8

## Usage
1. Ensure you have docker installed and running
2. Clone this repo
3. Open terminal and run, `chmod +x build.sh`
5. Run `./build.sh`

Easy! This should give you a linux prompt for a user called "devuser" with password "p@ssword1". This user is a sudoer.

# Finish the setup

1. Run you SL auth
2. Capture it using docker commit (see https://winsmarts.com/snapshot-a-docker-container-20df59bbd473)
    a) give it a tag of slinacan:sl

# Now to use it
1. chmod the run.sh file
    a) note that the run command mounts the current folder into ~/work
    b) It also will put the sl.log in the current folder

