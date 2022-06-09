# Minecraft Java on Ubuntu 18.04
### Written by TheGameAdmin

#### Pre-Requisites 
-  `dpkg --add-architecture i386; apt update; apt install wget tar unzip vim`
---
#### Java download jdk-18 & Install
-  `wget https://download.oracle.com/java/18/latest/jdk-18_linux-x64_bin.deb`
-  `dpkg -i jdk-18_linux-x64_bin.deb`
-  `update-alternatives --install "/usr/bin/java" "java" "/usr/lib/jvm/jdk-18/bin/java" 1`
---
#### Directory Structure
-  `mkdir -p minecraft/logs`
---
#### Configuration Setup
-  `echo "eula=true" > minecraft/eula.txt`

-  `touch minecraft/server.properties`
	```server-port=19135 
	rcon.port=19137
	query.port=19136
	rcon.password=Minecraft9000
	enable-rcon=true
	level-name=world
	motd=The Game Admin Server
	max-players=20
	level-seed=2976643220357667859```
---
#### Download and Run minecraft
-  `cd minecraft` 
-  `wget https://launcher.mojang.com/v1/objects/c8f83c5655308435b3dcf03c06d9fe8740a77469/server.jar`
-  `chmod 750 server.jar`
-  `java -jar server.jar`

