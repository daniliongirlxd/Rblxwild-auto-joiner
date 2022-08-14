# Rblxwild-auto-joiner

## Update v0.1:
- Pre-Alpha Release (testing)
- Version strictly for testing and after testing has finished this will no longer work

-----------------------------------------------------------------------------------------------------------------------------------------------------------------------

## Information:
- When there is a rain at [rblxwild](https://rblxwild.com) this program will join the rain and inform you of its success or failure
- **You need to be level 5+ on rblxwild**

-----------------------------------------------------------------------------------------------------------------------------------------------------------------------

## Installation:
1) First download the latest version of the program.
2) Extract the files to a foler of your choice
3) Edit the config with the help of the config guide below
4) Install [python](https://www.python.org/downloads/)
5) Now run the **"installer.bat"** file and it should start running, now you can minimise the chrome browser and the program and do some work while waiting for a notification. 
- Any problems open up a new issue on this github respitory!

-----------------------------------------------------------------------------------------------------------------------------------------------------------------------

## Notes:
- Im currently not level 5 on rblxwild so fixes may be delayed
- If you want to donate you can donate via BTC however i am not going to force you to but ngl i have $0.01 worth of btc rn lol.
- BTC Address: **3CcdeFVLHTr3b2a4oFhMswmbN1VNux6by1**
- If you have any questions, bugs or issues, make an [issuse](https://github.com/amprocode/Rblxwild-auto-joiner/issues) or join the [discord](https://discord.gg/cuUtsgMUPb)
- Enjoy!

-----------------------------------------------------------------------------------------------------------------------------------------------------------------------

## Config guide:

Default config.json file:
```json
{
  "minimum_amount": 3000,
  "browser": "chrome",
  "user_agent": "Da_agent",
  "windows_notification": true,
  "webhook_enabled": true,
  "webhook_ping": "<@1234567890987654321>",
  "webhook": "https:///discord.com/api/webhooks/xxxxxxxx/xxxxxxxxxxxxxx",
  "auth_key": "auth_token",
  "paid_captcha": false,
  "2_captcha_key": "2_captcha_key",
  "hkey": "h"
}
```
### minimum_amount:
Minimum rain amount intended for the program required to join the rain. If you dont want this and want to be notified of all rains leave it at 3000

Example: If you set it to 10000 it will only join rains that are bigger then or equal to 10000 R$

### browser:
Just put in the browser you are using, current options are:
- chromium
- opera
- edge
- firefox
- chrome

Copy and paste! This is used to get a cloudflare cookie which will help bypass some restrictions

### user_agent:
Go to [whatsmyua.info](https://www.whatsmyua.info/) and copy the user agent value

![image](https://user-images.githubusercontent.com/79641603/184401885-411205fd-e9e7-4b18-b0cf-001db6f70d00.png)

Paste this into the user_agent value

### windows_notification:
If set to "True" then a popup on the bottom right on your screen will display showing you information about the current rain

Here is an example:

![image](https://user-images.githubusercontent.com/79641603/184426126-6be3f570-5614-4c0c-b128-46dab143b8c1.png)

- A green tick indicates it joined the rain successfully.
- The red cross indicates it failed to join the rain.

### webhook_enabled:
Should be obvious but if you want the joiner to send a message to your discord webhook set it to true

### webhook_ping:
You can now ping a role or user instead of @everyone. If you need help getting an ID im sure this will help:

https://youtu.be/KVLdpboY7bg

Setting up ping:

If you want to ping **@everyone** or **@here** make sure your webhook_ping setting looks something like this:
```
"webhook_ping": "@everyone",
```
If you want to ping a **user** make sure your webhook_ping setting looks something like this:
```
"webhook_ping": "<@747719812054253568>",
```
If you want to ping a **role** just put a **&** symbol infront of the numbers. It should look something like this:
```
"webhook_ping": "<@&690632567663575090>",
```

**Obviously these are examples, replace the numbers with your own**

### webhook:
If you set webhook_enabled to true input your webhook into here to it can actually send it to you

Example of webhook:

![image](https://user-images.githubusercontent.com/79641603/184426254-68c86ad8-3d9b-4ee2-94f7-a804c518a129.png)

### auth_key:
This is your rblxwild login token, this is used to join rains.

- To get this head to [rblxwild](https://rblxwild.com).
- Next press the "F12" key on your keyboard or "CTRL + SHIFT + I"
- Now make sure "console" is selected, if not just click on it (image attached)

![image](https://user-images.githubusercontent.com/79641603/178447705-533c36c2-d3c1-4019-ab0c-8cd7770e4350.png)

- Next paste in the code below
```
copy(localStorage.getItem('authToken'))
```
- You should now have your rblxwild token copied to your clipboard, just open your config file and paste it inbetween the quotation marks.

### paid_captcha:
If you want to use 2captcha set it to true if you want to use free captcha set it to false

### 2_captcha_key:
If you are using 2 captcha put your api key in here

### hkey:
If you are using free captcha follow this.
First get the following extension for either [google](https://chrome.google.com/webstore/detail/editthiscookie/fngmhnnpilhplaeedifhccceomclgfbg) or [opera](https://addons.opera.com/en/extensions/details/edit-this-cookie) (i am sure there are other alternatives).
Next go to [h captcha signup](https://dashboard.hcaptcha.com/signup?type=accessibility) and well... signup!
Next check your email and click the confirmation link.
Next you will see a button that says **set cookie**. Click it and set your cookie.
Finally once it has been set open up the cookie extension and copy the hc_accessibility cookie (image shown below) and just paste it into your config.

**Make sure to keep note of the expiration, it normally resets every 12hrs**

![hkey](https://user-images.githubusercontent.com/79641603/184426751-c413978d-fec0-40b7-95dc-9e50543c4bb4.png)

## Current Issues:
- None
