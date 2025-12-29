---
repo: hackingthemarkets/gap-trading
url: 'https://github.com/hackingthemarkets/gap-trading'
homepage: null
starredAt: '2022-08-26T20:31:58Z'
createdAt: '2022-04-20T22:24:50Z'
updatedAt: '2025-07-20T10:54:23Z'
language: Python
license: NA
branch: main
stars: 35
isPublic: true
isTemplate: false
isArchived: false
isFork: false
hasReadMe: true
refreshedAt: '2025-12-29T17:35:18.449Z'
description: null
tags: []
---

# gap-trading


## deployment on linode ubuntu

```
apt-get upgrade
timedatectl list-timezones
timedatectl set-timezone America/Los_Angeles
git clone https://github.com/hackingthemarkets/gap-trading.git
cp sample_config.py config.py
apt install python3-pip
cd gap-trading
pip3 install -r requirements.txt
```

## cron
```
crontab -e

40 6 * * 1-5 python3 /root/gap-trading/long_smallcaps.py >> /root/trade.log 2>&1
40 6 * * 1-5 python3 /root/gap-trading/short_bigtech.py >> /root/trade.log 2>&1
55 12 * * 1-5 python3 /root/gap-trading/liquidate.py >> /root/trade.log 2>&1
```
