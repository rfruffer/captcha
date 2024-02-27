Fork is abandoned.
The fake button is rarely used, making the feature largely pointless. Additionally, the fork contains a bug preventing captcha from displaying for some users.

Telegram Captcha Bot
Telegram bot that validates new users that enter supergroup. Validation works like a simple captcha. Bot written in Go (Golang).

This bot has been tested on several supergroups (2000+ people) for a long time and has shown its effectiveness against spammers.

Fork information
Two fake buttons have been added, pressing on which the user gets banned.
Randomization of the button order. The original button for allowing access to the chat will never be the first in the list.
If print_success_and_fail_messages_strategy = "del" is selected in the configuration, the message about the user entering the chat is also deleted.
The user's first name (not @username) has been added to the welcome message.
Added the ability to disable and enable the bot for administrators using the /capcha command
Attack mode. In this mode, all new chat participants receive a temporary 5-minute ban. This command is useful during a mass invasion of spammers in the chat.
Added CAS antispam protection.
20230428141709

Cloud hosted instance of the bot
@gate_troitsk_bot - fork rus @CaptchaFakeBot - fork global

@cloud_tg_captcha_bot - original

How it works
Add the bot to your supergroup
Promote the bot for administrator privileges
A new user enters your supergroup
Bot restricts the user's ability to send messages
Bot shows a welcome message and a captcha button to the user
If the user doesn't press the button within 30 seconds then the user is banned by the bot
If you want to run your own instance of the bot
Option 1 (the easiest one): docker-compose + already built docker container
Option 2: docker-compose + build your own docker container
Option 3: systemd
Commands
/healthz - check that the bot is working correctly

/captcha - enable/disable captcha when joining the chat.

/attack - activate/deactivate attack mode.

In this mode, all new chat participants receive a temporary 5-minute ban. This command is useful during a mass invasion of spammers in the chat.

Сustomization
You can change several bot's settings (welcome message, ban duration, socks5 proxy server) through the configuration file config.toml

Alternatives / Forks
momai/tg-captcha-bot - fork of tg-captcha-bot with interesting additional features.
