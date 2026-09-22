# KeyNest

A small Chrome extension that stores your passwords locally, encrypted, with two separate vaults.

Built for personal use, and for IT teams or managers who need to share passwords with people on their team without ever handing over the actual password.

**Website and download:** https://github.com/adarshclarity-byte/keynest

**Contact:** adarsh.clarity@gmail.com


## What it does

You install the extension. You pick a master password. From then on, KeyNest saves logins you type into sign-up forms and fills them back in when you visit those sites again.

Your vault is encrypted with AES-GCM. The key is derived from your password using PBKDF2 with 250,000 rounds. Everything sits inside `chrome.storage.local` on your own machine. There is no server. There is no account. Nothing calls home.


## Two vaults

When you set it up, you can create two vaults instead of one. They live side by side, they have separate passwords, neither one can read the other.

**User vault**
- The regular one. You add logins, unlock with your password, view and edit what is inside.

**Admin vault** (optional)
- Meant for a manager, IT admin, parent, or shop owner.
- Set up with a second password, different from the user password.
- Anything saved here autofills silently on the right site.
- The user of the machine can sign in but never sees the actual password.
- To view or edit these entries, someone has to type the admin password.

Typical uses: an IT team sharing SaaS logins with employees, a manager giving a shared vendor account to teammates, a parent setting up streaming services on a family laptop.


## Installing it

1. Download the zip from the website (link above).
2. Extract it somewhere you will not accidentally delete.
3. Open `chrome://extensions` in a new tab.
4. Turn on **Developer mode** in the top-right corner.
5. Click **Load unpacked** and pick the folder you extracted. Not the zip itself, the folder inside it (the one that has `manifest.json`).
6. Pin KeyNest to your toolbar. Click the icon, set your password or passwords, done.

Chrome shows a "You have developer extensions installed" warning while developer mode is on. That is a standard Chrome notice, not something about KeyNest. You can dismiss it.


## Common questions

**Forgot the master password?**
There is no reset. Nobody has a copy. Write it on paper the first day.

**Does it sync between devices?**
No. Export from Options on one device, import on another. It is a manual copy.

**Will "Clear browsing data" in Chrome delete my vault?**
No. That dialog only clears cookies and storage for websites, not extensions.

**What actually deletes my data?**
Wiping from the Options page (you have to type DELETE), uninstalling the extension, or deleting your Chrome profile. Nothing else.

**Same password for both vaults?**
Not allowed. Setup checks and blocks it.

**Is it audited?**
No. One person built it. The code is small, feel free to read it before installing.

## Support

Run into a bug or have a question, write to **adarsh.clarity@gmail.com**.
