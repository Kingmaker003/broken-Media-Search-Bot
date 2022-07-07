# [Media Search bot](https://github.com/Mahesh0253/Media-Search-bot)

<p align="center">
  <a href="https://www.python.org">
    <img src="http://ForTheBadge.com/images/badges/made-with-python.svg" width ="250">
  </a>
  <a href="https://t.me/ShadowKing9o">
    <img src="https://telegra.ph/file/93a7e33b65dc93349c0be.jpg" width="250">
  </a><br>
  <a href="https://t.me/ShadowsArena">
    &nbsp;<img src="https://img.shields.io/badge/Shadow%20Arena-Channel-blue?style=plastic&logo=Telegram" width="130" height="18">&nbsp;
  </a>
  <a href="https://t.me/+9Zhp_GdQVctiNjc1">
    &nbsp;<img src="https://img.shields.io/badge/Movie%20Addaa-Group-blue?style=plastic&logo=Telegram" width="130" height="18">&nbsp;
  </a>
  <br>
  <a href="https://github.com/Kingmaker003/broken-Media-Search-Bot/stargazers">
    <img src="https://img.shields.io/github/stars/MasterShad0w/Shadow-Media-Search-Bot?style=social">
  </a>
  <a href="https://github.com/MasterShad0w/Shadow-Media-Search-Bot/fork">
    <img src="https://img.shields.io/github/forks/MasterShad0w/Shadow-Media-Search-Bot?label=Fork&style=social">
  </a>  
  <br>
  <a href="https://youtube.com/channel/UCqVIzF-2AhO_pY4uo8Rr5Hg">
    <img src="https://img.shields.io/badge/Subscribe-Shadow%20Arena-%23FA0606?style=for-the-badge&logo=Youtube" width="300">
  </a>
</p>

* Index channel or group files for inline search.
* When you post file on telegram channel or group this bot will save that file in database, so you can search easily in inline mode.
* Supports document, video and audio file formats with caption support.

## Installation

### Tutorial<br>
<a href="https://youtu.be/dsuTn4qV2GA">
  <img src="https://img.shields.io/badge/How%20to-Deploy-red?logo=youtube" width="147">
</a><br>

### Easy Way
[![Deploy](https://www.herokucdn.com/deploy/button.svg)](https://heroku.com/deploy?template=https://github.com/MasterShad0w/Shadow-Media-Search-Bot)


### Hard Way
```bash
# Create virtual environment
python3 -m venv env

# Activate virtual environment
env\Scripts\activate.bat # For Windows
source env/bin/activate # For Linux or MacOS

# Install Packages
pip3 install -r requirements.txt

# Edit info.py with variables as given below then run bot
python3 bot.py
```
Check [`sample_info.py`](sample_info.py) before editing [`info.py`](info.py) file

### Docker
```
docker run -d \
    -e BOT_TOKEN="123456:ABC-DEF1234ghIkl-zyx57W2v1u123ew11" \
    -e API_ID='12345' \
    -e API_HASH='0123456789abcdef0123456789abcdef' \
    -e CHANNELS='-10012345678' \
    -e ADMINS='123456789' \
    -e DATABASE_URI="mongodb+srv://...mongodb.net/Database?retryWrites=true&w=majority" \
    -e DATABASE_NAME=databasename \
    --restart on-failure \
    --name mediasearchbot botxtg/media-search-bot
```
You can also run with `env` file like below,
```
docker run -d \ 
     --env-file .env \
     --restart on-failure \
     --name mediasearchbot botxtg/media-search-bot
```

## Variables
### Required Variables
* `BOT_TOKEN`: Create a bot using [@BotFather](https://telegram.dog/BotFather), and get the Telegram API token.
* `API_ID`: Get this value from [telegram.org](https://my.telegram.org/apps)
* `API_HASH`: Get this value from [telegram.org](https://my.telegram.org/apps)
* `CHANNELS`: Username or ID of channel or group. Separate multiple IDs by space
* `ADMINS`: Username or ID of Admin. Separate multiple Admins by space
* `DATABASE_URI`: [mongoDB](https://www.mongodb.com) URI. Get this value from [mongoDB](https://www.mongodb.com). For more help watch this [video](https://youtu.be/dsuTn4qV2GA)
* `DATABASE_NAME`: Name of the database in [mongoDB](https://www.mongodb.com). For more help watch this [video](https://youtu.be/dsuTn4qV2GA)

### Optional Variables
* `COLLECTION_NAME`: Name of the collections. Defaults to Telegram_files. If you going to use same database, then use different collection name for each bot
* `CACHE_TIME`: The maximum amount of time in seconds that the result of the inline query may be cached on the server
* `USE_CAPTION_FILTER`: Whether bot should use captions to improve search results. (True/False)
* `AUTH_USERS`: Username or ID of users to give access of inline search. Separate multiple users by space. Leave it empty if you don't want to restrict bot usage.
* `AUTH_CHANNEL`: Username or ID of channel. Without subscribing this channel users cannot use bot.
* `START_MSG`: Welcome message for start command.
* `INVITE_MSG`: Auth channel invitation message.
* `USERBOT_STRING_SESSION`: User bot string session.
## Admin commands
```
channel - Get basic infomation about channels
total - Show total of saved files
delete - Delete file from database
index - Index all files from channel or group
logger - Get log file
```

## Tips
* Use `index` command or run [one_time_indexer.py](one_time_indexer.py) file to save old files in the database that are not indexed yet.
* You can use `|` to separate query and file type while searching for specific type of file. For example: `Avengers | video`
* If you don't want to create a channel or group, use your chat ID / username as the channel ID. When you send a file to a bot, it will be saved in the database.

## Contributions
Contributions are welcome.

## Thanks to [Pyrogram](https://github.com/pyrogram/pyrogram)

## Support
[Movie Group](https://t.me/+9Zhp_GdQVctiNjc1) and [Support Group](https://t.me/ShadowsArena)

## License
Code released under [The GNU General Public License](LICENSE).
