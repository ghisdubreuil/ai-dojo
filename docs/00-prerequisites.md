# Prerequisites: install the app and open the project

**Do this at least one day before the dojo (20 minutes).** You will install **one program** (the GitHub Copilot app), and sign in with your **company login (SSO)**. That is all: you do not need to create any account. Your company provides your access and your Copilot licence.

## 1. The checklist
| ☐ | You need | How to check |
|---|---|---|
| ☐ | A **computer** running **Windows, macOS or Linux** on which you are allowed to install the app | Ask IT if the install is blocked. |
| ☐ | Your **company login** (the one you use for your work email) and your **multi-factor method** (phone, authenticator app, security key) | You can sign in to your company email. |
| ☐ | The **GitHub Copilot app** installed and signed in with your company login | Parts 3 and 4. |
| ☐ | The **name of the dojo project** given by your organiser | Part 5. |
| ☐ | The project **added to the app**, and Copilot answering a test question | Parts 6 and 7. |
| ☐ | A stable internet connection | A video call works on it. |

## 2. Two words to know
| Word | In plain English |
|---|---|
| **Repository (repo)** | A project folder stored on GitHub. This dojo is one repo. |
| **Clone** | A copy of a repo **on your computer**. The app does this for you in Part 6. |


## 3. Install the GitHub Copilot app (5 minutes, once)
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
   - 🆘 If your computer blocks the install: ask IT to allow it, or ask the organiser for a loaner computer.
3. Open the **GitHub Copilot** app.
   - ✅ A welcome screen with a **Sign in to GitHub** button appears.

## 4. Sign in with your company login (SSO)
1. In the app, click **Sign in to GitHub**.
2. Your web browser opens. Sign in with your **company login**: enter your company email or username, and you are sent to your **company login page**.
3. Enter your **company password** and complete the **multi-factor** step (code, notification, security key) if asked.
4. When GitHub asks to authorise the app, click **Authorize**.
5. Return to the app.
   - ✅ You are signed in. If you are asked to **select repositories**, you can **skip** (you will add the dojo project in Part 6).
6. Choose a **theme** and finish the onboarding.
   - ✅ The app opens on its main screen, with a sidebar on the left.

🆘 If something goes wrong:
- **The browser shows a 404 page:** another GitHub account is open in that browser. Sign out of GitHub, or use a private (incognito) window, and restart from step 1.
- **The app asks you to choose "GitHub Enterprise Cloud" and to type an address ending in `.ghe.com`:** do it, using the address given by your organiser.
- **Sign-in works but Copilot does not answer:** ask your organiser or IT: your company manages Copilot access.

## 5. Get the project name
Your organiser tells you the name of the dojo project (`ai-dojo`) in your company's GitHub. Nothing to create, nothing to sign up for: you will add it to the app in the next part.

## 6. Add the project to the app
1. Open the GitHub Copilot app.
2. In the **sidebar** on the left, find the section **Sessions**. Click the small **add** control next to it (usually a **+** icon).
3. In the menu, click **Add GitHub repository**.
   - ✅ A list of repositories appears.
4. Click `ai-dojo` (the project named by your organiser) and confirm to **clone** it.
   - ✅ The project appears under **Sessions** in the sidebar.
   - 🆘 If it is not in the list: use the same menu, choose **Clone repository**, paste the project address given by your organiser and confirm.

## 7. Test that everything works
1. In the sidebar, click the **new session** control next to **Sessions** (usually a **+**), then, under **Start session in**, click `ai-dojo`.
2. Below the prompt box, check the drop-downs: **Environment** = **This computer**, **Workspace** = **Current checkout**.
3. Click the **mode** drop-down below the prompt box and choose **Interactive**.
4. Click in the prompt box, type `Hello! In one sentence, what is this project about?` and press **Enter**.
   - ✅ Copilot answers, and mentions a dojo, Maison Orélia, or Copilot training.
   - 🆘 If you see an authentication error: sign in again (Part 4).
   - 🆘 If Copilot says it has no access: ask your organiser or IT.
5. **You are ready.** Stop here and continue with the [introduction to Copilot](./01-getting-started-with-copilot.md), then the [app tour](./02-setup-click-by-click.md) on the day.

## 8. For Builder and Expert levels only
The Builder and Expert adventures ask Copilot to write and run small Python scripts. **There is nothing more to install**: in the session, set the **Environment** drop-down (below the prompt box) to **Cloud**. The whole session then runs in a GitHub-hosted sandbox instead of on your computer.

> **Facilitator:** test the **Cloud** environment in your dry run (check that cloud sessions are allowed for your company accounts and that Python scripts run). If not, fall back to **This computer** with Python installed by IT.

## 9. Troubleshooting
| Problem | What to try |
|---|---|
| Cannot install the app (blocked) | Ask IT for permission, or use a loaner computer. |
| "Sign in" opens a browser but nothing happens | Return to the app after authorising, and wait 10 seconds. If it still fails, quit and reopen the app. |
| Browser shows a 404 page during sign-in | Another GitHub account is open in that browser. Sign out of GitHub or use a private window, and restart. |
| The company login works but the app says no access | Your company has not enabled Copilot or the app for your account. Ask the organiser or IT. |
| The project is not listed under **Add GitHub repository** | Use **Clone repository** with the address given by your organiser. |
| An error mentions "git" | The app needs **Git** on the computer. Ask IT to install it, then restart the app. |
| A company login screen asks you to authorise | Click **Authorize** and sign in with your company credentials. |

## 10. For the facilitator: before the day
- ☐ Check with IT that every participant's **company GitHub account** can sign in to the **GitHub Copilot app** with SSO, that **Copilot access** is enabled for them, and that the organisation's **GitHub Copilot app** policy is on.
- ☐ Check that participants may **install software**, and ask IT in advance to approve the app (the app also needs **Git** on the computer; check that it is present on your standard laptops).
- ☐ Put the project inside your company's GitHub: on GitHub, click **+ → Import repository**, enter `https://github.com/ghisdubreuil/ai-dojo` as the source, and create it in your organisation (or clone it and push it to a new repository there).
- ☐ Give every participant access to it (write access), and send them its name and address. No participant needs to create an account.
- ☐ For adventure C3: enable **Issues** on the repository (repo **Settings → General → Features → Issues**), or create one issue per participant.
- ☐ Ask everyone to complete Parts 3 to 7 **one day before**, and to reply "OK" once Copilot answered "Hello". Fix blockers early.
- ☐ Do a full dry run on **each operating system** in the room (Windows and macOS) with a real company account, and note any label that differs.
- ☐ Prepare a backup plan: pair people who cannot install with a neighbour.

Next: [Introduction to Copilot](./01-getting-started-with-copilot.md).
