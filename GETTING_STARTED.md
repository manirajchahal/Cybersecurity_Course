# Getting Started with SHU Cybersecurity Club

Welcome! This guide will help you get set up and ready for your cybersecurity learning journey.

## 📋 Prerequisites

### Required
- A computer (Windows, Mac, or Linux)
- Internet connection
- Basic computer skills (file management, installing software)

### Recommended
- At least 8GB RAM (for running virtual machines)
- 50GB free disk space
- Administrative access to your computer

## 🚀 Quick Start (5 minutes)

### Step 1: Get the Course Materials
```bash
# Install Git if you don't have it
# Download from: https://git-scm.com/downloads

# Clone this repository
git clone https://github.com/manirajchahal/Cybersecurity_Course.git

# Navigate to the repository
cd Cybersecurity_Course

# View available weeks
ls
```

### Step 2: Join the Community
- Join our Discord/Slack: [Add your own community]
- Introduce yourself in the #introductions channel
- Check the #announcements for weekly updates

### Step 3: Start Learning
```bash
# Navigate to Week 1
cd Week1

# Read the overview
cat README.md

# Open the first lab
# Use your favorite text editor or markdown viewer
```

## 🔧 Environment Setup

### Option 1: Beginner-Friendly (Recommended for Weeks 1-3)

**For Windows Users:**
1. Install [Git Bash](https://git-scm.com/downloads) for Linux commands
2. Use [Windows Terminal](https://apps.microsoft.com/store/detail/windows-terminal/9N0DX20HK701) if not installed already
3. Install [Python 3](https://www.python.org/downloads/)
4. Install [VS Code](https://code.visualstudio.com/) as your editor

**For Mac Users:**
1. Open Terminal (built-in)
2. Install [Homebrew](https://brew.sh/): `/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"`
3. Install Python: `brew install python3`
4. Install VS Code: `brew install --cask visual-studio-code`

**For Linux Users:**
You're all set! Just make sure you have Python 3:
```bash
sudo apt update
sudo apt install python3 python3-pip
```

### Option 2: Virtual Machine (Recommended from Week 2+)

**Why use a VM?**
- Safe isolated environment for security testing
- Pre-configured security tools
- Easy to reset if something breaks
- Industry standard practice

**Setup Instructions (Windows):**

1. **Install VirtualBox** (free)
   - Download: https://www.virtualbox.org/wiki/Downloads
   - Install for your operating system

2. **Download Kali Linux** (security-focused Linux distribution)
   - Get the VirtualBox image: https://www.kali.org/get-kali/#kali-virtual-machines
   - Download the `.ova` file (pre-built VM)

3. **Import to VirtualBox**
   - Open VirtualBox
   - File → Import Appliance
   - Select downloaded `.ova` file
   - Click Import and wait

4. **Start Your VM**
   - Select Kali Linux VM
   - Click Start
   - Default credentials: `kali` / `kali`


**Setup Instructions (Mac):**

1. **Install UTM** (free)
   - Download: https://www.virtualbox.org/wiki/Downloads
   - Install for your operating system

2. **Download Kali Linux** (security-focused Linux distribution)
   - Get the .iso image: [https://www.kali.org/get-kali/#kali-virtual-machines](https://www.kali.org/get-kali/#kali-installer-images) under "Apple Silicon (ARM64)"
   - Download the `.iso` file (Kali Installer)

3. **Import to UTM**
   - Open UTM → “Create a New Virtual Machine”
   - Choose Virtualize (important! Only use Emulate if you’re running an x86 ISO on an ARM Mac)
   - Select Linux
   - When it asks for an installer image, select the Kali ARM64 .iso you downloaded
   - Allocate CPU, RAM, and disk space
   - Boot → the Kali installer will run normally

4. **Start Your VM**
   - Select Kali Linux VM
   - Click Start
   - Enter in your credentials set during installation
  

**Setup Instructions (Linux):**

1. **Install VirtualBox** (free)
   - sudo apt update
   - sudo apt install virtualbox virtualbox-ext-pack -y
   - virtualbox (to launch)

2. **Download Kali Linux** (security-focused Linux distribution)
   - Get the VirtualBox image: https://www.kali.org/get-kali/#kali-virtual-machines
   - Download the `.ova` file (pre-built VM)

3. **Import to VirtualBox**
   - Open VirtualBox
   - File → Import Appliance
   - Select downloaded `.ova` file
   - Click Import and wait

4. **Start Your VM**
   - Select Kali Linux VM
   - Click Start
   - Default credentials: `kali` / `kali`


## 🛠️ Essential Tools

### Week 1-2 Tools
```bash
# Linux users / Mac with Homebrew:
sudo apt install nmap wireshark curl wget   # Linux
brew install nmap wireshark curl wget       # Mac

# Windows:
# Download installers from official websites
# Nmap: https://nmap.org/download.html
# Wireshark: https://www.wireshark.org/download.html
```

### Week 3-4 Tools (Python libraries)
```bash
pip install cryptography pycryptodome requests beautifulsoup4
```

### Week 5-8 Tools (Advanced)
These will be covered as needed:
- Burp Suite Community Edition
- Metasploit (included in Kali Linux)
- OWASP ZAP

**Don't worry!** Each week's README will tell you exactly what tools you need.

## 📚 Learning Path

### For Complete Beginners
Start here and follow in order:
1. Week 1: Linux Basics
2. Week 2: Networking
3. Week 3: Cryptography
4. Week 4-5: Web Security
... continue sequentially

### For Those with Some Experience
You can skip ahead, but we recommend:
- Review Week 1 labs (quick refresher)
- Focus on areas you want to strengthen
- Jump to advanced weeks as needed

### Self-Paced Learning
- Complete labs at your own speed
- Aim for 2-4 hours per week (can be completed during club time)
- Document your progress
- Ask questions in Discord/Slack

## 📝 How to Complete Labs

### Step 1: Read the README
Every week has a README with:
- Overview of topics
- Learning objectives
- Resources
- Expected time commitment

### Step 2: Follow the Lab Instructions
Each lab includes:
- Background information
- Step-by-step tasks
- Commands to run
- Expected outputs

### Step 3: Document Your Work
Create a document with:
- Screenshots of commands and results
- Answers to questions
- Notes on what you learned
- Problems you encountered

**Template:**
```markdown
# Week X - Lab Y

## Name: [Your Name]
## Date: [Date]

## Task 1: [Task Name]
### Command Used:

[command here]

### Output:
[screenshot or text]
### Explanation:
[your understanding]
## Questions:
1. Question 1: [your answer]
2. Question 2: [your answer]
...
## Challenges Encountered:
[describe any issues]
## What I Learned:
[key takeaways]
```

### Step 4: Submit (if required)
- Follow instructor's submission guidelines
- Include all required components

## 🆘 Getting Help

### Before Asking
1. **Read error messages carefully** - they often tell you what's wrong
2. **Google the error** - someone likely had the same issue
3. **Check the week's README** - solutions might be there
4. **Review previous labs** - concepts build on each other

### When You Need Help
1. **Discord/Slack #help channel**
   - Describe what you tried
   - Include error messages
   - Share screenshots

2. **Office Hours**
   - Check schedule in README
   - Bring specific questions
   - Be ready to share your screen

3. **Study Groups**
   - Form groups with peers
   - Teach each other
   - Work through problems together

### How to Ask Good Questions
❌ Bad: "It doesn't work"
✅ Good: "I'm trying to run nmap on localhost (Week 2, Lab 1), but getting 'permission denied'. I tried running it with sudo but still not working. Screenshot attached."

## 🔒 Safety and Ethics

### Golden Rules
1. **Only test systems you own or have permission to test**
2. **Never use these skills illegally**
3. **Respect privacy and data**
4. **Follow the Computer Fraud and Abuse Act**
5. **When in doubt, ask first**

### What You Can Test
✅ Your own computers and devices
✅ Provided lab environments
✅ CTF platforms
✅ Explicitly authorized systems

### What You Cannot Test
❌ School network (without permission)
❌ Friends' devices (without permission)
❌ Company systems (without authorization)
❌ Any public website or server

**Remember:** Unauthorized access is illegal and can have serious consequences.

<!-- ## 📊 Tracking Your Progress

### Week-by-Week Checklist
Copy this to your notes:
```
□ Week 1: Linux Basics
  □ Lab 1: Linux Commands
  □ Lab 2: File Permissions
  
□ Week 2: Networking
  □ Lab 1: Network Scanning
  □ Lab 2: DNS/WHOIS
  
□ Week 3: Cryptography
  □ Lab 1: Encryption
  □ Lab 2: Hashing
... (continue through Week 12)
```

### Skills Tracker
Rate yourself (1-5) after each week:
- 1: Need more practice
- 2: Basic understanding
- 3: Can complete labs independently
- 4: Can explain to others
- 5: Could create similar labs

## 🎯 Success Tips

### Time Management
- **Set aside regular time**: 2-4 hours per week
- **Don't cram**: Cybersecurity requires practice
- **Start early**: Don't wait until deadline
- **Take breaks**: Prevent burnout

### Learning Strategies
- **Hands-on practice**: Don't just read, do!
- **Take notes**: Summarize in your own words
- **Teach others**: Best way to learn
- **Make mistakes**: Learn from failures
- **Stay curious**: Explore beyond labs

### Building Your Portfolio
- **Document everything**: Screenshots, write-ups
- **Create a GitHub**: Store your scripts and notes
- **Write blog posts**: Share your learning journey
- **Participate in CTFs**: Apply your skills
- **Network**: Connect with other learners

## 🏆 Beyond the Labs

### Next Steps
1. **CTF Competitions**
   - picoCTF (beginner-friendly)
   - TryHackMe (guided)
   - HackTheBox (challenging)

2. **Certifications**
   - CompTIA Security+ (entry-level)
   - CCNA (mid-level)

3. **Bug Bounties**
   - Start with small programs
   - Practice responsible disclosure
   - Build reputation

-->

## 📞 Resources

### This Course
- Main README: `README.md`
- Instructor Guide: `INSTRUCTOR_GUIDE.md`
- Weekly folders: `Week1/`, `Week2/`, etc.

### External Resources
- [Cybrary](https://www.cybrary.it/) - Free courses
- [SANS Cyber Aces](https://www.cyberaces.org/) - Tutorials
- [OWASP](https://owasp.org/) - Web security
- [Reddit r/netsec](https://reddit.com/r/netsec) - News
- [Krebs on Security](https://krebsonsecurity.com/) - Blog


## ✅ Pre-Week 1 Checklist

Before starting Week 1, make sure you have:
- [ ] Cloned the repository
- [ ] Joined Discord/Slack
- [ ] Set up basic tools (Git, text editor)
- [ ] Read this getting started guide
- [ ] Reviewed Week 1 README
- [ ] Set aside time for labs
- [ ] Created a notes document
- [ ] Introduced yourself to the community

## 🎉 Ready to Start?

You're all set! Head over to [Week 1](Week1/) and begin your cybersecurity journey.

---

*Questions? Reach out on Discord/Slack or email [contact info]*
