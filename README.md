# Description
World Chat Module enables you to talk globally with your faction or with both factions (if enabled by server).

The GM can see both factions messages if he has the chat active and gm mode on. (.gm on)
# Commands
List of fully functional commands:
* .chat <$TEXT>
  - Used to talk on the World Chat
* .chat on
  - Used to enable World Chat
* .chat off
  - Used to disable World Chat
* .chata <$TEXT>
  - Used to talk for GM's to alliance faction ( so you can talk to the other faction when cross-faction world chat is disabled )
* .chath <$TEXT>
  - Used to talk for GM's to horde faction ( so you can talk to the other factions when cross-faction world chat is disabled )
  
# Installation
## Core Setup

To add the module follow the next steps:
1. Go into the folder <source_of_335>/modules
2. Clone the repository here:
###Windows
Open git bash and paste this command
```
git clone https://github.com/wizzymore/mod_world_chat.git
```
###Linux
```
git clone https://github.com/wizzymore/mod_world_chat.git
```

## Database Setup
### Setting up commands
```sql
INSERT INTO `command` (`name`, `security`, `help`) VALUES ('chata', 1, 'Syntax: .chata $text - To speak as a GM only to Alliance');
INSERT INTO `command` (`name`, `security`, `help`) VALUES ('chath', 1, 'Syntax: .chath $text - To speak as a GM only to Horde');
INSERT INTO `command` (`name`, `security`, `help`) VALUES ('chat', 0, 'Syntax: .chat $text\n.chat on To show World Chat\n.chat off To hide World Chat');
```

## Server Config Setup
Create a file named : "WorldChat.conf" or copy the one from <build_of_335>/bin/<your_build_method/WorldChat.conf
```
###################################################################################################
# WIZZY WORLD CHAT SYSTEM
#
# These settings control WiiZZy's World Chat System
#
#    World_Chat.Enable
#        Description: Enables WiiZZy's World Chat System
#        Default:     True - (Enabled)
#                     False - (Disabled)

World_Chat.Enable = true

#
#    World_Chat.CrossFactions
#        Description: Enables world chatting cross-faction
#        Default:     False - (Disabled)
#                     True - (Enabled)
#

World_Chat.CrossFactions = false

#
###################################################################################################
```
## Start the server and enjoy
Done, you are ready to use the World Chat System! Go online and try it out!
