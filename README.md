### im drinkings a slurpee rn
lmao it works, You need to use the Mounts Feature in Pterodactyl and mount the full Titanfall 2 game @/mnt/titanfall on the container

### Get the tiddy falls 2 game.
quickest way to get the game, is to use steamcmd.sh and fool it to thinkings its a windows machine, login and then download the game to a dir. (all this is in the steamcmd docs)

./steamcmd.sh +@sSteamCmdForcePlatformType windows +force_install_dir /TF2/ +login *USERNAME* +app_update 1237970 validate +quit

The above line, downloads titanfall2 and put it in /TF2/

## Docker File?? Wanna build your own??

This egg is based off a custom docker image that was built off of https://github.com/pg9182/northstar-dedicated

All i did was make sure the user that was created was the Container user.
Fuck the entry script etc, the Enviroment variables handle all the server config anyways.

### Egg Vars

Ive only included Server_Name Server Description, and Server Password as Egg Vars add the others as you wish.


| Environment variable      | Description |
| ---                       | --- |
| NS_SERVER_NAME            | **Required.** The server name to show in the server browser. |
| NS_SERVER_DESC            | The server description to show in the server browser. |
| NS_SERVER_PASSWORD        | The password for the server. If empty, the server is public. |
| NS_PORT                   | The UDP game port. Must match with the forwarded port and be accessible from the default external IP. |
| NS_PORT_AUTH              | The TCP player authentication port. Must match with the forwarded port and be accessible from the default external IP. |
| NS_MASTERSERVER_URL       | The base URL of the master server. |
| NS_MASTERSERVER_REGISTER  | True/false for whether the server should register with the master server. If false, you will probably want to set NS_INSECURE to true. |
| NS_INSECURE               | Whether to allow unauthenticated direct connections to the server. |
