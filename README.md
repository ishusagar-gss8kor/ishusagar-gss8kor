<!--
  Ishu Sagar — GitHub Profile README (v2)
  Setup: create a PUBLIC repo named exactly "ishusagar-gss8kor" and put this file in it as README.md
-->

<!-- ============ HERO ============ -->
<p align="center">
  <img src="https://capsule-render.vercel.app/api?type=waving&color=0:0d1117,50:1f3a5f,100:2ea043&height=200&section=header&text=Ishu%20Sagar&fontSize=56&fontColor=ffffff&fontAlignY=38&desc=Automotive%20Systems%20%C2%B7%20Diagnostics%20%C2%B7%20Embedded&descAlignY=60&descSize=18&descColor=c9d1d9" alt="Ishu Sagar banner" />
</p>

<p align="center">
  <a href="https://github.com/ishusagar-gss8kor">
    <img src="https://readme-typing-svg.demolab.com?font=Fira+Code&weight=500&size=20&duration=3200&pause=900&color=58A6FF&center=true&vCenter=true&width=720&lines=Senior+Automotive+Systems+Engineer;Making+the+vehicle+behave+correctly%2C+not+just+the+code+compile;UDS+%C2%B7+DoCAN+%C2%B7+DoIP+%C2%B7+OBDonUDS;Requirements+%E2%86%92+Architecture+%E2%86%92+Software+%E2%86%92+Vehicle" alt="Typing animation" />
  </a>
</p>

<p align="center">
  <a href="https://linkedin.com/in/ishusagar"><img src="https://img.shields.io/badge/LinkedIn-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white"/></a>
  <a href="https://github.com/ishusagar-gss8kor?tab=repositories"><img src="https://img.shields.io/badge/Repositories-181717?style=for-the-badge&logo=github&logoColor=white"/></a>
  <img src="https://komarev.com/ghpvc/?username=ishusagar-gss8kor&style=for-the-badge&color=2ea043&label=Profile+Views"/>
</p>

---

## 🔌 Boot Log

```text
$ whoami
ishu_sagar — senior automotive systems engineer

$ cat focus.cfg
domain        = diagnostics + OBD regulatory requirements
languages     = C, C++, Python
mindset       = system intent first, implementation second
side_quest    = AI for engineering workflows & knowledge management

$ status
[ OK ] requirements understood
[ OK ] interfaces defined
[ OK ] diagnostics behaving
[ .. ] still learning, always
```

---

## 🧭 What I Do

I work where **standards, system behavior, embedded software and real vehicle constraints** collide, and I like being the person who connects those layers.

<table>
<tr>
<td width="50%" valign="top">

### 🏗️ Systems Engineering
- Requirement engineering & decomposition
- System architecture & interface definition
- Traceability & change management
- ASPICE-oriented development
- System-level problem analysis

</td>
<td width="50%" valign="top">

### 🩺 Diagnostics & OBD
- UDS (ISO 14229) · DoCAN (ISO 15765) · DoIP (ISO 13400)
- OBD / OBDonUDS · SAE J1979 / J2012
- DTC / DFC analysis
- Diagnostic communication design
- OBD monitoring concepts & regulatory requirements

</td>
</tr>
<tr>
<td valign="top">

### 💾 Embedded Software
- C / C++ / Python
- ECU software architecture, ASW / BSW interfaces
- Vehicle communication
- Debugging & root-cause analysis

</td>
<td valign="top">

### ⚙️ Tooling & Automation
- INCA · A2L / HEX / DCM
- Python automation for engineering workflows
- Diagnostic data analysis
- Git / GitHub, requirements & configuration tools

</td>
</tr>
</table>

---

## 🧠 How I Think: From Requirement to Vehicle

```mermaid
flowchart LR
    R([📄 Requirement]) --> S[System Model]
    S --> A[Architecture]
    S --> I[Interfaces]
    S --> D[Diagnostics]
    A --> SW[Software Behavior]
    I --> SW
    D --> SW
    SW --> V{{Verification & Test}}
    V --> VB([🚗 Vehicle Behavior])
    VB -. feedback .-> R
```

> **The goal is not just to make software work. The goal is to make the system behave correctly.**

---

## 📡 A Day in the Life: One Diagnostic Exchange

```mermaid
sequenceDiagram
    autonumber
    participant T as Tester
    participant E as ECU
    T->>E: 10 03 (DiagnosticSessionControl: extended)
    E-->>T: 50 03 (positive response)
    T->>E: 22 F1 90 (ReadDataByIdentifier: VIN)
    E-->>T: 62 F1 90 [data]
    T->>E: 19 02 FF (ReadDTCInformation: by status mask)
    E-->>T: 59 02 ... (DTCs + status)
    T->>E: 31 01 xx xx (RoutineControl: start)
    E--xT: 7F 31 22 (NRC: conditionsNotCorrect)
```

<details>
<summary><b>🔎 Cheat sheet: how I read a UDS frame</b></summary>

<br/>

| Byte | Meaning |
|------|---------|
| `SID` | Service request, e.g. `0x22` ReadDataByIdentifier |
| `SID + 0x40` | Positive response, e.g. `0x62` |
| `0x7F SID NRC` | Negative response with its reason code |
| `0x10` / `0x11` / `0x14` / `0x19` | Session control / ECU reset / Clear DTC / Read DTC |
| `0x27` / `0x2E` / `0x31` / `0x3E` | Security access / Write DID / Routine control / Tester present |

The real work starts after the byte level: *why* did this NRC occur, which requirement defines the condition, and which software path produced it?

</details>

---

## 🛠️ Tech Stack

<p align="center">
  <img src="https://img.shields.io/badge/C-00599C?style=for-the-badge&logo=c&logoColor=white"/>
  <img src="https://img.shields.io/badge/C%2B%2B-00599C?style=for-the-badge&logo=c%2B%2B&logoColor=white"/>
  <img src="https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white"/>
  <img src="https://img.shields.io/badge/Git-F05032?style=for-the-badge&logo=git&logoColor=white"/>
  <img src="https://img.shields.io/badge/GitHub-181717?style=for-the-badge&logo=github&logoColor=white"/>
</p>
<p align="center">
  <img src="https://img.shields.io/badge/UDS-ISO%2014229-2E7D32?style=for-the-badge"/>
  <img src="https://img.shields.io/badge/DoCAN-ISO%2015765-1565C0?style=for-the-badge"/>
  <img src="https://img.shields.io/badge/DoIP-ISO%2013400-6A1B9A?style=for-the-badge"/>
  <img src="https://img.shields.io/badge/OBD-J1979%20%2F%20J1979--2-F57C00?style=for-the-badge"/>
  <img src="https://img.shields.io/badge/ASPICE-Engineering-455A64?style=for-the-badge"/>
  <img src="https://img.shields.io/badge/INCA-A2L%20%2F%20HEX-B71C1C?style=for-the-badge"/>
</p>

---

## 🚀 What I Build

| | Focus | Outcome |
|---|---|---|
| 🩺 | **Diagnostics & OBD** | Clear DTC behavior, diagnostic communication and regulatory-driven requirements |
| 🏗️ | **System Engineering** | Complex requirements broken into behavior, interfaces, software responsibilities and verification criteria |
| 🤖 | **Engineering Automation** | Small Python tools that remove repetitive work and make analysis faster and more consistent |
| 🔍 | **Root-Cause Analysis** | Tracing a vehicle symptom back through ECU behavior to the requirement behind it |

<!--
  FEATURED PROJECTS: uncomment and replace YOUR_REPO to show pinned cards
  <p align="center">
    <a href="https://github.com/ishusagar-gss8kor/YOUR_REPO"><img src="https://github-readme-stats.vercel.app/api/pin/?username=ishusagar-gss8kor&repo=YOUR_REPO&theme=github_dark&hide_border=true"/></a>
    <a href="https://github.com/ishusagar-gss8kor/YOUR_REPO_2"><img src="https://github-readme-stats.vercel.app/api/pin/?username=ishusagar-gss8kor&repo=YOUR_REPO_2&theme=github_dark&hide_border=true"/></a>
  </p>
-->

---

## 🔭 Currently Exploring

- 🧩 Diagnostic architectures and OBDonUDS requirement traceability
- 🤖 Applying AI to engineering workflows and technical knowledge management
- 🐍 Python tooling for diagnostic data analysis

---

## 📊 GitHub Activity

<p align="center">
  <img height="165" src="https://github-readme-stats.vercel.app/api?username=ishusagar-gss8kor&show_icons=true&hide_border=true&theme=github_dark&rank_icon=github" alt="GitHub Stats"/>
  <img height="165" src="https://github-readme-stats.vercel.app/api/top-langs/?username=ishusagar-gss8kor&layout=compact&hide_border=true&theme=github_dark" alt="Top Languages"/>
</p>
<p align="center">
  <img width="95%" src="https://github-readme-activity-graph.vercel.app/graph?username=ishusagar-gss8kor&theme=github-compact&hide_border=true" alt="Activity Graph"/>
</p>

---

## 🤝 Let's Connect

I'm happy to talk diagnostics, OBD, system architecture or engineering automation.

<p align="center">
  <a href="https://linkedin.com/in/ishusagar"><img src="https://img.shields.io/badge/Connect%20on-LinkedIn-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white"/></a>
  <a href="https://github.com/ishusagar-gss8kor"><img src="https://img.shields.io/badge/Follow%20on-GitHub-181717?style=for-the-badge&logo=github&logoColor=white"/></a>
</p>

<p align="center">
  <img src="https://capsule-render.vercel.app/api?type=waving&color=0:2ea043,50:1f3a5f,100:0d1117&height=100&section=footer" />
</p>

<p align="center"><i>Systems thinking · Engineering discipline · Continuous learning</i></p>
