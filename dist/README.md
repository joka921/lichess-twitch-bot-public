# lichess-twitch-bot
A bot which allows playing of chess games between a twitch host and their twitch chess

## Prerequisites

 
## How to Install

### Mac/Linux:
- NOTE: Only Python 3 is supported!
- Download the repo into lichess-bot directory
- Navigate to the directory in cmd/Terminal: `cd lichess-bot`
- Install virtualenv: `pip install virtualenv`
- Setup virtualenv:
```
virtualenv .venv -p python3 #if this fails you probably need to add Python3 to your PATH
source .venv/bin/activate
pip install -r requirements.txt
```
- Copy `config.yml.default` to `config.yml`
- Edit `config.yml`: Insert the appropriate twitch channel (e.g. #thebiggreekschach)

### Windows:
- Here is a video on how to install the bot: (https://youtu.be/w-aJFk00POQ). Or you may proceed to the next steps.
- NOTE: Only Python 3 is supported!
- If you don't have Python, you may download it here: (https://www.python.org/downloads/). When installing it, enable "add Python to PATH", then go to custom installation (this may be not necessary, but on some computers it won't work otherwise) and enable all options (especially "install for all users"), except the last . It's better to install Python in a path without spaces, like "C:\Python\".
- To type commands it's better to use PowerShell. Go to Start menu and type "PowerShell" (you may use cmd too, but sometimes it may not work).
- Then you may need to upgrade pip. Execute "python -m pip install --upgrade pip" in PowerShell.
- Download the repo into lichess-bot directory.
- Navigate to the directory in PowerShell: `cd [folder's adress]` (like "cd C:\chess\lichess-bot").
- Install virtualenv: `pip install virtualenv`.
- Setup virtualenv:
```
virtualenv .venv -p python (if this fails you probably need to add Python to your PATH)
./.venv/Scripts/activate (.\.venv\Scripts\activate should work in cmd in administator mode) (This may not work on Windows, and in this case you need to execute "Set-ExecutionPolicy RemoteSigned" first and choose "Y" there [you may need to run Powershell as administrator]. After you executed the script, change execution policy back with "Set-ExecutionPolicy Restricted" and pressing "Y")
pip install -r requirements.txt
```
- Copy `config.yml.default` to `config.yml`
- Edit `config.yml`: Insert the appropriate twitch channel (e.g. #thebiggreekschach)


## Lichess OAuth
- Create an account for your bot on [Lichess.org](https://lichess.org/signup)
- NOTE: If you have previously played games on an existing account, you will not be able to use it as a bot account
- Once your account has been created and you are logged in, [create a personal OAuth2 token](https://lichess.org/account/oauth/token/create) with the "Play as a bot" selected and add a description
- A `token` e.g. `Xb0ddNrLabc0lGK2` will be displayed. Store this in `config.yml` as the `token` field
- NOTE: You won't see this token again on Lichess.
- From the new account, follow your main account
- Set challenges of new account to "friends only" (it is crucial that there is only one active game at a time)


## Lichess Upgrade to Bot Account
**WARNING** This is irreversible. [Read more about upgrading to bot account](https://lichess.org/api#operation/botAccountUpgrade).
- run `python lichess-bot.py -u`

## Twitch oauth token
 - For any of your twitch accounts, obtain an oauth token that allows reading of chat messages
 - This does not necessarily have to be your main account, since we are only reading messages.
 - 
 
## start
- run `python lichess-bot.py`
- On lichess, using your main account, challenge your Bot account for a correspondance match (unlimited time)
- The game should show up in the UI, play your moves on lichess, and follow the onscreen instructions of this app


## To Quit
- Press CTRL+C
- It may take some time to quit


# Acknowledgements
Thanks to the Lichess team, especially T. Alexander Lystad and Thibault Duplessis for working with the LeelaChessZero
team to get this API up. Thanks to the Niklas Fiekas and his [python-chess](https://github.com/niklasf/python-chess) code which allows engine communication seamlessly.

# License
This bot is licensed under the AGPLv3 (or any later version at your option). Check out LICENSE.txt for the full text.
