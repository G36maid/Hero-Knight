### GitHub Branching Workflow for Hero-Knight:

1. **Main Branch:**
   - This is your stable release branch. Only tested and stable features should be merged here.
   - Typically protected, so changes to this branch must go through pull requests and reviews.

2. **Dev Branch:**
   - The **dev** branch is where active development takes place. It's a staging ground for new features before they are merged into **main**.
   - You can push the latest changes here, but they may still need further testing.

3. **Feature Branches:**
   - For each new feature or update, create a separate feature branch, for example:
     - `feature/combat-system`
     - `feature/quest-system`
     - `feature/ai-behavior`
   - After completing a feature, you can merge it into **dev** via a pull request.

4. **Testing Workflow:**
   - Set up automated tests using Unity's testing tools (like NUnit) and GitHub Actions for continuous integration.
   - When a pull request is created, GitHub Actions can automatically run tests to ensure no new bugs are introduced.

---

### Example Git Commands for Your Workflow:

1. **Creating a Dev Branch:**
   ```bash
   git checkout -b dev
   git push origin dev
   ```

2. **Creating a Feature Branch:**
   ```bash
   git checkout -b feature/combat-system
   git push origin feature/combat-system
   ```

3. **Merging a Feature into Dev:**
   After completing a feature:
   ```bash
   git checkout dev
   git merge feature/combat-system
   git push origin dev
   ```

Would you like to integrate GitHub Actions for automated testing, or do you have a different specific Unity workflow in mind?