# Part 3: Code Completion with Inline Suggestions

[📚 Lab Guide](GUIDE.md) • [← Chat](02-chat.md)

---

**Goal**: Experience AI-powered code completion while writing Swift code.

**Scenario**: Add a description field to the landmark row display.

---

## Steps

1. Open **LandmarkRow.swift**
   Path: `Landmarks/Views/Landmarks/LandmarkRow.swift`
2. Locate the `HStack` containing the landmark name (around line 14)
3. Below the landmark name `Text` view, add this comment:

```swift
// Display the landmark description in one line; show full description on hover
```

4. Press **Enter** and wait for Copilot to suggest code
5. You should see a suggestion like:

```swift
Text(landmark.description)
    .font(.caption)
    .foregroundColor(.secondary)
    .lineLimit(1)
```

6. Press **Tab** to accept the suggestion

---

## Try More

- Add a comment for a date formatter
- Write a comment to create a computed property for landmark categories
- Start typing a function name and let Copilot complete the implementation

---

## ✅ Part 3 Complete!

You've learned how to:
- Trigger inline code suggestions with comments
- Accept suggestions with Tab
- Guide Copilot with descriptive comments
