## What is Server Backup?

This is a discord bot that will keep your personal server contents backed up, incase of a server termination, account deletion etc. This is just to deal with discord's randomness, we all love discord dont we?

---

## How does this work?

There are two systems working behind the scenes to keep your server backed up

1. **Initial Backup**: Backup every messages in the entire server, on bot startup
2. **Live Backup**: Backup messages as its being sent in the current moment. 

By default, both systems will function. but they can be disabled in the .env as follows: 
```INITIAL_BACKUP=false```
```LIVE_BACKUP=false```

---

### ⚙️ Installation

- Requires: `Nodejs 17+ & Typescript`
- Clone repo: `git clone https://github.com/Emitter-166/server-backup/ && cd server-backup`
- Install dependencies: `npm i`
- Copy .env: `cp example.env .env`
- Edit the `.env` and put in the required configuration (token, password, guildId)
- Build the project: `npm run build`
- Start: `npm start`

---

### 🧑‍🔧 Configuration

The configuration is done through the `.env` file. Here are the options:

- `TOKEN`: Your bot token goes here.
- `PASSWORD`: Encryption password you want to use. Keep empty if you don't want encryption.
- `GUILD_ID`: serverId of the server you want to back up.
- `INITIAL_BACKUP`: Should the bot do initial backup of the entire server on startup? (true/false)
- `LIVE_BACKUP`: Should the bot do live message backups as its being sent? If disabled, the program will shut down after initial backup is done (true/false)
- `IGNORE_CHANNELS`: Channels to avoid while back up. Provide the IDs, separated by commas.
- `IGNORE_USERS`: Users to avoid while back up. Provide the IDs, separated by commas.
- `BACKUP_DB`: Should the app back up the database on a weekly basis? (true/false).

Remember to replace the placeholders with your actual data.

---

### 🔥 Features

- Encrypted backups using AES-256 military grade algorithm
- Utilizing sqlite database for compactness and ease of handling
- Automatically backs up the entire server on startup
- Automatically backs up threads as well (Both Archived & Active)
- Backs up DB on weekly basis
- Highly customizable
- For the sake of simplicity, it only backs up the following params in a message
    - UserId
    - Message string content
    - Message attachments
    - Sent At

---

### ❗ Disclaimers

- I am not responsible for anything that may happen, such as, Data Corruption and etc
- You do need a 24/7 bot hosting for this to work at its fullest. Though you can run it locally to make initial back ups
- This was a quick project that was made for my own personal use, but I realized many other people may need this as well due to discords unpredictable behavior

