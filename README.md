What this does:
* Creates a Docker container
* Installs SmSn
* Sometimes, installs Gremlin-Server
    * Lately it can't seem to download Grapes
* Configures Gremlin-Server to work with SmSn

Remaining to do:
* Mount external graph data
* Make a Docker image from it

How to use this code:
* Navigate to where smsn-docker.sh (or this README file) is. Call that place PATH.
* Optional but recommended: Download apache-tinkerpop-gremlin-server-3.2.4-bin.zip to PATH.
    * This script can download it, but it's not smart about handling mirrors, hence slow.
    * Josh wrote a script that is clever about that; see the section called "# fetch and expand Gremlin Server" of the file install-smsn.unfinished.sh. I have not incorprated that code into this yet.
* From a shell, run this.
    * sudo docker run -it --name smsn-docker -v PATH:/mnt ubuntu bash
    * This gives the Docker container access to all the files in PATH. It does not modify them.
* After that, from within the resulting Docker-contained shell, run:
    * bash /mnt/docker-smsn.sh





