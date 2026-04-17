# Splunk BOTSv3 Training - MLATech Edition (2026)

![Visitors](https://api.visitorbadge.io/api/visitors?path=https%3A%2F%2Fgithub.com%2FMohammadLotfiA%2Fmlatech-splunk-training&labelColor=%23dce775&countColor=%23263759)

**Premium Splunk training for absolute beginners using the BOTSv3 dataset. Every SPL command is verified, corrected, and beginner-friendly. Interactive HTML with quizzes, labs, and CTF challenges.**

[

## 🚀 Features

- **Zero-to-Hero Splunk Training** - Install, data ingestion, SPL mastery, hunting
- **Interactive HTML App** - No server needed, works offline, mobile-friendly
- **15 Generic Hunt Drills** - Beginner data exploration exercises
- **15 BOTSv3 CTF Challenges** - Verified SPL commands with hints & solutions
- **Live Lab Instructions** - Kali + Metasploitable2 + Splunk Enterprise
- **Every SPL Command Verified** - Fixed against real BOTSv3 dataset
- **Quizzes & Knowledge Checks** - Interactive learning validation
- **Glassmorphism UI** - Premium 2026 design, TailwindCSS + React

## 📋 Prerequisites

- **Splunk Enterprise** (free Developer License recommended)
- **BOTSv3 Dataset** (download from official Splunk GitHub)
- **Modern browser** (Chrome, Firefox, Safari, Edge)
- **Optional**: VirtualBox + Kali Linux + Metasploitable2 for live labs

## 🎯 Quick Start

1. **Download & Open**
   ```bash
   git clone https://github.com/MohammadLotfiA/mlatech-splunk-training.git
   # Or just download index.html
   ```

2. **Open in Browser**
   ```
   Open index.html in any modern browser
   ```

3. **Follow the Tabs** (1-10)
   - Tab 1: Install Splunk Enterprise
   - Tab 2: Import BOTSv3 dataset  
   - Tab 3: Learn SPL (10 essential commands)
   - Tab 4: Generic hunt drills
   - Tab 5: BOTSv3 CTF challenges
   - Tab 6+: Live labs & advanced topics

## 🛠️ What Makes This Different

✅ **Every SPL command tested against real BOTSv3 data**  
✅ **Fixed sourcetype casing** (WinHostMon, PerfmonMk:Process, etc.)  
✅ **Correct field names** (OS → operatingSystem, site not uri_domain)  
✅ **Chronological accuracy** (`sort + _time | head 1` not `stats first()`)  
✅ **Beginner-first approach** - No assumptions, clear error explanations  
✅ **Production-ready labs** - Kali + Metasploitable2 + syslog forwarding  

❌ **No more "no results" frustration** - Every search returns data  
❌ **No fake placeholder flags** - Real BOTSv3 answers from verified writeups  
❌ **No broken field extractions** - Exact field names from the dataset  

## 📊 BOTSv3 Dataset

Download from official source:
```
https://github.com/splunk/botsv3
```

**Import Instructions** (Tab 2 covers both methods):
1. **Extract & Copy** → `C:\Program Files\Splunk\etc\apps\botsv3_data_set`
2. **OR Web Upload** → Settings → Add Data → Upload → Create `botsv3` index

**Verify**: `index=botsv3 earliest=0 | head 5`

## 🎮 Live Labs Setup

```
┌─────────────────┐    ┌──────────────────┐    ┌─────────────────┐
│ Windows + Splunk │◄──►│ Kali Linux (Att) │◄──►│ Metasploitable2 │
│   (Host-Only)   │    │  (Host-Only)     │    │   (Host-Only)   │
└─────────────────┘    └──────────────────┘    └─────────────────┘
```

**Network**: VirtualBox Host-Only Adapter (`192.168.56.0/24`)  
**Splunk Input**: UDP 514 syslog → `index=lab_data`  
**Attacks**: Hydra, Nmap, Nikto → Live Splunk detection

## 📖 Content Roadmap

```
Tab 1: Splunk 101 & Install (Windows MSI + Developer License)
Tab 2: BOTSv3 Data Import (2 methods, troubleshooting)
Tab 3: SPL For Noobs (table, stats, top, sort, head, etc.)
Tab 4: Generic Hunt Drills (15 beginner exercises)
Tab 5: BOTSv3 CTF (15 verified challenges)
Tab 6: Lab Infrastructure (Kali + Metasploitable2)
Tab 7: Simulation Wing (5 live attack labs)
Tab 8: Field Extractions (rex, permanent fields)
Tab 9: Advanced Alerts (3 detection rules)
Tab 10: Dashboards & Vis (4-panel SOC dashboard)
```

## 🔧 Development

Single HTML file - no build step needed.

```bash
# Edit the single file
index.html
# React + TailwindCSS + Babel standalone
# Deploy anywhere
```

## 🐛 Troubleshooting

**"No results from SPL"**
```
1. Set time picker to "All time"
2. Verify: index=botsv3 earliest=0 | head 20
3. Check sourcetype casing (WinHostMon ≠ winhostmon)
4. Copy-paste SPL exactly
```

**BOTSv3 import failed**
```
1. Use Developer License (10GB/day)
2. Create dedicated "botsv3" index
3. Extract .tgz first, then upload
4. Restart Splunk after import
```