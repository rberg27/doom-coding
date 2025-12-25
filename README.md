# doom-coding
Tired of Doom Scrolling? Replace one addiction with the marginally healthier addiction of Doom Coding. Here's a 5-minute guide for how to smartphone to code anywhere at anytime.

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
- Install Termius<br>
  https://apps.apple.com/us/app/termius-modern-ssh-client/id549039908
- Note your MagicDNS address of your computer (e.g., my-computer.tailnet-name.ts.net)<br>
  <img width="400" height="365" alt="image" src="https://github.com/user-attachments/assets/39e3d25a-167b-466d-8113-a9d3c6abe450" />
- Create a new host in Termius:<br>
  * Label: What you want your connection to be called
  * Hostname: Your MagicDNS address (my-computer.tailnet-name.ts.net)
  * Port: 22
  * Username/Password: Your login for your computer <br>
  <img width="400" height="245" alt="image" src="https://github.com/user-attachments/assets/5e0f0ea1-c59c-47d9-b85d-d51b4396c93d" /> <br>
  <img width="400" height="245" alt="image" src="https://github.com/user-attachments/assets/0f796605-57f2-4264-abf0-20369efdf895" />



## 3. Connect and Code
- Turn on Tailscale VPN on your phone<br>
  <img width="400" height="245" alt="image" src="https://github.com/user-attachments/assets/03646788-619b-427e-8e47-5bf8219c1c36" />
- Tap your host in Termius<br>
  <img width="400" height="370" alt="image" src="https://github.com/user-attachments/assets/18d5a03e-acf7-4069-93c2-c67d45a25183" />
- Run `claude` and start coding <br>
<img width="400" height="370" alt="image" src="https://github.com/user-attachments/assets/d92df1cd-570b-49b0-96f7-a5ce31644a6f" />

# Doom Coding Best Practices
- Track your progress: End sessions by asking Claude to update CLAUDE.md with where you left off
- Preview websites: Go to your desired directory and start an HTTP server<br>
```
  python -m http.server 3005
```
  then visit http://your-machine.tailnet-name.ts.net:3005 in a browser on your phone<br>
  *Wherever you would use localhost:PORT to view an application, replace localhost with your-machine.tailnet-name.ts.net*
- View Databases: Use the PostgreSQL app to troubleshoot databases on the go<br>
  https://apps.apple.com/us/app/postgresql-client/id1233662353
