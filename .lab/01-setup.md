# Part 1: Prerequisites & Setup

[📚 Lab Guide](GUIDE.md) • [← Overview](00-overview.md)

---

Before starting the workshop, ensure you have:

- **Xcode 15 or later** installed
- **GitHub Copilot for Xcode** extension ([Download here](https://github.com/github/CopilotForXcode/releases))
- Signed in to **GitHub Copilot** in Xcode with your GitHub account

---

## 🔧 Installation & Setup

### Step 1: Install GitHub Copilot for Xcode

Download the latest `.dmg` from the [releases page](https://github.com/github/CopilotForXcode/releases) and drag the app into **Applications**.

### Step 2: Background Item

A background item will be added to enable the GitHub Copilot for Xcode extension app to connect to the host app. This permission is usually automatically added when first launching the app.

### Step 3: Grant Required Permissions

Grant the required permissions: **Background**, **Accessibility**, and **Xcode Source Editor Extension**.

- **Background**: Done in the previous step.
- **Accessibility**: The first time the application runs, a permission prompt will appear.
- **Xcode Source Editor Extension**: This must be enabled manually. Click **Extension Permission** from the GitHub Copilot for Xcode application settings to open the System Preferences to the Extensions panel. Select **Xcode Source Editor** and enable **GitHub Copilot**.

### Step 4: Sign In to GitHub Copilot

**Option A (menu bar)**
1. Click the **Copilot** icon in the macOS menu bar
2. Choose **Sign in to GitHub Account**
3. Authorize in the browser when prompted

**Option B (app → chat panel)**
1. Run the **GitHub Copilot for Xcode** app
2. In the Copilot Chat panel that appears, click **Sign in**
3. Authorize in the browser when prompted

### Step 5: Open This Workshop Project

Clone this repository and open in Xcode:

```bash
git clone https://github.com/copilot-dev-days/xcode-workshop.git
cd xcode-workshop
open Landmarks.xcodeproj
```

### Step 6: Open Copilot Chat

The Copilot Chat panel should already be open by default. If you don't see it, you can open it in two ways:
- **Via Xcode menu**: Xcode → Editor → GitHub Copilot → Open Chat
- **Via GitHub Copilot app menu**: Click the menu bar icon → Open Chat

---

## ✅ Part 1 Complete!

You've set up:
- GitHub Copilot for Xcode extension
- Required permissions (Background, Accessibility, Source Editor)
- GitHub authentication
- The workshop project in Xcode with Copilot Chat open

---

[📚 Lab Guide](GUIDE.md) • [← Overview](00-overview.md)

👉 **[Continue to Part 2: Understanding Code with Copilot Chat →](02-chat.md)**
