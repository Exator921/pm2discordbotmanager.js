# pm2discordbotmanager.js
Discord bot managing script for people locally running their discord bot using pm2 and want a easy interface for reading logs and quickly controlling the bot.

<sub>This is not limited to discord bot use and will work for any pm2 instance, the main use is for discord bot's but you can use it for anything running with pm2.</sub>

## Set Up
The first things you'll need is express, socket.io, and of course pm2.
```terminal
npm install express socket.io pm2
```
> [!IMPORTANT]
> Socket.io may need admin privileges to install. If your on Mac or Linux run the install for all (or just socket.io) under sudo, if on Windows run your terminal as admin.

Once these dependices are on your system install the index.js script to your machine from this repo, there will be a few things in the script you may wanna edit and there are comments to let you know what to change and other things you'll wanna know for usage.

>[!NOTE]
>There is a note in there about a favicon (tab icon), setting this up is optional. I added it to the script cause I wanted it on my tab but if you don't want it and this section gives you errors feel free to remove the section. If you do want it the favicon file MUST be named `favicon.png` for it to work and render the image.

## Usage
With everything installed and the script set up, the only thing you need to do now is run the script with pm2.

Example use:
```terminal
pm2 start index.js --name BotMonitor -- start
```

One running the site can be accessed via your devices IP address in the url bar followed by the port.

Example:

```url
http://1.1.1.1:4000
```

>[!NOTE]
>It is highly recommended to use a secondary/local IP service such as Tailscale if you want to access this site on other devices and off the same Wi-Fi as the host device. If your only looking to use the site on the device running the bot and script this can be ignored but it is recommened and will keep things more secure. I use it in tandom with Tailscale making the site only able to be accessed by devices with Tailscale installed and signed into my Tailscale account. I can see and manage the bot from anywhere using my Tailscale IP addresses with this script.

## Example Of How The Page Will Look
<img width="1440" height="876" alt="Example of how the page will look image" src="https://github.com/user-attachments/assets/a7612751-e2dd-40cc-bd7c-f4aff13e1949" />
