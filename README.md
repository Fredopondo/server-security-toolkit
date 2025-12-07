# Server Security Toolkit

Emergency security tools for Linux servers. Created after surviving a real crypto-mining attack.

## Quick Start

```bash
# Download and run scanner
curl -sSL https://raw.githubusercontent.com/maxtors-debug/server-security-toolkit/main/scan.sh | sudo bash

# Or clone and use all tools
git clone https://github.com/maxtors-debug/server-security-toolkit.git
cd server-security-toolkit
sudo ./scan.sh        # Scan for malware
sudo ./harden.sh      # Harden server security
sudo ./monitor.sh     # Start 24/7 monitoring
```

## Tools Included

| Script | Purpose |
|--------|---------|
| `scan.sh` | Detect crypto miners, backdoors, rootkits |
| `harden.sh` | Secure SSH, firewall, fail2ban setup |
| `monitor.sh` | 24/7 malware monitoring daemon |
| `cleanup.sh` | Remove known malware families |
| `audit.sh` | Full security audit report |

## What It Detects

- Crypto miners (XMRig, c3pool, cryptonight)
- Backdoors (reverse shells, unauthorized SSH)
- Credential scanners (TruffleHog, GitLeaks)
- Suspicious systemd services
- Exposed database ports (Prisma Studio, etc.)
- Unauthorized cron jobs
- Hidden processes

## Real Attack This Stopped

- **Attacker Location:** Tokyo, Japan
- **Attack Vector:** CVE-2025-55182 (React Server Components RCE)
- **CVSS Score:** 10.0 (CRITICAL)
- **Malware:** XMRig miner, rsyslo backdoor, reverse shell
- **Impact:** 100% CPU, credential theft attempt
- **Result:** Detected, removed, server hardened

### About CVE-2025-55182

A critical vulnerability in React Server Components allows unauthenticated remote code execution. Attackers can send malicious HTTP requests that, when deserialized by React, execute arbitrary code on the server.

**Affected:** Next.js, React Router, and other frameworks using React Server Components

**Fix:** Update to Next.js 15.5.7+ or 16.0.7+

More info: https://react.dev/blog/2025/12/03/critical-security-vulnerability-in-react-server-components

## License

MIT - Free to use, modify, share. Stay safe!
