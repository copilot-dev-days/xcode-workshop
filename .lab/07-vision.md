# Part 7: Copilot Vision (Optional)

[📚 Lab Guide](GUIDE.md) • [← MCP Server](06-mcp.md)

---

**Goal**: Use Copilot Vision to generate code from UI designs and screenshots.

> **Note**: Copilot Vision may require specific feature flags or preview access. Check if it's available in your Copilot for Xcode installation.

---

## What is Copilot Vision?

Copilot Vision enables the AI to "see" and understand visual content like UI mockups, screenshots, and design files. You can upload images directly in the chat, and Copilot will generate code that matches the design.

---

## Scenario

Create a new custom landmark card component from a design mockup.

---

## Steps

1. **Prepare your design**: Take a screenshot or find a design mockup of a card UI you want to implement (e.g., a modern card with image, title, subtitle, and action buttons)

2. **Create a new Swift file**:
   - In Xcode, right-click on `Landmarks/Views` folder
   - Select **New File → SwiftUI View**
   - Name it `LandmarkCard.swift`

3. **Open Copilot Chat** panel in Agent mode

4. Click the **Attach Image** button (📎 icon) and upload your design mockup

5. Enter a prompt like:

```
Create a new SwiftUI view called LandmarkCard based on this design mockup.
The card should:
- Display a landmark image at the top
- Show the landmark name and location
- Include a favorite button
- Use the app's existing color scheme and follow iOS design guidelines
- Be reusable with any Landmark model
Make it responsive for different screen sizes.
```

6. Copilot will analyze the image and generate SwiftUI code in the new file

7. Review the generated code and test it by:
   - Adding a preview at the bottom of the file
   - Using it in `LandmarkList` to replace existing row views

---

## Example Prompts with Vision

- `Create this card component in SwiftUI with proper spacing, shadows, and rounded corners`
- `Build a settings panel based on this screenshot, matching the iOS native style`

---

## 💡 Tips for Better Results

- Use clear, high-resolution images or screenshots
- Provide specific requirements (colors, fonts, spacing)
- Mention the data model to use (e.g., "use the Landmark model")
- Specify platform requirements (iOS version, device sizes)
- Request specific SwiftUI features if needed (LazyVGrid, GeometryReader, etc.)

---

## Try More

- Create a custom detail header based on a design mockup
- Implement a statistics dashboard view from an image
- Build a custom filter/sort menu UI from a screenshot

---

## ✅ Part 7 Complete!

You've learned how to:
- Upload design mockups to Copilot Chat
- Generate SwiftUI code from visual designs
- Iterate on vision-generated code for better results

---

[📚 Lab Guide](GUIDE.md) • [← MCP Server](06-mcp.md)

👉 **[Continue to Part 8: Best Practices, Tips & Resources →](08-tips-and-resources.md)**
