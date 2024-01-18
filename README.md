<p align="middle"> <h1 align="middle">Rᴇᴀᴅᴍᴇ​​​​​ ( ͡👁️ ͜ʖ ͡👁️)</h1></p>
<h1 align="middle">Iɴᴛʀᴜsɪᴏɴ Dᴇᴛᴇᴄᴛɪᴏɴ Sʏsᴛᴇᴍ - Hᴏᴍᴇ Lᴀʙ 🧑‍💻
  
# Tool:
<h2> 🐽 𝚂nort as an Intrusion Detection System 🕵️

# Machines:
<h2>  Attacker: Kali ☠️ | Victim: Metasploitable 2 👦 | IDS: Linux Mint 🍀


# Attack and Detection Scenario:
  > ## ▶️ YOUTUBE Lab Demo ⬇️


# Screenshots
> ## Snort Installation
![snort-installation](https://github.com/0xBash/IDS-Home-Lab/assets/76225821/d88398c2-fde8-48db-bc63-5991f4c96c24)
> ## Editing ipvar $HOME_NET
![config-snortconf](https://github.com/0xBash/IDS-Home-Lab/assets/76225821/000c0534-2f49-450f-a114-cea162d39fae)
> ## Custom Rules:
 ![snort-custom_rule](https://github.com/0xBash/IDS-Home-Lab/assets/76225821/a896941f-52f1-40ae-80d3-2a440e464116)


# VIM config and Snort config

## Configuring line number in VIM 
```
$ vim /root/.vimrc
```
> Line 1. set number ; Line 2. syntax on
## Snort's main config file location
```
$ sudo vim /etc/snort/snort.conf
```
## Snort's Custom rules location
```
$ sudo vim /etc/snort/rules/rules.local
```
## Custom ICMP Ping Detection Rule
```
alert ICMP any any -> $HOME_NET any (msg:"ICMP Ping Detected"; sid:100001; rev:1;)
```
## Start the Snort Detection
```
snort  -q -l /var/log/snort -i ens34 -A console -c /etc/snort/snort.conf
```
> -q for Quite-Mode (ids/ips) run ; -l for logging traffic ;
> -i for Interface ; -A for Alert-mode ; -c defines location of config file
