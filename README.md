# Landmarks — GitHub Copilot for Xcode Workshop

[📚 Lab Guide](workshop/GUIDE.md)

---

> **Quick Reference Guide** — For detailed instructions, see the individual parts below.

---

## 📚 Lab Parts

| Part | Title |
|------|-------|
| [**00**](workshop/00-overview.md) | Overview & Checklist |
| [**01**](workshop/01-setup.md) | Prerequisites & Setup |
| [**02**](workshop/02-chat.md) | Understanding Code with Copilot Chat |
| [**03**](workshop/03-completion.md) | Code Completion with Inline Suggestions |
| [**04**](workshop/04-agent-mode.md) | Agent Mode — Multi-File Refactoring |
| [**05**](workshop/05-plan-agent.md) | Plan Agent — Breaking Down Complex Tasks |
| [**06**](workshop/06-mcp.md) | GitHub MCP Server Integration |
| [**07**](workshop/07-vision.md) | Copilot Vision (Optional) |
| [**08**](workshop/08-tips-and-resources.md) | Best Practices, Tips & Resources |

> 📝 Lab guides are also available in the [`workshop/`](workshop/) folder for offline reading.

---

## About This Project

This repository contains a simple SwiftUI demo app based on [Apple's SwiftUI tutorial](https://developer.apple.com/tutorials/swiftui/creating-and-combining-views). It is designed as a **hands-on workshop** to help you master **GitHub Copilot for Xcode** through practical exercises.

## Prerequisites

- **Xcode 15 or later** installed
- **GitHub Copilot for Xcode** extension ([Download here](https://github.com/github/CopilotForXcode/releases))
- Signed in to **GitHub Copilot** in Xcode with your GitHub account

## Quick Start

```bash
git clone https://github.com/copilot-dev-days/xcode-workshop.git
cd xcode-workshop
open Landmarks.xcodeproj
```

## Running Tests

Press **Cmd + U** in Xcode, or via command line:

```bash
xcodebuild test -scheme Landmarks -destination 'platform=iOS Simulator,name=iPhone 15'
```
