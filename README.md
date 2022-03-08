
# Telegram to Discord Message Bot — Forward Telegram Messages to Discord 

### Dependencies

1. Python 3.6+ 
2. [Anaconda Python Console](https://www.anaconda.com/products/individual) (Optional, makes pip install debugging go away)
3. Create you own discord bot, add it to your server and retrive token. Follow Steps [here](https://www.writebots.com/discord-bot-token/).
4. Have a Telegram account with valid phone number


### Installing and Setup
1. Clone this repository
2. Open your choice of console (or Anaconda console) and navigate to cloned folder 
3. Run Command: `python3 -m pip install -r requirements.txt`.
4. Fill out a configuration file. An exmaple file can be found at `config.yml-sample`. 


### First Run and Usage

1. Change the name of `config.yml-sample` to `config.yml`

#### Filling `config.yml` file

* Create a two channels on Telegram as `channel_send` and `channel_recieve` and fill in their channel ids in config.yml
* Add your Telegram `api_id` and `api_hash` to config.yml | Read more [here](https://core.telegram.org/api/obtaining_api_id)
* Add your `discord_bot_token` to config.yml | Read more [here](https://www.writebots.com/discord-bot-token/)
* Add your `discord_1_channel` channel id. Remember when you remove extra discord channels you have to update code in `discord_messager.py` under comment `DISCORD SERVER START EVENT` and `MESSAGE SCREENER`

#### Editing `discord_messager.py`

* Whenever you add and delete discord channels in `config.yml`; `discord_messager.py` will have to be updated. If you know basic python you will understand the code.
* Multiple send/recieve telegram channels in `config.yml` can added without any code change.

2. Read the Version History and Changelog and below before running the script.

3. Run the command `python3 forwardgram.py config.yaml`

```
***PLEASE NOTE:  In the first time initializing the script, you will be requried to validate your phone number using telegram API. This happens only at the first time (per session name).
```


