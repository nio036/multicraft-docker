Single Multicraft container modified from LZStealth.

docker build -t multicraft .
 
docker run -d -it -p 80:80 -p 25565:25565 --name devtest  -v MulticraftData:/mc multicraft

  

enter bash
docker exec -it multicraft /bin/bash

Map container path to "/mc"

Map Container port 80 to whatever you want for the web portal.

Map TCP/UDP ports for your game server(s). Map as many as needed. (Default is 25565 for minecraft but is NOT added by default)



Map the following Variables as needed. (The following are defaulted variables)

- MC_DAEMON_ID="1"
- MC_DAEMON_PW="qwerty123"
- MC_FTP_IP=""
- MC_FTP_PORT="21"
- MC_FTP_SERVER="y"
- MC_KEY=""
