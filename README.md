# What is Server Backup?
This is a discord bot that will keep your personal server contents backed up, incase of a server termination, account deletion etc.

# How does this work?
There is two systems working behind the scenes to keep your server backed up

1. Initial Backup : Backup every messages in the entire server, on bot startup
2. Live Backup    : Backup messages as its being sent in the current moment. 

By default, both systems will function. but they can be disabled in the .env as follows: 
```INITIAL_BACKUP=false
LIVE_BACKUP=false
```