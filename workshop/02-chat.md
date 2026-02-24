# Part 2: Understanding Code with Copilot Chat

[📚 Lab Guide](GUIDE.md) • [← Setup](01-setup.md)

---

**Goal**: Learn how to select a model and use Copilot Chat to explore codebases.

---

## Steps

1. Open the Landmarks project in Xcode
2. Navigate to **ContentView.swift**
   Path: `Landmarks/Views/ContentView.swift`
3. Open the **Copilot Chat** panel (see [Setup](01-setup.md) step 6)
4. **Select a model**: In the chat input area, look for the model selector (to the right of the wrench/settings icon), click it and choose the model you want. If **GPT-5 mini** is available, you can try that first.
   - Different models may provide different response styles and capabilities
   - You can experiment with different models to see which works best for you
5. Select **Ask** mode using the mode toggle
6. Try these prompts:
   - `Explain what this file does`
   - `What SwiftUI components are used in this view?`

---

## Expected Result

Copilot provides clear explanations of the code structure and functionality.

---

## 💡 Tips

- You can ask follow-up questions to dive deeper
- Use `@workspace` to query across the entire project
- Reference specific code by selecting it before asking
- Try switching between different models to compare their responses

---

## ✅ Part 2 Complete!

You've learned how to:
- Select and switch between AI models
- Use Ask mode to explore codebases
- Ask follow-up questions for deeper understanding
- Use `@workspace` for project-wide queries
