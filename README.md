# doom-coding
If you're addicted to your phone and addicted to coding, let me introduce you to "Doom Coding".

Instead of doom scrolling mindlessly on social media, you can use your smartphone, computer, and Claude Code to build on-the-go!

After this 5-minute setup guide, you'll be able to code anywhere at any time.

You can code in the air!<br>
<img width="400" height="316" alt="image" src="https://github.com/user-attachments/assets/38e4c29f-9793-4700-bb99-17e368400cc4" /> <br>

You can code on a run! <br>
<img width="400" height="316" alt="image" src="https://github.com/user-attachments/assets/f5449004-0a76-44ee-9922-a5cce1423f93" /> <br>


You can code at the club! <br>
<img width="400" height="299" alt="image" src="https://github.com/user-attachments/assets/f3d05c00-a47a-4ebe-8db3-1795a6a0798c" /><br>

Anywhere you have Internet connection, you'll be able to make progress on the projects you care about. I am based in Philadelphia and was able to build an MVP from my phone while traveling in Taiwan (check out www.friendlyr.ai to help shape the future of connection!)

Thankfully for us, being on your phone 24/7 is a global cultural norm. Now we can turn our screen time into work time - happy doom coding my friends!


# What You Need
1. A Computer running 24/7 with Internet Connection
2. A Smartphone

# Overview
Use Tailscale, Termius, Claude Code, and laptop to continue building anywhere you have Internet connection.

# Getting Started

## 1. Set Up Your Computer
- Disable sleep in power settings<br>
  <img width="480" height="282" alt="image" src="https://github.com/user-attachments/assets/3305aaf1-046c-4505-89ba-2398d0601bf7" />
- Enable SSH/Remote Login<br>
  <img width="472" height="313" alt="image" src="https://github.com/user-attachments/assets/b13ee636-ecec-4962-bf83-d32adc219809" />
- Install Tailscale and sign in<br>
  <img width="400" height="506" alt="image" src="https://github.com/user-attachments/assets/f3d68264-0aa4-47a6-b7c9-2efe18bc3627" /><br>
  https://tailscale.com/download
- Install Claude Code on your laptop<br>
  https://docs.anthropic.com/en/docs/claude-code/overview

## 2. Set Up Your Phone
- Install Tailscale → Sign in with the same account<br>
  https://tailscale.com/download
- Install Termius (A Mobile Terminal Tool) <br>
  https://apps.apple.com/us/app/termius-modern-ssh-client/id549039908
- Note your MagicDNS address of your computer (e.g., my-computer.tailnet-name.ts.net)<br>
  <img width="400" height="359" alt="image" src="https://github.com/user-attachments/assets/6da3907d-ca08-48c8-9f18-54c8d644b21e" />

- Create a new host in Termius:<br>
  * Label: What you want your connection to be called
  * Hostname: Your MagicDNS address (my-computer.tailnet-name.ts.net)
  * Port: 22
  * Username/Password: Your login for your computer <br>
  <img width="400" height="320" alt="image" src="https://github.com/user-attachments/assets/5e0f0ea1-c59c-47d9-b85d-d51b4396c93d" /> <br>
  <img width="400" height="300" alt="image" src="https://github.com/user-attachments/assets/0f796605-57f2-4264-abf0-20369efdf895" />



## 3. Connect and Code
- Turn on Tailscale VPN on your phone<br>
  <img width="400" height="245" alt="image" src="https://github.com/user-attachments/assets/03646788-619b-427e-8e47-5bf8219c1c36" />
- Tap your host in Termius<br>
  <img width="400" height="370" alt="image" src="https://github.com/user-attachments/assets/18d5a03e-acf7-4069-93c2-c67d45a25183" />
- Run `claude` and start coding <br>
<img width="400" height="400" alt="image" src="https://github.com/user-attachments/assets/d92df1cd-570b-49b0-96f7-a5ce31644a6f" />

# Troubleshooting
- If you're not able to establish a connection from your phone via Termius to your computer:
## 1. Reset your Tailscale VPN
- Check your phone settings to make sure you are connected to the Tailscale VPN. <br>
<img width="400" height="227" alt="image" src="https://github.com/user-attachments/assets/1b041eff-9001-4e41-8922-c7f3bcb368da" /> <br>
- Check the Tailscale app to make sure the Tailscale VPN is on. If your phone and doom coding computer does not show a green circle for connected, there is an issue with your Tailscale/Internet connection.
<img width="400" height="517" alt="image" src="https://github.com/user-attachments/assets/e5da61ab-828d-4f40-920d-840306c284ed" />



## 2. Make sure your computer is ON and UNLOCKED
When disconnecting/reconnecting power, make sure you unlock the computer. 
# Best Practices
- Track your progress: End sessions by asking Claude to update CLAUDE.md with where you left off
- Preview websites: Go to your desired directory and start an HTTP server<br>
```
  python -m http.server 3005
```
  then visit http://your-machine.tailnet-name.ts.net:3005 in a browser on your phone<br>
  *Wherever you would use localhost:PORT to view an application, replace localhost with the machines MagicDNS from the Tailscale app (e.g. your-machine.tailnet-name.ts.net) *
- View Databases: Use the PostgreSQL app to troubleshoot databases on the go<br>
- Bookmark Supporting Sites: On your computer, bookmark the sites you refer to during development (e.g. Google OAuth, GitHub) to make it easier to reference from your phone. I use the Chrome app to seamlessly access the sites I need. 
  https://apps.apple.com/us/app/postgresql-client/id1233662353

# Happy Doom Coding!

Too much screen time is probably a bad thing - but working code is for sure better than brain rot
