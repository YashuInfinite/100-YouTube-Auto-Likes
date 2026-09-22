# 100-YouTube-Auto-Likes

A Python and Selenium browser-automation project for testing YouTube Like interactions across multiple signed-in accounts using a local Chrome debugging session.

## ⚠️ Important Notice

This project is provided for **educational and testing purposes**.

Automating engagement across multiple accounts can violate YouTube's Terms of Service and may result in likes being removed, accounts being restricted, or other platform enforcement. Use this project only with accounts and environments you are authorized to automate.

---

## 📺 Video Tutorial

Watch the tutorial for the complete setup and demonstration:

https://www.youtube.com/watch?v=FVumnHy5Tzo&t=1s&ab_channel=HelloWorld

Watch up to approximately **3 minutes and 46 seconds** for the relevant setup and implementation details.

---

## ✨ Features

* 🐍 Python-based automation
* 🤖 Selenium WebDriver
* 🌐 Local Chrome debugging session
* ▶️ Supports YouTube videos
* 📱 Supports YouTube Shorts through the corresponding script
* 🔄 Demonstrates switching between multiple signed-in accounts
* 👍 Automates interaction with the YouTube Like button
* 🖥️ Runs locally on Windows

---

## 📁 Project Structure

```text
100-Youtube-Auto-Likes-Using-Localhost/
│
├── video.py
├── shorts.py
└── README.md
```

### `video.py`

Used for the regular YouTube video workflow.

### `shorts.py`

Used for the YouTube Shorts workflow.

---

# 🛠️ Setup

## 1. Locate Chrome

First, locate your Chrome installation directory.

A typical Windows installation may be:

```text
C:\Users\<USERNAME>\AppData\Local\Google\Chrome\Application
```

For example:

```text
C:\Users\Hp\AppData\Local\Google\Chrome\Application
```

Your Chrome installation path may be different.

---

## 2. Open Command Prompt

Press:

```text
Windows Key
```

Search for:

```text
cmd
```

and open Command Prompt.

Navigate to your Chrome installation directory:

```bash
cd C:\Users\Hp\AppData\Local\Google\Chrome\Application
```

Replace the path with your own Chrome installation path.

---

## 3. Start Chrome With Remote Debugging

Launch Chrome with remote debugging enabled:

```bash
chrome.exe --remote-debugging-port=9222 --user-data-dir="YOUR_LOCALHOST_PROFILE_PATH"
```

Example:

```bash
chrome.exe --remote-debugging-port=9222 --user-data-dir="C:\Users\Hp\Desktop\Bots\Chromedriver\Localhost"
```

### What this does

The `--remote-debugging-port=9222` option allows Selenium to connect to the Chrome session.

The `--user-data-dir` option specifies the Chrome profile directory used for the automation session.

> Replace `YOUR_LOCALHOST_PROFILE_PATH` with a directory that you control.

---

# 🐍 4. Install Selenium

Open a new terminal in your project directory.

Install the required Selenium version:

```bash
pip install selenium==4.2.0
```

Verify the installed version:

```bash
python -c "import selenium; print(selenium.__version__)"
```

---

# 🔐 5. Browser Account Setup

Sign in to the YouTube accounts you are authorized to use in the Chrome profile.

The original project uses multiple accounts and Brand Accounts to demonstrate repeated account switching.

Make sure that you only automate accounts that you own or have explicit authorization to use.

---

# 🔗 6. Configure the Video URL

Open `video.py` and locate the YouTube URL.

Replace it with the URL of the video you want to test.

Example:

```python
driver.get("https://www.youtube.com/watch?v=YOUR_VIDEO_ID")
```

For YouTube Shorts, configure the corresponding URL in:

```text
shorts.py
```

---

# ▶️ 7. Run the Script

For a regular YouTube video:

```bash
python video.py
```

For a YouTube Short:

```bash
python shorts.py
```

The script connects to the previously launched Chrome debugging session and performs the configured browser interactions.

---

# 🔄 How the Automation Works

The general workflow is:

```text
Start Chrome
      ↓
Enable Remote Debugging
      ↓
Connect Selenium
      ↓
Open YouTube Video
      ↓
Interact With Like Button
      ↓
Open Account Menu
      ↓
Switch Account
      ↓
Repeat Configured Workflow
```

The automation relies on YouTube's current page structure and element selectors.

---

# 🧩 YouTube UI Changes

YouTube regularly changes its website structure.

If an existing selector stops working, the corresponding Selenium locator may need to be updated.

For development and debugging, inspect the page using your browser's Developer Tools:

```text
Ctrl + Shift + C
```

Then inspect the relevant element and update the Selenium locator in the script.

> Avoid relying on long absolute XPath expressions where possible. Stable attributes, semantic selectors, or relative XPath expressions are generally easier to maintain.

---

# ⚠️ Selenium Version

The original project was written around:

```text
Selenium 4.2.0
```

If you experience compatibility problems with the existing code, check the installed Selenium version:

```bash
python -c "import selenium; print(selenium.__version__)"
```

To remove the existing version:

```bash
pip uninstall selenium
```

Then install the project version:

```bash
pip install selenium==4.2.0
```

---

# 🛡️ Responsible Use

This repository is intended to demonstrate:

* Selenium browser automation
* Chrome remote debugging
* Browser profile management
* Account-switching workflows
* Web UI interaction
* Maintaining automation scripts when websites change

Do not use the project to:

* manipulate engagement metrics,
* evade platform enforcement,
* automate accounts you do not control,
* bypass security mechanisms,
* or violate platform policies.

---

# 📌 Disclaimer

This project is provided **for educational and testing purposes only**.

The author does not encourage misuse of the software or violation of YouTube's policies, applicable laws, or the rights of other users.

You are responsible for how you use this code and for ensuring that your use complies with the applicable platform rules and laws.

---

Built with:

```text
Python + Selenium + Chrome
```

---

## ⭐ Support the Project

If you found the project useful for learning Selenium and browser automation, consider giving the repository a ⭐ on GitHub.

---

## 🔧 Future Improvements

Possible improvements for legitimate testing environments include:

* Better Selenium selectors
* Explicit waits instead of fixed delays
* Error handling and logging
* Configurable browser profiles
* Headless testing for non-engagement workflows
* Automated test reports
* Page-object architecture
* Support for automated UI regression testing

---

**Educational project for Selenium and browser automation.**
