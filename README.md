# NGINX-Reverse-Proxy-Generator
On daily basis I need to configure reverse proxy using nginx. Now it feels like a boring task to me. So I automate the entire process using bash. So now I can configure reverse proxy with SSL less than a minutes. It makes my life more eaiser now.
🔰 Badges
<p align="left"> <img src="https://img.shields.io/badge/status-active-brightgreen?style=for-the-badge" /> <img src="https://img.shields.io/badge/nginx-supported-blue?style=for-the-badge&logo=nginx&logoColor=white" /> <img src="https://img.shields.io/badge/docker-friendly-2496ED?style=for-the-badge&logo=docker&logoColor=white" /> <img src="https://img.shields.io/badge/bash-script-yellow?style=for-the-badge&logo=gnubash&logoColor=black" /> <img src="https://img.shields.io/badge/ssl-automatic-green?style=for-the-badge&logo=letsencrypt" /> </p>

 🟦 **Overview**


Managing multiple applications enpoints means one recurring headache:
creating Nginx reverse proxies again and again.

```
New domain

New port

New container

New config

Test → Reload → SSL

Fix path issues

Websocket upgrade

Header forwarding

Error debugging
```

🕒 Manual time: 10–15 minutes per service
⚡ With this tool: < 1 mins

This wizard automatically builds production-grade reverse proxy configs safely and interactively.

🚀 **Features**
💠 **Interactive CLI Wizard**

Prompts only what’s needed:

Domain

Upstream host (default: 127.0.0.1)

Port (Docker app port)

Optional / → /s redirect

Optional dedicated access logs

SSL (Let’s Encrypt)

💠 **Production-Ready Nginx Config**
```
WebSockets

HTTP/1.1 keep-alive

Proxy timeouts

Correct headers

Buffer tuning

Health check endpoint

Zero-downtime reload
```

💠**Bulletproof Error Handling**
```
Nginx config test before reload

Auto-backup existing configs

Upstream reachability test

Clean inline warnings

No accidental overwrite

No impact to other websites
```

💠**Full SSL Automation**

With:
```
certbot --nginx

Supports:

domain.com

www.domain.com
```
🛠 **Installation**

**Create script:**
```
sudo nano /usr/local/bin/rahul-revproxy
```

Paste the script from this repository.

### Make executable:
```
sudo chmod +x /usr/local/bin/revproxy.sh
```

Run:
```
./revproxy.sh
```
📦 **Example Usage**
```
Enter domain: api.example.com
Use default upstream host 127.0.0.1? y
Enter port: 3052
Redirect / to /s? y
Enable dedicated logs? y
Enable SSL? y
```

🎉**Reverse Proxy + SSL ready instantly.**

🩻 Health Check Endpoint Added

### Each generated config includes:
```
/_nginx_health → OK - served by nginx for <your-domain>
```
<p align="center">
  <img src="images/screenshot.png" width="500">
</p>

### Great for:

Monitoring

ALB/ELB Health Checks

Automated uptime tools

🧩**Why This Exists**

When managing 10–50 Docker services —
reverse proxies become a time-consuming repetitive chore.

This tool:

Saves time

Prevents mistakes

Ensures consistency

Gives production-safe configs

Works for ANY stack

## Thanks for you time.
