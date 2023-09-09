---
title: "Hellohook"
description: "Create your own welcome bot with a custom profile picture! Set the welcome message to be regular text and/or an embed. Comes with usernames, user avatars, pings/mentions, server member counts, and leave messages. Send different welcome messsages based on the invite url! Create different 'bots' using webhooks."
cogname: "hellohook"
---

<img src="./hellohook.jpg" alt="Logo: a resting cat being scratched in the chin" class="mb-2 h-24 rounded aspect-square" />

<span class="px-3 py-1 text-xs text-white bg-green-600 rounded-full select-none">✅ Works on Red 3.5</span>

# Hellohook

<component-coghero cog="hellohook" desc="Create your own welcome bot with a custom profile picture! Set the welcome message to be regular text and/or an embed. Comes with usernames, user avatars, pings/mentions, server member counts, and leave messages. Send different welcome messsages based on the invite url! Create different 'bots' using webhooks."></component-coghero>


## Drafting your Webhook Message

### [Get started on Discohook >](https://discohook.org/?data=eyJtZXNzYWdlcyI6W3siZGF0YSI6eyJjb250ZW50IjpudWxsLCJlbWJlZHMiOlt7InRpdGxlIjoiVGl0bGUgU2FtcGxlIiwiZGVzY3JpcHRpb24iOiJEZXNjcmlwdGlvbiBTYW1wbGUiLCJjb2xvciI6MTAwNjYzNjMsImF1dGhvciI6eyJuYW1lIjoiQXV0aG9yIFNhbXBsZSJ9LCJmb290ZXIiOnsidGV4dCI6IkZvb3RlciBTYW1wbGUifSwiaW1hZ2UiOnsidXJsIjoiaHR0cHM6Ly9jZG4uZGlzY29yZGFwcC5jb20vYXR0YWNobWVudHMvODc1OTA3MTU3ODUyMjk5Mjc0Lzg3NTkwNzQ3NzIzNTk4MjM1Ni91bnNwbGFzaC5jb20tcGhvdG9zLVg0NUd5SXBqcFpjLmpwZyJ9fV19fV19)  

When you are done on Discohook:
- Scroll to the bottom
- Click "JSON Data Editor"
- Click "Copy to Clipboard"
- Paste it into the bot command

*Disclaimer: Discohook is a website that makes creating webhooks easy. Not affiliated with this cog. [Image from Unsplash.](https://unsplash.com/photos/X45GyIpjpZc)*

<br />

## Variables

> **`https://&&SERVERCOUNT&&`** for server member count (268)

> **`https://&&SERVERCOUNTORD&&`** for server member count with the th/st/nd ordinals (268th)

> **`https://&&USERAVATAR&&`** for user profile picture url

> **`https://&&USERMENTION&&`** for user mention (`<@1234567890123456>`)

- User mentions can only be used in Content, or the Embed's Body Description, or they won't appear correctly.

> **`https://&&USERNAME&&`** for username as text (`Clyde`)

> **`https://&&USERNAME1234&&`** for username#1234 as text (`Clyde#1234`)

<br />

**Adding https:// in front is required.**  
Discohook will not export the needed JSON if it says "Invalid URL" (even though the bot will make them valid at runtime), so this is a workaround.

<br />


## Examples

After you save them into the bot, when a new user joins, the variables will be replaced with the new user's info.

- [Ping a user when they join + send an embed](https://discohook.org/?data=eyJtZXNzYWdlcyI6W3siZGF0YSI6eyJjb250ZW50IjoiaHR0cHM6Ly8mJlVTRVJNRU5USU9OJiYiLCJlbWJlZHMiOlt7InRpdGxlIjoiV2VsY29tZSB0byBIZWxsb2hvb2sgOikiLCJkZXNjcmlwdGlvbiI6IkxvcmVtIGlwc3VtIGRvbG9yIHNpdCBhbWV0LCBjb25zZWN0ZXR1ciBhZGlwaXNjaW5nIGVsaXQsIHNlZCBkbyBlaXVzbW9kIHRlbXBvciBpbmNpZGlkdW50IHV0IGxhYm9yZSBldCBkb2xvcmUgbWFnbmEgYWxpcXVhLiIsImNvbG9yIjoxNDUwMDY3NSwidGh1bWJuYWlsIjp7InVybCI6Imh0dHBzOi8vJiZVU0VSQVZBVEFSJiYifX1dfX1dfQ)  
![Discohook example](https://cdn.discordapp.com/attachments/875907157852299274/934225213393076224/Screenshot_2022-01-21_at_15-17-00_Discohook.png)

<br />

## Why?

Life was once peaceful in the land of Cats. As the land grew, the Cats community decided to run its own bot, named the Cat Lord. The Cat Lord welcomed every cat that passed through its gates.

Then, one day, the land of Dogs found the Cat Lord a very helpful bot. However, the Dogs were not large enough yet to justify running its own bot. Yet, it would be a bad idea all the same to welcome new dogs with a bot named "The Cat Lord".

An agreement was made, and Hellohook was born.

Despite being a single bot, the welcome messages can finally be unique between both lands.

The Cat Lord lives on. The Dog Lord is born.

All live in harmony forevermore.

<br />

## FAQ

### **Hellohook and the test command doesn't send anything!**

First, check your Red Bot console.

#### No module named

As of Red 3.5, you may have run into an error `No module named requests`. Shut down your Red bot, then run `pip install requests` before `redbot #####` to start it back up.

For any other module/package, run `pip install PACKAGENAMEHERE`.

Afterwards, re-set your hellohook greet/leave message (even with no changes) to force an update.

As of 17 August 2023, this has been patched, but may happen again in the future, and with different modules/packages. If it does, please let me know in the [Support Discord](/discord) or file a GitHub bug report.

#### send() got an unexpected keyword argument

If it says `send() got an unexpected keyword argument '####'`, please let me know in the [Support Discord](/discord) or file a GitHub bug report.

As of 10 June 2022, this has been patched, but may happen again in the future.

<br />

### **How do I send a webhook styled as the person who joined?**

This feature is not recommended. Hellohook does not officially support this feature, since it may be against Discord's ToS.

But, Hellohook is open-source, so you are free to customize the bot by [forking the code](#forking-hellohook).

In the code, find the marker MM101, and add the code below:

```
            # (MM101) Add custom parameters here
            greetMessageJson["username"] = userObj.display_name
            greetMessageJson["avatar_url"] = userObj.display_avatar.url
```

<br />

## Forking Hellohook

<component-cogfork cog="hellohook"></component-cogfork>
<br /><br />

## Install

### Step 1: Download

Clone or download this project.

### Step 2: Add your Discord Bot info

Copy `.env.example` to `.env`, then:
- Add your bot's token to `dpy_token`
- Add your bot's User ID to `dpy_user_id`

The bot prefix is @ping or Slash command.

### Step 3: Run the Bot

Setup a [venv](https://docs.python.org/3/library/venv.html) using Python >=3.9 and install requirements

```
python3.9 -m venv ~/dpyenv
source ~/dpyenv/bin/activate
pip install -r requirements.txt
```

In the future, you can run your bot anytime using
```
source ~/dpyenv/bin/activate
python3 -m main
```


## Support

[Join the Discord >](https://coffeebank.github.io/discord)
