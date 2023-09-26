# create_tekegram_bot
Создаем телеграмм ботов


PingMe CLI
Release Go Report Card GitHub issues License Awesome Go Dev Reference

Documentation • Supported Services • Install • Github Action • Configuration • Contributing •

About
PingMe is a personal project to satisfy my needs of having alerts, most major platforms have integration to send alerts but its not always useful, either you are stuck with one particular platform, or you have to do alot of integrations. I needed a small utility which i can just call from my backup scripts, cron jobs, CI/CD pipelines or from anywhere to send a message with particular information. And i can ship it everywhere with ease. Hence, the birth of PingMe.

Everything is configurable via environment variables, and you can simply export the logs or messages to a variable which will be sent as message, and most of all this serves as a swiss army knife sort of tool which supports multiple platforms.

Supported services
Discord
Email
Gotify
Line
Mastodon
Mattermost
Microsoft Teams
Pushbullet
Pushover
RocketChat
Slack
Telegram
Textmagic
Twillio
Zulip
Wechat
Install
MacOS & Linux Homebrew
brew install kha7iq/tap/pingme
Shell Script
By default pingme is going to be installed at /usr/bin/ sudo is requried for this operation.

If you would like to provide a custom install path you can do so as input to script. i.e ./install.sh $HOME/bin

curl -s https://raw.githubusercontent.com/kha7iq/pingme/master/install.sh | sudo sh
or

curl -sL https://bit.ly/installpm | sudo sh
Linux
AUR
# build from sources
yay -S pingme

# binary
yay -S pingme-bin
Manual
# Chose desired version, architecture & target os
export PINGME_VERSION="0.2.4"
export ARCH="x86_64"
export OS="Linux"
wget -q https://github.com/kha7iq/pingme/releases/download/v${PINGME_VERSION}/pingme_${OS}_${ARCH}.tar.gz && \
tar -xf pingme_${OS}_${ARCH}.tar.gz && \
chmod +x pingme && \
sudo mv pingme /usr/local/bin/pingme
Windows
scoop bucket add pingme https://github.com/kha7iq/scoop-bucket.git
scoop install pingme
Alternatively you can head over to release pages and download deb, rpm or binary for windows & all other supported platforms.

Docker
Docker container is also available on both dockerhub and github container registry.

latest tag will always pull the latest version available, or you can also download specific version. Checkout release page for available versions.

Docker Registry

docker pull khaliq/pingme:latest
Github Registry

docker pull ghcr.io/kha7iq/pingme:latest
Run

docker run ghcr.io/kha7iq/pingme:latest
Github Action
A github action is available for integration with your workflows, you can find it on Github Market Place or here Github Repo.

- name: PingMe-Action
  uses: kha7iq/pingme-action@v1
Usage
❯ pingme

NAME:
   PingMe - Send message to multiple platforms

USAGE:
   main [global options] command [command options] [arguments...]

DESCRIPTION:
   PingMe is a CLI tool which provides the ability to send messages or alerts to multiple
   messaging platforms and also email, everything is configurable via environment
   variables and command line switches.Currently supported platforms include Slack, Telegram,
   RocketChat, Discord, Pushover, Mattermost, Pushbullet, Microsoft Teams, Twillio, Mastodon,
   email address, Line, Gotify and Wechat.

COMMANDS:
   telegram    Send message to telegram
   rocketchat  Send message to rocketchat
   slack       Send message to slack
   discord     Send message to discord
   teams       Send message to microsoft teams
   pushover    Send message to pushover
   email       Send an email
   mattermost  Send message to mattermost
   pushbullet  Send message to pushbullet
   twillio     Send sms via twillio
   zulip       Send message to zulip
   mastodon    Set status message for mastodon
   line        Send message to line messenger
   wechat      Send message to wechat official account
   gotify      Send push notification to gotify server
   help, h     Shows a list of commands or help for one command

GLOBAL OPTIONS:
   --help, -h  show help (default: false)
Check Documentation Page for more details.

Configuration
All the flags have corresponding environment variables associated with it. You can either provide the value with flags or export to a variable.

View the Documentation Page for more details.

Contributing
Contributions, issues and feature requests are welcome!
Feel free to check issues page. You can also take a look at the contributing guide.

Acknowledgments
This project is based on amazing library Notify
