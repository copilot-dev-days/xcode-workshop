# Part 4: Agent Mode — Multi-File Refactoring

[📚 Lab Guide](GUIDE.md) • [← Completion](03-completion.md)

---

**Goal**: Use Agent Mode to make changes across multiple files automatically.

**Scenario**: Update the favorite indicator throughout the app to use heart icons.

---

## Steps

1. Open **LandmarkList.swift**
   Path: `Landmarks/Views/Landmarks/LandmarkList.swift`
2. Open the **Preview Canvas** to see the current UI (Cmd + Option + Enter)
3. Switch to **Agent** mode in the Copilot Chat panel
4. Enter this prompt:

```
Update all favorite buttons to use heart-shaped icons (filled heart for favorited,
outline heart for not favorited) across all views in the project.
```

5. Copilot will analyze the codebase and propose changes to multiple files
6. Review the proposed changes in the diff view
7. Check the Preview Canvas to see the updated UI

---

## What Happened?

- Agent Mode identified all files with favorite functionality
- It updated icons consistently across `LandmarkRow`, `LandmarkDetail`, and other views
- Changes were made simultaneously across multiple files

---

## Try More Complex Tasks (Optional)

- `Add a rating system (1-5 stars) to landmarks with mock data`
- `Implement a dark mode toggle in the settings view`
- `Add categories filter chips at the top of the landmark list`

---

## ✅ Part 4 Complete!

You've learned how to:
- Use Agent Mode for multi-file refactoring
- Review proposed changes in the diff view
- Verify changes with the Preview Canvas
