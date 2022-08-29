# dehydrate_keyhelp-hook

## Download & Install

https://github.com/dehydrated-io/dehydrated

and

https://github.com/nicti/dehydrate_keyhelp

## Download - Hook

```
wget https://raw.githubusercontent.com/Florian491/dehydrate_keyhelp-hook/main/hook.sh
chmod +x hook.sh
```

### Set deploy_challenge in hook.sh:

```
/usr/bin/node ~/dehydrated/dehydrated_keyhelp/src/index.js --delay 90 --domain ${1} --token ${3} --config ~/dehydrated/dehydrated_keyhelp/config/domains.yml
```

## CMD - dehydrated

```
dehydrated/dehydrated --cron --domain example.com --alias wildcard.example.com --challenge dns-01 --hook ~/dehydrated/hook.sh

or

dehydrated/dehydrated --cron --domain *.example.com --alias wildcard.example.com --challenge dns-01 --hook ~/dehydrated/hook.sh
```
