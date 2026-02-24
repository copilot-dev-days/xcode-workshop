# Part 5: Plan Agent — Breaking Down Complex Tasks

[📚 Lab Guide](GUIDE.md) • [← Agent Mode](04-agent-mode.md)

---

**Goal**: Use Plan Agent to decompose large features into manageable steps.

**Scenario**: Add user authentication to the app.

---

## Steps

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

---

## Benefits of Plan Agent

- Breaks down complex features into actionable steps
- Helps you understand the architecture before coding
- Identifies dependencies and potential issues early
- Provides a roadmap you can follow incrementally

---

## ✅ Part 5 Complete!

You've learned how to:
- Use Plan mode to decompose complex features
- Review and refine AI-generated plans
- Execute plans step by step
