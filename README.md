# Chrony Zabbix Monitoring Template

**This template is based on https://github.com/zabbix/community-templates/blob/main/Applications/NTP/template_chrony_accuracy/6.0/template_chrony_accuracy.yaml**

Works for Zabbix 7.x Active Agent

## Deploy Commands

Everything is executed by only a few basic deploy scripts. 

```bash
cd /usr/local/src
git clone https://github.com/Futur-Tech/futur-tech-zabbix-chrony.git
cd futur-tech-zabbix-chrony

./deploy.sh 
# Main deploy script

./deploy-update.sh -b main
# This script will automatically pull the latest version of the branch ("main" in the example) and relaunch itself if a new version is found. Then it will run deploy.sh. Also note that any additional arguments given to this script will be passed to the deploy.sh script.
```

Finally import the template in Zabbix Server and attach it to your host.