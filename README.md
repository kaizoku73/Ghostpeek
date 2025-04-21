# 👻 GhostPeek

A cool domain reconnaissance tool that helps you discover tons of information about any website with just one command!

## What is GhostPeek?

GhostPeek is a Python tool I made to learn more about web domains. Give it a domain name, and it will quietly gather all sorts of interesting information:

- 🔍 Finds subdomains you didn't know existed
- ℹ️ Shows who owns the domain (WHOIS info)
- 🌐 Maps out all the DNS records
- 🖥️ Discovers what IP addresses the domain uses
- 🔧 Identifies what technologies the website is built with
- 📸 Takes screenshots of the websites
- 📊 Creates a nice HTML report you can browse

## Why I Made This

I created GhostPeek as a personal project to learn more about how websites are structured and to practice my Python skills. It combines a bunch of different tools into one simple command, saving you time when you want to check out a website's technical details.

## Installation

```bash
# Clone the repo
git clone https://github.com/kaizoku73/Ghostpeek.git
cd ghostpeek

# Install requirements
pip install -r requirements.txt
```

### Dependencies

- Python 3.6+
- requests
- dnspython
- python-whois
- rich
- selenium
- python-Wappalyzer
- setuptools

## How to Use

Simple usage:
```bash
python ghostpeek.py -d example.com
```

Or run the script and enter the domain when prompted:
```bash
python ghostpeek.py
```

### Options

```
-d, --domain    Target domain to investigate
-o, --output    Custom output directory (optional)
-t, --threads   Number of threads to use (default: 10)
--no-threading  Disable threading for sequential processing
```

## Example Output

When you run GhostPeek, you'll see something like this:

```
  ▄████  ██░ ██  ▒█████    ██████ ▄▄▄█████▓ ██▓███  ▓█████ ▓█████  ██ ▄█▀
 ██▒ ▀█▒▓██░ ██▒▒██▒  ██▒▒██    ▒ ▓  ██▒ ▓▒▓██░  ██▒▓█   ▀ ▓█   ▀  ██▄█▒ 
▒██░▄▄▄░▒██▀▀██░▒██░  ██▒░ ▓██▄   ▒ ▓██░ ▒░▓██░ ██▓▒▒███   ▒███   ▓███▄░ 
░▓█  ██▓░▓█ ░██ ▒██   ██░  ▒   ██▒░ ▓██▓ ░ ▒██▄█▓▒ ▒▒▓█  ▄ ▒▓█  ▄ ▓██ █▄ 
░▒▓███▀▒░▓█▒░██▓░ ████▓▒░▒██████▒▒  ▒██▒ ░ ▒██▒ ░  ░░▒████▒░▒████▒▒██▒ █▄
 ░▒   ▒  ▒ ░░▒░▒░ ▒░▒░▒░ ▒ ▒▓▒ ▒ ░  ▒ ░░   ▒▓▒░ ░  ░░░ ▒░ ░░░ ▒░ ░▒ ▒▒ ▓▒
  ░   ░  ▒ ░▒░ ░  ░ ▒ ▒░ ░ ░▒  ░ ░    ░    ░▒ ░      ░ ░  ░ ░ ░  ░░ ░▒ ▒░     made by kaizoku
░ ░   ░  ░  ░░ ░░ ░ ░ ▒  ░  ░  ░    ░      ░░          ░      ░   ░ ░░ ░ 
      ░  ░  ░  ░    ░ ░        ░                      ░  ░   ░  ░░  ░   

Give your desire domain: example.com

Your secrets will be stored in: recon_example.com_20250421_123456

Revealing WHOIS secrets for example.com
Domain Name      : EXAMPLE.COM
Registrar        : RESERVED-Internet Assigned Numbers Authority
Creation Date    : 1992-01-01 00:00:00
Expiration Date  : 2023-01-01 00:00:00

Hunting for subdomains of example.com
Found 3 unique domain(s)
→ example.com
→ www.example.com
→ mail.example.com

Unmasking 3 domains
Infiltrating example.com...
✓ example.com resolves to 93.184.216.34
Decoding DNS secrets for example.com...
A: 93.184.216.34
NS: a.iana-servers.net
NS: b.iana-servers.net
MX: 0 example.com.s1a1.psmtp.com

Tracing ASN network for 93.184.216.34...
ASN         : 15133
Name        : EDGECAST
Description : EDGECAST - EDGECAST CDN
RIR         : ARIN
Country     : US

Identifying technology fingerprints for example.com...
- Cloudflare
- jQuery
- Google Analytics

Capturing visual evidence of example.com (attempt 1/3)...
Loading https://example.com...
Waiting for page to stabilize...
Setting viewport to capture full page: 1200x800
Scrolling through page...
Taking screenshot...
Screenshot saved to recon_example.com_20250421_123456/screenshot_example.com.png

Mission accomplished!
Your intelligence report awaits: recon_example.com_20250421_123456/report.html
```

## The HTML Report

After GhostPeek finishes, it will automatically open an HTML report in your browser with tabs for:
- Overview with key information
- WHOIS details
- Subdomain list
- DNS records for each domain
- Technology stack
- Screenshots of all websites

## Disclaimer

This tool is meant for learning and exploring websites you have permission to scan.

## License

This project is open source, feel free to use and modify it. Just don't forget to credit me if you share it!

---

Made with ❤️ by kaizoku
