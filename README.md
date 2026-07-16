# ShadowEye — Elite OSINT Intelligence Engine

<p align="center">
  <img src="https://img.shields.io/badge/Version-2.0.0-blue?style=for-the-badge" alt="Version">
  <img src="https://img.shields.io/badge/OSINT-Elite-red?style=for-the-badge" alt="OSINT">
  <img src="https://img.shields.io/badge/Auto-Execute-brightgreen?style=for-the-badge" alt="Auto-Execute">
  <img src="https://img.shields.io/badge/Platforms-50+-orange?style=for-the-badge" alt="Platforms">
  <img src="https://img.shields.io/badge/Bug%20Bounty-Ready-green?style=for-the-badge" alt="Bug Bounty">
  <img src="https://img.shields.io/badge/Platform-opencode-purple?style=for-the-badge" alt="Platform">
  <img src="https://img.shields.io/badge/License-MIT-yellow?style=for-the-badge" alt="License">
</p>

<p align="center">
  <b>全自动 OSINT intelligence engine that automatically searches 50+ platforms when given a photo or name.</b>
</p>

<p align="center">
  <i>See the unseen. Find the unfound. Know the unknown.</i>
</p>

---

## What is ShadowEye?

ShadowEye is an **elite OSINT intelligence engine** designed for **bug bounty hunters** and **security researchers**. It transforms your opencode AI into a **全自动 intelligence professional** that:

- **Auto-Executes** — No confirmation needed, just works
- **Searches 50+ Platforms** — Covers all major social media and OSINT sources
- **Runs in Parallel** — Multiple searches simultaneously
- **Generates Full Reports** — Professional, organized, actionable
- **Works Instantly** — Photo or name → Full intelligence report

### Key Capabilities

| Capability | Description | Platforms |
|------------|-------------|-----------|
| **Photo Analysis** | Extract metadata, GPS, camera info | EXIF, Google, Yandex, TinEye |
| **Face Recognition** | Identify people from photos | PimEyes, FaceCheck, SocialCatfish |
| **Social Media Sweep** | Find all profiles | Facebook, Instagram, Twitter, LinkedIn, TikTok, YouTube, Reddit, Pinterest, Snapchat |
| **Username Enumeration** | Discover accounts across 400+ sites | Sherlock, Maigret, Namechk, KnowEm |
| **Email Investigation** | Find emails, check breaches | Hunter.io, HIBP, DeHashed, IntelX |
| **Phone Discovery** | Find phone numbers | Truecaller, Sync.me, WhitePages |
| **Domain Recon** | Map attack surfaces | Subfinder, Amass, Shodan, Censys |
| **Breach Check** | Find leaked data | HIBP, BreachDirectory, Leaked.site |

---

## Installation

### Prerequisites
- [opencode](https://opencode.ai) installed
- Git
- Python 3.x (for some tools)

### Quick Install (Recommended)

```bash
# Clone the repository
git clone https://github.com/EngOREOO/ShadowEye---OSINT-Skill.git

# Copy to opencode skills directory
cp -r ShadowEye---OSINT-Skill ~/.agents/skills/shadoweye

# Install optional tools (recommended for full power)
pip install sherlock-project maigret theHarvester

# Restart opencode to load the skill
```

### Manual Install

```bash
# Create skill directory
mkdir -p ~/.agents/skills/shadoweye

# Copy files
cp SKILL.md ~/.agents/skills/shadoweye/
cp README.md ~/.agents/skills/shadoweye/
cp LICENSE ~/.agents/skills/shadoweye/

# Restart opencode
```

### Verify Installation

After restarting opencode, the skill should be automatically loaded. Test by:

1. Sending a photo to the AI
2. Typing a person's name
3. Asking "who is this person?"

If ShadowEye starts searching automatically, it's working correctly.

### Optional Tools Installation

For maximum power, install these tools:

```bash
# Username enumeration
pip install sherlock-project
pip install maigret

# Email/domain recon
pip install theHarvester

# Subdomain enumeration
go install -v github.com/projectdiscovery/subfinder/v2/cmd/subfinder@latest
go install github.com/owasp-amass/amass/v4/...@master

# HTTP probing
go install -v github.com/projectdiscovery/httpx/cmd/httpx@latest

# Metadata extraction
brew install exiftool
```

---

## Usage

### How It Works — Fully Automatic

**Just provide input → ShadowEye does everything automatically:**

```
User: [sends photo]
ShadowEye: [automatically runs full OSINT pipeline]
ShadowEye: [presents complete intelligence report]
```

**No commands needed. No confirmation needed. Just works.**

### Input Types → Auto-Actions

| Input Type | What Happens Automatically |
|------------|---------------------------|
| **Photo** | EXIF extraction → Reverse image search → Face recognition → Social media sweep → Username enumeration → Email discovery → Full report |
| **Person Name** | Name search → Username enumeration → Email discovery → Social media sweep → Breach check → Full report |
| **Email** | Breach check → Email reputation → Linked accounts → Social profiles → Full report |
| **Username** | Username enumeration across 400+ platforms → Full report |
| **Domain** | Subdomain enumeration → DNS analysis → Tech stack → Exposed files → Full report |
| **Phone** | Phone lookup → Social profiles → Breach check → Full report |

### Example: Photo Analysis

**Input:**
```
[User uploads photo of a person]
```

**Auto-Execution (happens automatically):**
1. ✅ Extract EXIF metadata (GPS, camera, timestamp)
2. ✅ Reverse image search on Google, Yandex, TinEye, Bing
3. ✅ Face recognition on PimEyes, FaceCheck
4. ✅ Generate name variations
5. ✅ Search Facebook, Instagram, Twitter, LinkedIn, TikTok
6. ✅ Enumerate usernames on 400+ sites
7. ✅ Search for email patterns
8. ✅ Check data breaches
9. ✅ Generate complete intelligence report

**Output:**
```markdown
# ShadowEye Intelligence Report

## Target: John Smith
**Generated:** 2026-07-16 04:45:00
**Confidence:** HIGH (8/10)

---

## IDENTITY
| Field | Value | Source |
|-------|-------|--------|
| Full Name | John Smith | Face recognition |
| Age | ~32 | Photo analysis |
| Location | San Francisco, CA | GPS metadata |
| Occupation | Software Engineer | LinkedIn |

## SOCIAL MEDIA ACCOUNTS
| Platform | Username | URL | Verified |
|----------|----------|-----|----------|
| Facebook | john.smith | facebook.com/john.smith | ✅ |
| Instagram | @johnsmith_dev | instagram.com/johnsmith_dev | ✅ |
| Twitter | @johnsmith | twitter.com/johnsmith | ✅ |
| LinkedIn | johnsmith | linkedin.com/in/johnsmith | ✅ |
| GitHub | jsmith | github.com/jsmith | ✅ |

## EMAILS FOUND
| Email | Source | Breach? |
|-------|--------|---------|
| john.smith@gmail.com | Hunter.io | ⚠️ Yes |
| jsmith@techcorp.com | LinkedIn | No |

## CONFIDENCE SCORE: 8/10
## RISK LEVEL: MEDIUM
```

---

## Example Output

### Photo Analysis Report

```markdown
# ShadowEye Intelligence Report

## Target: Photo Analysis
**Generated:** 2026-07-16 04:45:00
**Confidence:** HIGH (9/10)

---

## PHOTO METADATA
| Field | Value |
|-------|-------|
| Camera | iPhone 15 Pro Max |
| GPS | 40.7128° N, 74.0060° W (New York, NY) |
| Date | 2026-07-15 14:32:15 |
| Software | Adobe Photoshop 25.0 |
| Owner | Not embedded |

## FACE ANALYSIS
| Attribute | Value |
|-----------|-------|
| Name | Sarah Johnson (92% confidence) |
| Age | ~28 years old |
| Gender | Female |
| Ethnicity | Caucasian |
| Hair | Brown, long |
| Glasses | Yes, prescription |
| Distinguishing | Small tattoo on left wrist |

## CONTEXT CLUES
| Item | Details |
|------|---------|
| Background | Manhattan skyline, likely rooftop |
| Clothing | Nike athletic wear |
| Watch | Apple Watch Series 9 |
| Phone | iPhone 15 Pro (visible in reflection) |

## SOCIAL MEDIA ACCOUNTS
| Platform | Username | URL | Confidence |
|----------|----------|-----|------------|
| Facebook | sarah.johnson | facebook.com/sarah.johnson | HIGH |
| Instagram | @sarahj_nyc | instagram.com/sarahj_nyc | HIGH |
| LinkedIn | sarahjohnson | linkedin.com/in/sarahjohnson | HIGH |
| Twitter | @sarahjohnson | twitter.com/sarahjohnson | MEDIUM |
| TikTok | @sarahj | tiktok.com/@sarahj | HIGH |

## EMAILS FOUND
| Email | Source | Breach? |
|-------|--------|---------|
| sarah.johnson@gmail.com | Hunter.io | ⚠️ Yes (2023) |
| sjohnson@techcorp.com | LinkedIn | No |

## DATA BREACHES
| Service | Date | Data Exposed |
|---------|------|--------------|
| LinkedIn | 2023 | Email, password hash |
| Adobe | 2013 | Email, password hint |

## CONFIDENCE SCORE: 9/10
## RISK LEVEL: MEDIUM
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
