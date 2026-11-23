# Prerequisites: get your own copy and work from your web browser

**Do this at least one day before the dojo (15 minutes).** Nothing needs to be installed on your computer: everything runs in a web browser.

## 1. The checklist
| ☐ | You need | How to check |
|---|---|---|
| ☐ | A **recent web browser** (Chrome, Edge, Firefox or Safari) | Open https://github.com. The page loads normally. |
| ☐ | A **GitHub account** | You can sign in at https://github.com. No account yet? Click **Sign up** (free). |
| ☐ | **Access to GitHub Copilot** | Open https://github.com/settings/copilot while signed in. You see Copilot settings, with a plan or a seat. |
| ☐ | **Access to Codespaces** (the online workspace) | At the end of Part 3 below, a Codespace opens. |
| ☐ | A **stable internet connection** | A video call works on it. |

### About Copilot access (read this carefully)
- **Company-provided seat (Copilot Business or Enterprise):** the best case. Your organisation assigns a seat to your GitHub account. Ask your IT or the dojo organiser if you are unsure.
- **Personal plan (Pro, Student):** works if you use a personal GitHub account.
- **Copilot Free:** limited monthly allowances of completions and chat usage, and meant for **personal accounts only**, not for accounts managed by an organisation. A dojo uses many chat messages, so you may hit the limit. Check the current limits on the [plans page](https://docs.github.com/en/copilot/get-started/plans).
- **Company-managed GitHub account (sometimes called an "enterprise managed user")**: your organisation decides whether you can fork repositories or use Codespaces. If a step below is blocked, tell the organiser: this is a policy setting, not something you did wrong.

## 2. Three words to know
| Word | In plain English |
|---|---|
| **Repository (repo)** | A project folder stored on GitHub. This dojo is one repo. |
| **Fork** | Your **own copy** of someone else's repo, on your GitHub account. You can change it freely. |
| **Clone** | A copy of a repo **on a computer** (yours, or an online one). In this dojo the online workspace (Codespace) does the cloning for you. |

You cannot save changes in the original repo. That is why you first create **your own copy** (Part 3).

## 3. Get your own copy (fork) and open it in the browser
1. Open the dojo repository: `https://github.com/ghisdubreuil/ai-dojo`. Sign in if asked.
2. At the top right of the page, click the **Fork** button.
   - ✅ A page titled **Create a new fork** opens.
3. Leave the name as `ai-dojo`. Under **Owner**, make sure your own account is selected.
4. Click **Create fork**.
   - ✅ After a few seconds you land on a page whose address looks like `https://github.com/YOUR-USERNAME/ai-dojo`, with "forked from ghisdubreuil/ai-dojo" under the title.
   - 🆘 If the **Fork** button is greyed out or an error says forking is not allowed: your organisation restricts it. Ask the organiser to give you a copy instead (see "If you cannot fork" below).
5. **Bookmark this page.** It is your own copy: `https://github.com/YOUR-USERNAME/ai-dojo`.
6. Click the green **Code** button, then the **Codespaces** tab, then **Create codespace on main**.
   - ✅ A new tab opens, builds your workspace for 1 to 3 minutes, then shows an editor in your browser.
7. Test Copilot: press `Ctrl + Alt + I` (Mac: `Control + Command + I`), type `Hello`, and press **Enter**.
   - ✅ Copilot answers. **You are ready.** Stop here and continue with the [setup guide](./02-setup-click-by-click.md) on the day.
   - 🆘 If no chat opens or Copilot does not answer, see Part 6.

> **Coming back later:** go to `https://github.com/codespaces`. Your workspace is listed there: click its name to reopen it. Your files and your work are still there. Workspaces stop after a period of inactivity (your work is kept) and may be deleted after a long time unused.

### If you cannot fork
Ask the organiser to do one of these:
- create a **template repository** in the organisation and give you access, then use the green **Use this template** button, then **Create a new repository**;
- or create a copy of the repository **inside the organisation** for each participant, then use that copy in Part 3 step 6.

## 4. Choose how to work from the web
There are three ways to use Copilot from a browser. For this dojo, use **Codespaces**.

| | **Codespaces** ✅ recommended | **github.dev** (the lightweight editor) | **Copilot on github.com** |
|---|---|---|---|
| **How to open** | **Code → Codespaces → Create codespace** | On your repo page, press the `.` key (or replace `github.com` with `github.dev` in the address bar) | Go to https://github.com/copilot |
| **What it is** | A complete VS Code in your browser, with a terminal | A light editor to read and edit files | A chat page on GitHub, tied to your repos |
| **Run code** | Yes | **No** (no terminal, no run) | No |
| **Copilot Chat with modes (Ask, Plan, Agent)** | Yes | Not confirmed in GitHub's documentation: check on your side | Chat only; it can start a cloud agent session when you ask it to create a pull request or research a repository |
| **Good for** | **All levels, all adventures** | Quickly reading or fixing a document | Quick questions about your repo, as a backup |

### Which one when
- **Default:** Codespaces. Every adventure is written for it.
- **If Codespaces is blocked** for you (policy or quota): you can still do the *reading* part of Discovery adventures with Copilot on github.com. Open your repo, ask Copilot about the documents, and check the answers in the files on GitHub. Several click-by-click steps will differ, so tell the organiser to adapt.
- **github.dev** is handy to correct a typo in a document, but it cannot run the scripts of the Builder and Expert levels. If you press `.` by mistake, nothing is lost: close the tab.

### Working on GitHub.com: a few useful facts
- Copilot Chat is available from any page on GitHub, and can be used in the context of a repository, an issue or a pull request.
- You can upload images and PDFs to the chat (drag them in, or use **Upload from computer**).
- Copilot Chat keeps your recent conversations (up to 100, for 28 days).

## 5. Working with the original repo on your computer (optional, for the curious)
You do **not** need this for the dojo. If you want a local copy later:
1. Install **Git** and **Visual Studio Code**, and install the **GitHub Copilot** extension in VS Code.
2. On your fork's page, click **Code → Local** and copy the HTTPS address.
3. In VS Code: **View → Command Palette → Git: Clone**, paste the address, choose a folder, and click **Open**.
4. Run `pip install -r requirements.txt` in the VS Code terminal for the Builder and Expert adventures (Python 3.10 or later required).

## 6. Troubleshooting
| Problem | What to try |
|---|---|
| No **Codespaces** tab, or "Codespaces is disabled" | Your organisation may have turned it off. Ask the organiser. |
| "You've reached your Codespaces limit" or a quota message | Free personal accounts have a monthly allowance. Ask the organiser whether the organisation can pay for usage, or share a workspace. |
| The Codespace opens but there is no chat icon | Wait one minute (extensions load), then reload the browser tab. |
| Chat says "Sign in to use Copilot" | Click the button and sign in with the GitHub account that has Copilot. |
| "Copilot is not available for your account" | Check https://github.com/settings/copilot. If no seat appears, ask the organiser to assign one. |
| Copilot stops answering mid-dojo | You may have used the monthly allowance (Free plan). Ask the organiser for a seat, or continue the next day. |
| Single sign-on (SSO) screen asks you to authorise | Click **Authorize** and sign in with your company credentials. |
| I forgot where my workspace is | Go to https://github.com/codespaces. |

## 7. For the facilitator: before the day
- ☐ Confirm every participant has a **Copilot seat** (or a plan that covers the session) and that **Codespaces** are enabled and funded for them.
- ☐ Decide: participants **fork** this repo, or you provide a **template** or a per-participant copy. If you want a template, open the repo's **Settings** and tick **Template repository**.
- ☐ Ask everyone to complete Part 3 **one day before**, and to reply "OK" once Copilot answered "Hello". Fix blockers in advance.
- ☐ Do a full dry run yourself (Part 3, the setup guide, the warm-up, one Discovery adventure) and note any label that differs.
- ☐ Optional: ask your GitHub administrator about Codespaces **prebuilds** to shorten the waiting time at startup.
- ☐ Prepare a backup plan for people who cannot get a Codespace: pair them with a neighbour, or use Copilot on github.com for the reading adventures.

Next: [Introduction to Copilot](./01-getting-started-with-copilot.md), then the [click-by-click setup](./02-setup-click-by-click.md).
