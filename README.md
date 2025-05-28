
![Logo](https://i.imgur.com/0ih5Uv0.png)

EMC Nation Tracker (ENT) is a disnake bot focused around making it easier for EarthMC players to track what happens within their nations. It aims to better integrate EarthMC with Discord by showing things such as citizens joining and leaving your nation, who is online, and keeping track of who in your Discord is verified as a citizen.  
## Features

- See current relationships with other nations with /information relations
- Get notified on when people leave and join your nation in a dedicated notifications channel
- Ensure the integrity of your citizens by verifying them on your Discord automatically
- See who is online at any time by having an Online Players embed in your Discord


## Commands

Information:
- /configuration settings -> See the current settings for your server such as your notifications channel and who you are tracking.
- /information relations -> Check to see the enemies and allies of a particular nation

Notifications:
- /notification channel -> Set the channel in which notifications will appear for nations you track
- /notification status -> Enable/Disable notifications for your server
- /notifications add -> Add a nation to track in your notifications
- /notificcations remove -> Remove a nation from tracking

Online Players Embeds:
- /embed add -> Create a new embed message in the current channel which will then turn into the Online Player Embed after some time (Cannot have more than one nation at a time)
- /embed remove -> Destroy the current Online Embed making it no longer update

Verifications:
- /verify add -> Link a Discord user and a Minecraft user together on your server.
- /verify remove -> Unlink a Discord and Minecraft user
- /verify check -> See what Minecraft username a Discord user is linked to
- /verify give-verified-role -> Enable/Disable automatically giving verified members your citizen role (Only will turn on if the citizen role has been set)
- /verify verify-checkup -> Scans through your verified players and removes them if they have left the server and also gives verified members the citizen role (If citizen role has been set)
## Navigation
ENT works off  of a very simple structure to allow easy debugging and updates. Here is a basic rundown of how to navigate the files:  
- Utils Folder -> Stores all commonly used functions such as updating server configurations for easy reuse.  
- Cogs Folder -> Stores logic for a collection of commands, such as embed.py defining all  /embed commands. The "cogs" which are the classes where the commands are stored are then loaded as extensions in the main.py file.  
- Background Tasks Folder -> Stores logic for all of the background processes and upkeep done by the bot such as checking for new notificiations and updating online embeds. Like commands, background tasks are also loaded in the main.py file as cogs.  
- api_storage Folder -> Stores all data about nations that have been tracked.  
- server_configurations Folder -> Stores all server configurations for servers using the bot.  
- constants.py -> Stores some directory information.  
- main.py -> The main builder file for the bot which loads in everything.


## Roadmap

- Add a feature to verifications to automatically check the API to see whether a user is actually a member of a nation
- Add a way to set a "default nation" for a server so when you don't specify a target it is automatically assumed
- Allow multiple OnlineEmbeds as well as letting you choose which channel and whether they are enabled/disabled


## Authors

- [@roDEV0](https://github.com/roDEV0) - Lead Developer

