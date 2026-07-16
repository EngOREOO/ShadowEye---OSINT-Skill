# ShadowEye — OSINT Skill

<p align="center">
  <img src="https://img.shields.io/badge/Version-1.0.0-blue?style=for-the-badge" alt="Version">
  <img src="https://img.shields.io/badge/OSINT-Expert-red?style=for-the-badge" alt="OSINT">
  <img src="https://img.shields.io/badge/Bug%20Bounty-Ready-green?style=for-the-badge" alt="Bug Bounty">
  <img src="https://img.shields.io/badge/Platform-opencode-purple?style=for-the-badge" alt="Platform">
  <img src="https://img.shields.io/badge/License-MIT-yellow?style=for-the-badge" alt="License">
</p>

<p align="center">
  <b>A powerful OSINT skill for opencode that transforms your AI into an elite intelligence gatherer.</b>
</p>

<p align="center">
  <i>See what others can't. Find what others miss.</i>
</p>

---

## What is ShadowEye?

ShadowEye is an advanced **Open Source Intelligence (OSINT)** skill designed for **bug bounty hunters** and **security researchers**. It transforms your opencode AI into a seasoned intelligence professional capable of:

- **Photo Analysis** — Extract metadata, GPS locations, camera info, and identify people
- **Reverse Image Search** — Cross-reference images across 10+ platforms
- **Social Media Discovery** — Find profiles across all major platforms
- **Username Enumeration** — Discover accounts across 400+ sites
- **Email Investigation** — Check breaches, reputation, and linked accounts
- **Domain Reconnaissance** — Map attack surfaces, find exposed assets
- **Private Program Scope Analysis** — Understand and map bug bounty targets

---

## Key Features

### Photo Intelligence
```
Input: Photo of a person
Output: Full intelligence profile
```
- EXIF metadata extraction (GPS, camera, timestamps)
- Reverse image search (Google, Yandex, TinEye, Bing)
- Face recognition and analysis
- Background object identification
- Clothing/brand detection
- Social media profile matching

### Social Media Deep Dive
- Facebook, Instagram, Twitter/X, LinkedIn, TikTok
- YouTube, Pinterest, Reddit, GitHub
- Platform-specific username enumeration
- Activity timeline reconstruction

### Domain & Infrastructure Recon
- Subdomain enumeration (Subfinder, Amass)
- DNS record analysis
- Technology fingerprinting
- Port scanning
- Exposed file detection (.env, .git, backups)
- Certificate transparency logs
- Historical data (Wayback Machine)

### Breach & Leak Analysis
- HaveIBeenPwned integration
- DeHashed searches
- IntelX intelligence
- Password leak detection

### Bug Bounty Ready
- Private program scope analysis
- Attack surface mapping
- Low-hanging fruit identification
- Report generation templates

---

## Installation

### Prerequisites
- [opencode](https://opencode.ai) installed
- Git

### Quick Install

```bash
# Clone the repository
git clone https://github.com/EngOREOO/ShadowEye---OSINT-Skill.git

# Copy to opencode skills directory
cp -r ShadowEye---OSINT-Skill ~/.agents/skills/shadoweye

# Restart opencode to load the skill
```

### Manual Install

```bash
# Create skill directory
mkdir -p ~/.agents/skills/shadoweye

# Copy SKILL.md
cp SKILL.md ~/.agents/skills/shadoweye/

# Restart opencode
```

### Verify Installation

After restarting opencode, the skill should be automatically loaded. You can verify by typing:

```
/osint
```

If the command is recognized, ShadowEye is installed correctly.

---

## Usage

### Quick Commands

| Command | Description |
|---------|-------------|
| `/osint` | Activate OSINT mode |
| `/osint photo.jpg` | Analyze a photo |
| `/osint John Doe` | Investigate a person |
| `/osint example.com` | Recon a domain |
| `/osint user@email.com` | Investigate an email |
| `/osint @username` | Search username |

### Photo Analysis

```
/osint photo.jpg
```

ShadowEye will:
1. Extract all EXIF data (GPS, camera, date)
2. Perform reverse image search on multiple platforms
3. Identify the person (if public figure)
4. Search for social media profiles
5. Check for data breaches
6. Generate a full intelligence report

### Person Investigation

```
/osint John Smith
```

ShadowEye will:
1. Search social media platforms
2. Enumerate usernames (Sherlock, Maigret)
3. Find email patterns
4. Check data breaches
5. Search public records
6. Generate a profile report

### Domain Reconnaissance

```
/osint example.com
```

ShadowEye will:
1. Enumerate subdomains
2. Analyze DNS records
3. Fingerprint technology stack
4. Scan for exposed files
5. Check certificate transparency
6. Query Wayback Machine
7. Generate a recon report

### Email Investigation

```
/osint user@example.com
```

ShadowEye will:
1. Check data breaches (HIBP)
2. Analyze email reputation
3. Find linked social accounts
4. Identify associated domains
5. Generate an investigation report

---

## Example Output

### Photo Analysis Report

```markdown
# OSINT Report: Photo Analysis

## Summary
Photo analyzed from LinkedIn profile. Subject identified as 
John Smith, Software Engineer at Tech Corp, based in San Francisco.

## Identity
- **Name:** John Smith
- **Age:** ~32 years old
- **Location:** San Francisco, CA (GPS: 37.7749° N, 122.4194° W)
- **Occupation:** Software Engineer

## Digital Footprint
### Social Media
| Platform | Username | URL |
|----------|----------|-----|
| LinkedIn | johnsmith | linkedin.com/in/johnsmith |
| GitHub | jsmith | github.com/jsmith |
| Twitter | @johnsmith_dev | twitter.com/johnsmith_dev |

## Technical Assets
- **Email:** john.smith@techcorp.com
- **GitHub Repos:** 15 public repos
- **Domains:** johnsmith.dev (personal blog)

## Risk Assessment
- **Exposure Level:** MEDIUM
- **Key Findings:** Public profile with consistent username
- **Recommendations:** Monitor for credential leaks
```

---

## Tools & Integration

ShadowEye works with these OSINT tools (install separately):

```bash
# Sherlock - Username enumeration
pip install sherlock-project

# Maigret - Extended username search
pip install maigret

# theHarvester - Email/domain recon
pip install theHarvester

# Amass - Subdomain enumeration
go install github.com/owasp-amass/amass/v4/...@master

# Subfinder - Subdomain discovery
go install -v github.com/projectdiscovery/subfinder/v2/cmd/subfinder@latest

# httpx - HTTP probing
go install -v github.com/projectdiscovery/httpx/cmd/httpx@latest

# Nuclei - Vulnerability scanning
go install -v github.com/projectdiscovery/nuclei/v3/cmd/nuclei@latest

# ExifTool - Metadata extraction
brew install exiftool
```

---

## Configuration

ShadowEye works out of the box with default settings. For advanced configuration, you can customize the skill by editing:

```bash
~/.agents/skills/shadoweye/SKILL.md
```

### Custom Platforms

Add custom social media platforms to search:

```markdown
### Additional Platforms
| Platform | URL | Notes |
|----------|-----|-------|
| CustomSite | customsite.com | Add your target |
```

### Custom Wordlists

For username enumeration, create custom wordlists:

```bash
~/.agents/skills/shadoweye/wordlists/usernames.txt
```

---

## Scope & Ethics

### In Scope
- ✅ Public information gathering
- ✅ Passive reconnaissance
- ✅ Open source intelligence
- ✅ Authorized bug bounty testing
- ✅ Security research with permission

### Out of Scope
- ❌ Unauthorized system access
- ❌ Social engineering without consent
- ❌ Private account access
- ❌ Credential stuffing
- ❌ Service disruption

### Legal Notice
ShadowEye is designed for **authorized security testing** and **bug bounty programs** only. Always obtain proper authorization before conducting any reconnaissance. The author is not responsible for misuse of this tool.

---

## Contributing

Contributions are welcome! Please follow these steps:

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

### Ideas for Contributions
- [ ] New platform integrations
- [ ] Additional OSINT tools
- [ ] Report templates
- [ ] Automation scripts
- [ ] Documentation improvements

---

## Roadmap

- [ ] v1.1 — Add Shodan integration
- [ ] v1.2 — Add Censys support
- [ ] v1.3 — Add Maltego integration
- [ ] v1.4 — Add automated reporting
- [ ] v2.0 — AI-powered face recognition
- [ ] v2.1 — Real-time monitoring
- [ ] v2.2 — Team collaboration features

---

## Support

- **Issues:** [GitHub Issues](https://github.com/EngOREOO/ShadowEye---OSINT-Skill/issues)
- **Discussions:** [GitHub Discussions](https://github.com/EngOREOO/ShadowEye---OSINT-Skill/discussions)
- **Contact:** Open an issue for questions

---

## License

This project is licensed under the MIT License — see the [LICENSE](LICENSE) file for details.

---

## Acknowledgments

- [opencode](https://opencode.ai) — The AI platform
- [Sherlock](https://github.com/sherlock-project/sherlock) — Username enumeration
- [Maigret](https://github.com/soxoj/maigret) — Extended username search
- [theHarvester](https://github.com/laramies/theHarvester) — Email recon
- [Amass](https://github.com/owasp-amass/amass) — Subdomain enumeration
- All the OSINT community for their amazing tools and research

---

<p align="center">
  <b>ShadowEye — See the unseen. Find the unfound.</b>
</p>

<p align="center">
  <img src="https://img.shields.io/github/stars/EngOREOO/ShadowEye---OSINT-Skill?style=social" alt="Stars">
  <img src="https://img.shields.io/github/forks/EngOREOO/ShadowEye---OSINT-Skill?style=social" alt="Forks">
  <img src="https://img.shields.io/github/watchers/EngOREOO/ShadowEye---OSINT-Skill?style=social" alt="Watchers">
</p>
