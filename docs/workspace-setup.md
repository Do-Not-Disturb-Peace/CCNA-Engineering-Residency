# Workspace Setup Guide

## 1. Create the GitHub Repository

Create a new public repository named:

`CCNA-Engineering-Residency`

Recommended settings:
- Description: `60-day hands-on CCNA network engineering residency using Cisco Packet Tracer, troubleshooting, documentation, and enterprise-style deployments.`
- Visibility: Public
- Do not initialize with a README, license, or `.gitignore` if you plan to push this prepared package.

## 2. Extract This Package

Extract the ZIP into a permanent folder such as:

`C:\Users\LaToya\Documents\GitHub\CCNA-Engineering-Residency`

Do not work directly from Downloads or inside the ZIP archive.

## 3. Install Git

After installation, open PowerShell and verify:

```powershell
git --version
```

Configure your identity:

```powershell
git config --global user.name "LaToya Ellis"
git config --global user.email "YOUR_GITHUB_EMAIL"
git config --global init.defaultBranch main
```

Use a GitHub noreply email if you do not want your private email exposed in commit history.

## 4. Open the Project in VS Code

In VS Code:

1. Select **File > Open Folder**.
2. Select `CCNA-Engineering-Residency`.
3. Accept the recommended extensions.
4. Open `README.md`.
5. Press `Ctrl+Shift+V` to open Markdown Preview.

## 5. Initialize and Push

Open the VS Code terminal and run:

```powershell
git init
git add .
git commit -m "Initialize CCNA Engineering Residency"
git branch -M main
git remote add origin https://github.com/Do-Not-Disturb-Peace/CCNA-Engineering-Residency.git
git push -u origin main
```

GitHub may open a browser authentication window. Approve the sign-in.

## 6. VS Code Extensions

Install only these initially:

- Markdown All in One
- Code Spell Checker
- GitLens
- GitHub Pull Requests and Issues
- Material Icon Theme

Avoid installing unnecessary extensions. They add noise and can slow the editor.

## 7. Markdown Workflow

- Edit `.md` files in VS Code.
- Use `Ctrl+Shift+V` for full preview.
- Use `Ctrl+K`, then `V` for side-by-side preview.
- Save images under `images/`.
- Use relative links, for example:

```markdown
![Topology](../../images/day01-topology.png)
```

## 8. OBS Studio Baseline

Create a scene named `CCNA Lab Recording`.

Add these sources:
1. Display Capture or Window Capture for Packet Tracer
2. Audio Input Capture for your microphone
3. Optional Window Capture for the topology diagram

Recommended recording settings:
- Format: MKV
- Encoder: Hardware encoder when available
- Resolution: 1920×1080
- Frame rate: 30 FPS
- Audio: 48 kHz
- Recording quality: High quality, medium file size

Record to a local folder outside the Git repository:

`Videos\CCNA-Residency`

Do not commit raw recordings to GitHub. Upload selected videos to YouTube as Unlisted or Public and link them from Markdown.

Perform a 60-second test recording. Confirm:
- Text is readable
- Microphone is clear
- Desktop notifications are disabled
- Browser tabs and personal data are hidden

## 9. diagrams.net Baseline

Create a reusable diagram file:

`diagrams/enterprise-network-template.drawio`

Use:
- Cisco network device shapes
- Consistent left-to-right traffic flow
- Device hostnames
- Interface labels only when necessary
- VLAN and subnet labels
- A simple legend

Export public diagrams as PNG into `images/`.

## 10. Monday Readiness Test

Before Monday, confirm all five items:

- [ ] `README.md` previews correctly in VS Code
- [ ] `git status` works
- [ ] First commit appears on GitHub
- [ ] Packet Tracer opens and saves a `.pkt` file
- [ ] OBS produces a clear 60-second recording
