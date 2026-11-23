# Prerequisites: install the app and get your own copy of the project

**Do this at least one day before the dojo (30 minutes).** You will install two programs on your computer (Git and the GitHub Copilot app), sign in, and get your own copy of this project.

## 1. The checklist
| ☐ | You need | How to check |
|---|---|---|
| ☐ | A **computer** running **Windows, macOS or Linux** that you are allowed to install software on | Ask your IT team if the install is blocked. |
| ☐ | A **GitHub account** | You can sign in at https://github.com. No account yet? Click **Sign up** (free). |
| ☐ | **Access to GitHub Copilot** (a plan, or your own model provider) | See "About Copilot access" below. |
| ☐ | **Git** installed | Part 3. |
| ☐ | The **GitHub Copilot app** installed and signed in (personal or company account) | Parts 3b and 3c. |
| ☐ | **Your own copy** (a "fork") of the dojo project | Part 4. |
| ☐ | The project **added to the app**, and Copilot answering a test question | Parts 5 and 6. |
| ☐ | A stable internet connection | A video call works on it. |

### About Copilot access
- **Company seat (Copilot Business or Enterprise):** the best case. Ask your IT team or the dojo organiser if you are unsure. The organisation's administrator must keep the **GitHub Copilot app** policy enabled (it is on by default).
- **Personal plan (Pro, Pro+, Student) or Copilot Free:** the app is available on every Copilot plan. Free has limited monthly usage, so a full dojo may exceed it. Check the current limits on the [plans page](https://docs.github.com/en/copilot/get-started/plans).
- **No Copilot plan:** the app also lets you sign in with **your own model provider** (you enter its credentials during sign-in).
- **Company-managed GitHub accounts:** your organisation decides whether you can fork repositories or sign in to the app. If a step below is blocked, tell the organiser: this is a policy, not a mistake of yours.

## 2. Three words to know
| Word | In plain English |
|---|---|
| **Repository (repo)** | A project folder stored on GitHub. This dojo is one repo. |
| **Fork** | Your **own copy** of someone else's repo, on your GitHub account. You can change it freely. |
| **Clone** | A copy of a repo **on your computer**. The app does this for you in Part 5. |

You cannot save changes in the original project. That is why you first create **your own copy** (Part 4).

## 3. Install Git (5 minutes, once)
The app needs **Git** on your computer. Check first: if you already have it, skip this part.
1. Open a terminal:
   - **Windows:** click the Start menu, type `cmd`, and press **Enter**.
   - **macOS:** press `Command + Space`, type `Terminal`, and press **Enter**.
2. Type `git --version` and press **Enter**.
   - ✅ If you see a version number such as `git version 2.x.x`: Git is installed. Skip to Part 3b.
   - If you see "command not found" or "not recognized": install it.
3. Install Git:
   - **Windows:** go to https://git-scm.com/downloads, click **Windows**, run the downloaded installer, and click **Next** on every screen (the default options are fine), then **Install** and **Finish**.
   - **macOS:** the terminal may offer to install the developer tools when you type `git --version`: click **Install** and wait. Otherwise, download Git from https://git-scm.com/downloads.
4. **Close the terminal and open a new one**, type `git --version` again.
   - ✅ A version number appears.

## 3b. Install the GitHub Copilot app (5 minutes, once)
1. Download the installer for your computer (click the link, the download starts):

   | Your computer | Download |
   |---|---|
   | **Windows** (most PCs) | [GitHub-Copilot-windows-x64-setup.exe](https://github.com/github/app/releases/latest/download/GitHub-Copilot-windows-x64-setup.exe) |
   | Windows on ARM | [GitHub-Copilot-windows-arm64-setup.exe](https://github.com/github/app/releases/latest/download/GitHub-Copilot-windows-arm64-setup.exe) |
   | **Mac with Apple chip** (M1, M2, M3…) | [GitHub-Copilot-darwin-arm64.dmg](https://github.com/github/app/releases/latest/download/GitHub-Copilot-darwin-arm64.dmg) |
   | Mac with Intel chip | [GitHub-Copilot-darwin-x64.dmg](https://github.com/github/app/releases/latest/download/GitHub-Copilot-darwin-x64.dmg) |
   | Linux (x64) | [GitHub-Copilot-linux-x64.AppImage](https://github.com/github/app/releases/latest/download/GitHub-Copilot-linux-x64.AppImage) |
   | Linux (ARM) | [GitHub-Copilot-linux-arm64.AppImage](https://github.com/github/app/releases/latest/download/GitHub-Copilot-linux-arm64.AppImage) |

   All versions: https://github.com/github/app/releases. Not sure which Mac you have? Apple menu → **About This Mac**: "Chip: Apple M…" means Apple chip; "Processor: Intel…" means Intel.
2. Install it:
   - **Windows:** double-click the downloaded `.exe` and follow the installer.
   - **macOS:** double-click the `.dmg`, then drag the app icon into **Applications**.
   - **Linux:** make the `.AppImage` file executable and run it.
   - 🆘 If your computer blocks the install (company restrictions): ask IT to allow it, or ask the organiser for a loaner computer.
3. Open the **GitHub Copilot** app.
   - ✅ A welcome screen with a **Sign in to GitHub** button appears.
4. Sign in. **Choose the case that matches you in Part 3c** (personal account or company account).

## 3c. Sign in: personal account or company account
First, find out which kind of GitHub account you have. Ask your IT team or the organiser if unsure.

| If… | You are in case |
|---|---|
| You use your **own** GitHub account (created by you, with your personal email) | **A. Personal account** |
| Your company gave you a GitHub account whose username looks like `firstname_company`, and you sign in with your **company login** (Microsoft, Okta, etc.) on github.com | **B. Company-managed account (github.com)** |
| Your company GitHub address looks like `https://yourcompany.ghe.com` | **C. Company account with data residency (`*.ghe.com`)** |
| Your company hosts GitHub on its **own server** (an internal address such as `github.yourcompany.com`) | **D. GitHub Enterprise Server** |
| You use your personal account, and your company's organisation invited you and requires single sign-on | **E. Personal account with company SSO** |

### Case A — Personal account
1. In the app, click **Sign in to GitHub**.
2. Your browser opens. Sign in to GitHub and click **Authorize** when asked.
3. Return to the app. ✅ You are signed in.

### Case B — Company-managed account (github.com)
1. In the app, click **Sign in to GitHub**.
2. Your browser opens on github.com. Enter your **company username** (`firstname_company`) **or** use the sign-in option that sends you to your company's identity provider. You then land on your **company login page** (Microsoft, Okta…).
3. Sign in with your **company email and password**, and complete the **multi-factor** step (code, notification, security key) if asked.
4. When GitHub asks to authorise the app, click **Authorize**.
5. Return to the app. ✅ You are signed in with your company account.
   - 🆘 If the browser shows a **404 page**: you are probably signed in to the wrong GitHub account in that browser. Sign out of GitHub, then restart from step 1, or use a private/incognito window.
   - 🆘 If the browser logs you in automatically to a **personal** account you do not want to use: sign out of GitHub in the browser first.
   - 🆘 If the page says your account has **no Copilot access**: your seat is not assigned. Ask the organiser or IT.

### Case C — Company account with data residency (`*.ghe.com`)
1. In the app, click **Sign in to GitHub**.
2. When asked, choose **GitHub Enterprise Cloud** and type your company's **`*.ghe.com` address** (for example `yourcompany.ghe.com`). Ask IT for the exact address.
3. Your browser opens on your company's GitHub. Sign in with your **company login** and multi-factor step, then click **Authorize**.
4. Return to the app. ✅ You are signed in.

### Case D — GitHub Enterprise Server (company-hosted)
1. The app first needs an account on github.com or on `*.ghe.com`. Sign in as in case A, B or C (ask IT which one you must use).
2. In the app, open **Settings** (the settings dialog).
3. In the sidebar of the dialog, click **Accounts**.
4. Click **Add account**, then **GitHub Enterprise Server**.
5. Follow the prompts: your browser opens, you sign in with your company credentials and authorise the app.
6. ✅ Your company server account is now connected.

### Case E — Personal account with company SSO
1. Sign in as in case A.
2. When you open your company's repositories, GitHub may show a message asking you to **authorise your sign-in session for the organisation** (single sign-on). Click **Authorize** (or **Continue**) and sign in with your company credentials.

### If you have no Copilot plan at all
In the app's sign-in flow you can choose to sign up, or to use **your own model provider**: select it, enter its credentials, and click **Save and continue**.

> **Important for companies:** the organisation's administrator must keep the **GitHub Copilot app** policy enabled (it is on by default), and your account must have a Copilot seat. Without them the app will open but Copilot will not answer.

## 4. Get your own copy (fork) of the project
1. In your browser, open the dojo project: `https://github.com/ghisdubreuil/ai-dojo`. Sign in to GitHub if asked.
2. At the top right of the page, click **Fork**.
   - ✅ A page titled **Create a new fork** opens.
3. Leave the name as `ai-dojo`. Under **Owner**, make sure your own account is selected.
4. Click **Create fork**.
   - ✅ After a few seconds you land on `https://github.com/YOUR-USERNAME/ai-dojo`, with "forked from ghisdubreuil/ai-dojo" under the title.
   - 🆘 If **Fork** is greyed out or an error says forking is not allowed: your organisation restricts it. See "If you cannot fork" below.

### If you cannot fork (typical with company-managed accounts)
A **company-managed account** (cases B, C and D above) can usually only work with repositories **inside your company's GitHub**: it cannot fork a public project that lives on someone else's account. In that case the **organiser** must first put a copy of the project inside the company's GitHub (see "For the facilitator" below), and you either:
- use the green **Use this template** → **Create a new repository** button on that company copy (if it is a template), or
- use the copy the organiser created for you.
Then continue with Part 5, picking **that** repository.

## 5. Add the project to the app
1. Open the GitHub Copilot app.
2. In the **sidebar** on the left, find the section **Sessions**. Click the small **add** control next to it (usually a **+** icon).
3. In the menu, click **Add GitHub repository**.
   - ✅ A list of your repositories appears.
4. Click `YOUR-USERNAME/ai-dojo` (your fork), and confirm to **clone** it.
   - ✅ The project appears under **Sessions** in the sidebar.
   - 🆘 If your fork is not in the list: use the same menu and choose **Clone repository**, then paste `https://github.com/YOUR-USERNAME/ai-dojo` and confirm.
   - 🆘 If you already have the folder on your computer: choose **Open local folder** and select it.

## 6. Test that everything works
1. In the sidebar, click the **new session** control next to **Sessions** (usually a **+**), then, under **Start session in**, click `ai-dojo`.
2. Below the prompt box, check the drop-downs: **Environment** = **This computer**, **Workspace** = **Current checkout**.
3. Click the **mode** drop-down below the prompt box and choose **Interactive**.
4. Click in the prompt box, type `Hello! In one sentence, what is this project about?` and press **Enter**.
   - ✅ Copilot answers, and mentions a dojo, Maison Orélia, or Copilot training.
   - 🆘 If you see an authentication error: sign in again (Part 3c).
   - 🆘 If Copilot says it has no access or no plan: ask the organiser to check your seat or your plan.
5. **You are ready.** Stop here and continue with the [introduction to Copilot](./01-getting-started-with-copilot.md), then the [app tour](./02-setup-click-by-click.md) on the day.

## 7. For Builder and Expert levels only (optional until you get there)
The Builder and Expert adventures ask Copilot to write and run small Python scripts. Two options:
- **Run on your computer:** install **Python 3.10 or later** from https://www.python.org/downloads/ (on Windows tick **Add python.exe to PATH** in the installer). Check with `python --version` or `python3 --version` in a terminal.
- **Or use a cloud environment:** in the session's **Environment** drop-down, choose **Cloud**. The whole session then runs in a GitHub-hosted sandbox. Test this in your dry run before relying on it.

## 8. Troubleshooting
| Problem | What to try |
|---|---|
| Cannot install the app (blocked) | Ask IT for permission, or use a loaner computer. |
| "Sign in" opens a browser but nothing happens | Return to the app after authorising, and wait 10 seconds. If it still fails, quit and reopen the app. |
| The app says you have no access | Your Copilot seat or plan is missing, or the organisation disabled the GitHub Copilot app policy. Ask the organiser. |
| Your fork is not listed under **Add GitHub repository** | Use **Clone repository** with the URL of your fork. |
| An error mentions "git" | Git is not installed or the terminal was not reopened. Redo Part 3, then restart the app. |
| Copilot stops answering mid-dojo | You may have reached your plan's usage limit. Ask the organiser. |
| Single sign-on (SSO) screen asks you to authorise | Click **Authorize** and sign in with your company credentials. |
| Browser shows a 404 page during sign-in | You are signed in to the wrong GitHub account in that browser. Sign out of GitHub or use a private window, and restart the sign-in. |
| The company login works but the app says no Copilot access | Your Copilot seat is not assigned, or the GitHub Copilot app policy is disabled. Ask the organiser or IT. |

## 9. For the facilitator: before the day
- ☐ Check that every participant has a **Copilot seat or plan** (or tell them to use their own model provider), and that the organisation's **GitHub Copilot app** policy is enabled.
- ☐ Check that participants may **install software**. Ask IT in advance for approval of Git and the app.
- ☐ Decide: participants **fork** this repo, or you give each a copy (template: tick **Template repository** in the repo's **Settings**).
- ☐ **Company-managed accounts cannot fork a public repository from outside the company.** Put a copy of the project inside your company's GitHub organisation first: on GitHub, click **+ → Import repository**, enter `https://github.com/ghisdubreuil/ai-dojo` as the source, and create it in your organisation (or clone it and push it to a new repository there). Then make it a **template** (**Settings → Template repository**) so each participant can create their own copy.
- ☐ Tell participants which sign-in case applies to them (A to E in Part 3c) and, for `*.ghe.com`, the exact address.
- ☐ Ask everyone to complete Parts 3 to 6 **one day before**, and to reply "OK" once Copilot answered "Hello". Fix blockers early.
- ☐ Do a full dry run on **each operating system** in the room (Windows and macOS), and note any label that differs.
- ☐ For Expert adventure C3, enable **Issues** on forks (repo **Settings → General → Features → Issues**), or seed one issue per participant.
- ☐ Prepare a backup plan: pair people who cannot install with a neighbour.

Next: [Introduction to Copilot](./01-getting-started-with-copilot.md).
