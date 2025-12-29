---
repo: maxim-avramenko/monitoring
url: 'https://github.com/maxim-avramenko/monitoring'
homepage: ''
starredAt: '2023-12-19T22:20:58Z'
createdAt: '2018-12-28T00:38:05Z'
updatedAt: '2025-06-18T17:16:31Z'
language: Lua
license: NA
branch: master
stars: 11
isPublic: true
isTemplate: false
isArchived: false
isFork: false
hasReadMe: true
refreshedAt: '2025-12-29T17:34:51.712Z'
description: >-
  grafana, prometheus, alertmanager, node-exporter, cadvisor, alertmanager-bot
  for telegram in docker-compose and awesome grafana dashbord
tags:
  - alertmanager
  - alertmanager-bot-telegram
  - bash
  - cadvisor
  - docker-compose
  - grafana
  - node-exporter
  - prometheus
---

Monitoring for node and docker containers
=

Repository contains a docker container composition to set up and run monitoring service based on:
```markdown
1) prometheus
2) node-exporter
3) cadvisor
4) alertmanager
5) alertmanager-bot (send alerts to telegram chat)
6) grafana (with awesome dashbord)
```

To init and run monitoring on your host use command:
```shell
git clone https://github.com/maxim-avramenko/monitoring.git \
&& cd monitoring \
&& ./init site.localhost
```
Monitoring service list (add this domain name list to your /etc/hosts):
```markdown
1) grafana.site.localhost
2) node-exporter.site.localhost
3) prometheus.site.localhost
4) alertmanager.site.localhost
5) alertmanager-bot.site.localhost
6) cadvisor.site.localhost
```

You can change domain name with ./init your-domain.name.com but don't forget to stop monitoring and remove all docker volumes
```shell
docker-compose down -v \
&& ./init my-domain.name.com
```
After reinitialisation you must add domain names to your system /etc/hosts
```markdown
1) grafana.my-domain.name.com
2) node-exporter.my-domain.name.com
3) prometheus.my-domain.name.com
4) alertmanager.my-domain.name.com
5) alertmanager-bot.my-domain.name.com
6) cadvisor.my-domain.name.com
```
