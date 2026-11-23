# App tour, click by click (15 minutes)

Do this on the day of the dojo, once. It assumes you completed the [prerequisites](./00-prerequisites.md): the app is installed, you are signed in, and your copy of the project (`ai-dojo`) is added.

> **About this guide.** Labels in the app can change. Every step has a **✅ You should see** check and a **🆘 If not** fallback. If your screen differs slightly, look for the closest match, or ask your facilitator.
> **Convention:** **bold** = something to click or a label on screen. `code style` = something to type or copy-paste exactly.

---

## Part 1 — Meet the sidebar
1. Open the **GitHub Copilot** app.
   - ✅ The main screen opens, with a **sidebar** on the left.
2. Look at the sidebar. The items you will use:
   | Item | What it is |
   |---|---|
   | **New** | Starts a new agent session. |
   | **Sessions** | Your connected projects and their sessions. A **+** control next to it starts a new session or adds a project. |
   | **Chats** | General conversations without a workspace. |
   | **Issues**, **Pull requests** | Work items from GitHub (used in adventure C3). |
   | **Customize** | Skills, plugins and tools. |
3. Under **Sessions**, check that `ai-dojo` is listed.
   - 🆘 If not, redo Part 5 of the prerequisites.

---

## Part 2 — Start a session (your daily gesture)
1. In the sidebar, click the **new session** control next to **Sessions** (a **+** icon).
2. Under **Start session in**, click `ai-dojo`.
   - ✅ A screen with a **prompt box** appears, with drop-downs below it.
3. Below the prompt box, check the **Environment** drop-down. It must say **This computer**. If not, click it and choose **This computer**.
4. Check the **Workspace** drop-down. It must say **Current checkout**. If not, click it and choose **Current checkout**.
5. Click the **mode** drop-down (it may read **Interactive**, **Plan** or **Autopilot**) and choose **Interactive**.
6. In the same menu, move your mouse over **Tool permissions** and click **Assisted**.
   - ✅ The setting is now **Assisted**.
   - 🚫 Do not choose **Approve all**.
7. Leave the **model** and **reasoning effort** drop-downs as they are.

---

## Part 3 — Send your first message
1. Click inside the prompt box.
2. Paste the safety sentence:
   ```
   Rule for this session: do not create, modify or delete any file unless I explicitly ask you to. Answer only from the project files.
   ```
3. Press **Enter**.
   - ✅ Copilot confirms it understood.
4. Type: `What can you tell me about this project in three sentences?` and press **Enter**.
   - ✅ Words appear gradually: Copilot is reading the project and answering. Wait until it stops.
   - If a **permission request** appears (Copilot wants to read files or run something): read it, then allow it if it is about reading the project's files. See the permission rules in the [introduction](./01-getting-started-with-copilot.md#tool-permissions).

---

## Part 4 — Point Copilot to a file with `@`
1. In the prompt box, type `@`.
   - ✅ A list of files pops up.
2. Type a few letters, for example `products`.
3. Click `products.csv` in the list (or use the arrow keys and press **Enter**).
   - ✅ The file is attached to your message.
4. Type your question after it, for example: `What does each column mean?` and press **Enter**.
   - 🆘 If no list appears, type the path yourself: `data/products.csv`.

---

## Part 5 — Find your project folder and open files on your computer
The app focuses on conversation: to **look at the files yourself** (and verify Copilot), you open them with your computer's normal programs.
1. In your session, type and send:
   ```
   What is the full path of this project folder on my computer? Give me only the path.
   ```
2. Copy the path Copilot gives you.
3. Open the folder:
   - **Windows:** open **File Explorer**, click in the address bar at the top, paste the path, press **Enter**.
   - **macOS:** in **Finder**, press `Shift + Command + G`, paste the path, press **Enter**.
4. ✅ You see the folders `Adventures`, `data`, `docs`, `my-work`.
5. **Pin the folder** so you can come back: Windows, right-click the folder → **Pin to Quick access**; macOS, drag the folder to the Finder sidebar.
6. To open a file:
   - **CSV files** (`data/*.csv`): double-click. They open in a spreadsheet program (Excel, Numbers). Look, but do not save changes.
   - **Markdown files** (`.md`) and other text files: right-click → **Open with** → **Notepad** (Windows) or **TextEdit** (macOS).
   - 🆘 If a program asks to convert or repair a CSV: cancel, and keep the file untouched.

---

## Part 6 — Check what Copilot changed
1. Above the prompt box, click **Changes**.
   - ✅ It shows the differences made to your project. In a read-only task it should be **empty**.
2. If you see a change you did not ask for: type `Undo your changes to that file.` and press **Enter**, then check **Changes** again.

---

## Part 7 — Useful habits
| I want to… | Do this |
|---|---|
| **Start fresh** on a new topic | Click the **+** next to **Sessions** and start a new session (repeat Parts 2 and 3). |
| **Brainstorm without a workspace** | Use **Chats** in the sidebar. |
| **Ask a follow-up** | Type in the same prompt box: "shorter", "as a table", "explain step 2". |
| **See keyboard shortcuts** | In the app menu bar: **Help → Keyboard Shortcuts**. |
| **Tidy up** | Right-click a chat → **Archive chat**. For sessions: app **Settings → Sessions → Manage sessions**. |
| **Have Copilot create a file** | Ask in plain words: "Save this as `my-work/email.md`." Then check **Changes**. |

## You are ready
Go to the [warm-up adventure](../Adventures/StartHere.md).
