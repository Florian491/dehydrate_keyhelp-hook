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

### Change the deploy_challenge in hook.sh (line 26):

```
/usr/bin/node ~/pfad/to/dehydrated_keyhelp/src/index.js --delay 90 --domain ${1} --token ${3} --config ~/pfad/to/dehydrated_keyhelp/config/domains.yml
```

```
Example:
/usr/bin/node ~/dehydrated/dehydrated_keyhelp/src/index.js --delay 90 --domain ${1} --token ${3} --config ~/dehydrated/dehydrated_keyhelp/config/domains.yml
```

## CLI - start-dehydrated:

```
Example:
~/pfad/to/dehydrated/dehydrated --cron --domain example.com --alias example.com --challenge dns-01 --hook ~/pfad/to/dehydrated/hook.sh
or
~/pfad/to/dehydrated/dehydrated --cron --domain *.example.com --alias wildcard.example.com --challenge dns-01 --hook ~/pfad/to/dehydrated/hook.sh
```

```
Example:
dehydrated/dehydrated --cron --domain example.com --alias example.com --challenge dns-01 --hook ~/dehydrated/hook.sh
or
dehydrated/dehydrated --cron --domain *.example.com --alias wildcard.example.com --challenge dns-01 --hook ~/dehydrated/hook.sh
```

The hook.sh sends the variables (domain & token) to the node.js application (index.js).
