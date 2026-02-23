# Landmarks - GitHub Copilot for Xcode Workshop

This repository contains a simple SwiftUI demo app based on [Apple's SwiftUI tutorial](https://developer.apple.com/tutorials/swiftui/creating-and-combining-views). It is designed as a **hands-on workshop** to help you master
**GitHub Copilot for Xcode** through practical exercises.

## What You'll Learn

- **Code Completion**: Get intelligent inline suggestions as you type
- **Copilot Chat**: Ask questions about your codebase and get instant answers
- **Agent Mode**: Multi-file refactoring and complex code generation
- **Plan Agent**: Break down complex tasks into actionable steps
- **MCP Servers**: Extend Copilot with GitHub integration
- **Copilot Vision** (optional): UI-aware code generation

---

## Prerequisites


Before starting the workshop, ensure you have:

- **Xcode 15 or later** installed
- **GitHub Copilot for Xcode** extension ([Download here](https://github.com/github/CopilotForXcode/releases))
- Signed in to **GitHub Copilot** in Xcode with your GitHub account

### Installation & Setup

#### 1. Install GitHub Copilot for Xcode

Download the latest `.dmg` from the [releases page](https://github.com/github/CopilotForXcode/releases) and drag the app into **Applications**.

#### 2. Background Item

A background item will be added to enable the GitHub Copilot for Xcode extension app to connect to the host app. This permission is usually automatically added when first launching the app.

#### 3. Grant Required Permissions

Grant the required permissions: **Background**, **Accessibility**, and **Xcode Source Editor Extension**.

- **Background**: Done in the previous step.
- **Accessibility**: The first time the application runs, a permission prompt will appear.
- **Xcode Source Editor Extension**: This must be enabled manually. Click **Extension Permission** from the GitHub Copilot for Xcode application settings to open the System Preferences to the Extensions panel. Select **Xcode Source Editor** and enable **GitHub Copilot**.

#### 5. Sign In to GitHub Copilot

**Option A (menu bar)**
1. Click the **Copilot** icon in the macOS menu bar
2. Choose **Sign in to GitHub Account**
3. Authorize in the browser when prompted

**Option B (app → chat panel)**
1. Run the **GitHub Copilot for Xcode** app
2. In the Copilot Chat panel that appears, click **Sign in**
3. Authorize in the browser when prompted

#### 6. Open This Workshop Project

Clone this repository and open in Xcode:

```bash
git clone https://github.com/copilot-dev-days/xcode-workshop.git
cd copilot-xcode-workshop
open Landmarks.xcodeproj
```

#### 8. Open Copilot Chat

The Copilot Chat panel should already be open by default. If you don't see it, you can open it in two ways:
- **Via Xcode menu**: Xcode → Editor → GitHub Copilot → Open Chat
- **Via GitHub Copilot app menu**: Click the menu bar icon → Open Chat


---

## Workshop Exercises

### Exercise 1: Understanding Code with Copilot Chat

**Goal**: Learn how to select a model and use Copilot Chat to explore codebases.

**Steps**:

1. Open the Landmarks project in Xcode
2. Navigate to **ContentView.swift**
   Path: `Landmarks/Views/ContentView.swift`
3. Open the **Copilot Chat** panel (see  **Installation & Setup** step)
4. **Select a model**: In the chat input area, look for the model selector (to the right of the wrench/settings icon), click it and choose the model you want. If **GPT-5 mini** is available, you can try that first.
   - Different models may provide different response styles and capabilities
   - You can experiment with different models to see which works best for you
5. Select **Ask** mode using the mode toggle
6. Try these prompts:
   - `Explain what this file does`
   - `What SwiftUI components are used in this view?`
 
**Expected Result**: Copilot provides clear explanations of the code structure and functionality.

**Tips**:
- You can ask follow-up questions to dive deeper
- Use `@workspace` to query across the entire project
- Reference specific code by selecting it before asking
- Try switching between different models to compare their responses

---

### Exercise 2: Code Completion with Inline Suggestions

**Goal**: Experience AI-powered code completion while writing Swift code.

**Scenario**: Add a description field to the landmark row display.

**Steps**:

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

**Try More**:
- Add a comment for a date formatter
- Write a comment to create a computed property for landmark categories
- Start typing a function name and let Copilot complete the implementation

---

### Exercise 3: Agent Mode - Multi-File Refactoring

**Goal**: Use Agent Mode to make changes across multiple files automatically.

**Scenario**: Update the favorite indicator throughout the app to use heart icons.

**Steps**:

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

**What Happened?**
- Agent Mode identified all files with favorite functionality
- It updated icons consistently across `LandmarkRow`, `LandmarkDetail`, and other views
- Changes were made simultaneously across multiple files

**Try More Complex Tasks** (Optional):
- `Add a rating system (1-5 stars) to landmarks with mock data`
- `Implement a dark mode toggle in the settings view`
- `Add categories filter chips at the top of the landmark list`

---

### Exercise 4: Plan Agent - Breaking Down Complex Tasks

**Goal**: Use Plan Agent to decompose large features into manageable steps.

**Scenario**: Add user authentication to the app.

**Steps**:

1. Open the Copilot Chat panel
2. In the Copilot Chat panel, use the mode dropdown to select **Plan**
3. Enter this prompt:

```
I want to add user authentication to this app. Users should be able to:
- Sign up with email and password
- Log in and log out
- See personalized favorite landmarks
Create a plan for implementing this feature.
```

4. Copilot will generate a step-by-step implementation plan:
   - Create User model and authentication service
   - Add login/signup views
   - Implement session management
   - Update data models to associate favorites with users
   - Add authentication state to the app

5. Review the plan and ask for clarification if needed
6. Execute the plan step by step, or ask Copilot to implement specific steps

**Benefits of Plan Agent**:
- Breaks down complex features into actionable steps
- Helps you understand the architecture before coding
- Identifies dependencies and potential issues early
- Provides a roadmap you can follow incrementally


---

### Exercise 5: GitHub MCP Server Integration

**Goal**: Extend Copilot with GitHub integration using MCP (Model Context Protocol).

**What is MCP?**
MCP allows Copilot to interact with external tools and services. The GitHub MCP Server lets Copilot access your repositories, issues, pull requests, and more directly from the chat.

#### Setup GitHub MCP Server

1. Open the **Copilot Chat** panel
2. Click the **wrench** icon to open Settings (it opens the **Tools** tab)
3. In the MCP settings:
   - Click **Browse MCP Servers**
   - Find and select **GitHub** from the registry
   - Click **Install**
4. Authenticate with GitHub when prompted
5. Select the GitHub account/organization you want to grant access to
6. In the **Tools** tab, the **Available MCP Tools** list will update automatically—confirm the GitHub MCP Server appears there

#### Using GitHub MCP Server

Once the GitHub MCP Server is installed, try these prompts in Copilot Chat (Ask or Agent mode):

**Query 1: List Your Repositories**
```
List all repositories in my GitHub account
```

**Query 2: Check Pull Requests**
```
What are the open pull requests in this project?
```

**More Things You Can Try** (Optional):
- `Show me recent issues in the <repository-name> repository`
- `Generate release notes from commits`

---

### Exercise 6: Copilot Vision (Optional)

**Goal**: Use Copilot Vision to generate code from UI designs and screenshots.

**Note**: Copilot Vision may require specific feature flags or preview access. Check if it's available in your Copilot for Xcode installation.

**What is Copilot Vision?**
Copilot Vision enables the AI to "see" and understand visual content like UI mockups, screenshots, and design files. You can upload images directly in the chat, and Copilot will generate code that matches the design.

**Scenario**: Create a new custom landmark card component from a design mockup.

**Steps**:

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

**Example Prompts with Vision**:
- `Create this card component in SwiftUI with proper spacing, shadows, and rounded corners`
- `Build a settings panel based on this screenshot, matching the iOS native style`

**Tips for Better Results**:
- Use clear, high-resolution images or screenshots
- Provide specific requirements (colors, fonts, spacing)
- Mention the data model to use (e.g., "use the Landmark model")
- Specify platform requirements (iOS version, device sizes)
- Request specific SwiftUI features if needed (LazyVGrid, GeometryReader, etc.)

**Try More**:
- Create a custom detail header based on a design mockup
- Implement a statistics dashboard view from an image
- Build a custom filter/sort menu UI from a screenshot

---

## Best Practices & Tips

### Getting Better Suggestions

1. **Write Clear Comments**: Use descriptive comments before functions to guide Copilot
   ```swift
   // Function to validate email format using regex, returns true if valid
   func validateEmail(_ email: String) -> Bool {
   ```

2. **Use Descriptive Names**: Well-named variables and functions help Copilot understand context
   ```swift
   // Good: Copilot understands what you need
   let filteredLandmarksByCategory =

   // Less clear
   let filtered =
   ```

3. **Provide Examples**: Show Copilot what you want with an example
   ```swift
   // Example: formatDate("2024-01-15") returns "Jan 15, 2024"
   func formatDate(_ dateString: String) -> String {
   ```

### Working with Agent Mode

- **Be Specific**: Instead of "improve this code", say "add error handling and input validation"
- **Break Down Tasks**: Large features work better as multiple smaller prompts
- **Review Changes**: Always review multi-file changes before accepting
- **Iterate**: If the result isn't perfect, provide feedback and ask for adjustments

### Chat Effectively

- **Select Context**: Select relevant code before asking questions
- **Use Slash Commands** (if available):
  - `/explain` - Explain selected code
  - `/fix` - Fix issues in selected code
  - `/tests` - Generate unit tests
  - `/doc` - Generate documentation
- **Ask Follow-ups**: Treat it like a conversation with a senior developer


## Troubleshooting

Please refer to the official guide:
- [TROUBLESHOOTING.md](https://github.com/github/CopilotForXcode/blob/main/TROUBLESHOOTING.md)

---

## Additional Resources

- [GitHub Copilot for Xcode Documentation](https://github.com/github/CopilotForXcode)
- [GitHub Copilot Documentation](https://docs.github.com/copilot)
- [Apple SwiftUI Tutorials](https://developer.apple.com/tutorials/swiftui)
- [Model Context Protocol (MCP) Specification](https://modelcontextprotocol.io/)

---

## Running Tests

This app uses XCTestPlans for organizing and running tests.

**Run tests in Xcode**: Press **Cmd + U**

**Run tests via command line**:
```bash
xcodebuild test -scheme Landmarks -destination 'platform=iOS Simulator,name=iPhone 15'
```

---

## Workshop Completion Checklist

After completing this workshop, you should be able to:

- [ ] Use Copilot Chat to understand and explore codebases
- [ ] Accept and use inline code suggestions effectively
- [ ] Apply Agent Mode for multi-file refactoring
- [ ] Break down complex features with Plan Agent
- [ ] Set up and use MCP servers (GitHub integration)
- [ ] (Optional) Generate code from UI mockups with Copilot Vision
- [ ] Write better prompts for more accurate suggestions
- [ ] Generate unit tests with Copilot
- [ ] Debug issues using Copilot's help

---

## Next Steps

Now that you've completed the workshop, try using Copilot in your own projects:

1. **Start Small**: Use inline suggestions for routine coding tasks
2. **Ask Questions**: Use chat to understand unfamiliar codebases
3. **Refactor Confidently**: Use Agent Mode for large-scale changes
4. **Iterate**: Don't expect perfection on the first try - refine your prompts
5. **Stay in Flow**: Let Copilot handle boilerplate so you focus on architecture

**Remember**: Copilot is a tool to augment your skills, not replace them. Always review generated code for correctness, security, and adherence to your project's standards.

---

## Feedback & Contributions

Found issues or have suggestions for improving this workshop?

- Open an issue in this repository
- Submit a pull request with improvements
- Share your experience and learnings with the community

**For GitHub Copilot for Xcode feedback**: Visit the [official repository](https://github.com/github/CopilotForXcode)

Happy coding with GitHub Copilot for Xcode! 🚀




