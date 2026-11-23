# Prerequisites: install the app and get your own copy of the project

**Do this at least one day before the dojo (30 minutes).** You will install two programs on your computer (Git and the GitHub Copilot app), sign in, and get your own copy of this project.

## 1. The checklist
| ☐ | You need | How to check |
|---|---|---|
| ☐ | A **computer** running **Windows, macOS or Linux** that you are allowed to install software on | Ask your IT team if the install is blocked. |
| ☐ | A **GitHub account** | You can sign in at https://github.com. No account yet? Click **Sign up** (free). |
| ☐ | **Access to GitHub Copilot** (a plan, or your own model provider) | See "About Copilot access" below. |
| ☐ | **Git** installed | Part 2. |
| ☐ | The **GitHub Copilot app** installed and signed in | Part 3. |
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
1. Open https://github.com/github/app in your browser, then follow the **Download** link of the README, or open the **Releases** page and pick the file for your computer:
   - Windows (most computers): the file ending in `windows-x64-setup.exe` (use `windows-arm64` only on ARM laptops).
   - Mac with an Apple chip (M1, M2, M3…): `darwin-arm64.dmg`. Mac with an Intel chip: `darwin-x64.dmg`. (To know: Apple menu → **About This Mac**.)
   - Linux: the `.AppImage` file.
2. Install it:
   - **Windows:** double-click the downloaded `.exe` and follow the installer.
   - **macOS:** double-click the `.dmg`, then drag the app icon into **Applications**.
   - **Linux:** make the `.AppImage` file executable and run it.
3. Open the **GitHub Copilot** app.
   - ✅ A welcome screen with a **Sign in to GitHub** button appears.
   - 🆘 If your computer blocks the install (company restrictions): ask IT to allow it, or ask the organiser for a loaner computer.
4. Click **Sign in to GitHub** and follow the prompts in your browser (sign in, then authorise).
   - If you have **no Copilot plan**, the app lets you sign up, or use your own model provider: select it, enter the credentials, and click **Save and continue**.
5. If asked to **select repositories**, you can **skip** for now (you will add the dojo project in Part 5).
6. Choose a **theme** and finish the onboarding.
   - ✅ The app opens on its main screen, with a sidebar on the left.

## 4. Get your own copy (fork) of the project
1. In your browser, open the dojo project: `https://github.com/ghisdubreuil/ai-dojo`. Sign in to GitHub if asked.
2. At the top right of the page, click **Fork**.
   - ✅ A page titled **Create a new fork** opens.
3. Leave the name as `ai-dojo`. Under **Owner**, make sure your own account is selected.
4. Click **Create fork**.
   - ✅ After a few seconds you land on `https://github.com/YOUR-USERNAME/ai-dojo`, with "forked from ghisdubreuil/ai-dojo" under the title.
   - 🆘 If **Fork** is greyed out or an error says forking is not allowed: your organisation restricts it. See "If you cannot fork" below.

### If you cannot fork
Ask the organiser to give you a copy in the organisation: either a **template** (the green **Use this template** → **Create a new repository** button), or a per-participant repository.

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
   - 🆘 If you see an authentication error: sign in again (Part 3b, step 4).
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

## 9. For the facilitator: before the day
- ☐ Check that every participant has a **Copilot seat or plan** (or tell them to use their own model provider), and that the organisation's **GitHub Copilot app** policy is enabled.
- ☐ Check that participants may **install software**. Ask IT in advance for approval of Git and the app.
- ☐ Decide: participants **fork** this repo, or you give each a copy (template: tick **Template repository** in the repo's **Settings**).
- ☐ Ask everyone to complete Parts 3 to 6 **one day before**, and to reply "OK" once Copilot answered "Hello". Fix blockers early.
- ☐ Do a full dry run on **each operating system** in the room (Windows and macOS), and note any label that differs.
- ☐ For Expert adventure C3, enable **Issues** on forks (repo **Settings → General → Features → Issues**), or seed one issue per participant.
- ☐ Prepare a backup plan: pair people who cannot install with a neighbour.

Next: [Introduction to Copilot](./01-getting-started-with-copilot.md).
