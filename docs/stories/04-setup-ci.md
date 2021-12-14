# Setup Continuous Integration

**As a:** Developer  
**I need:** the ability to continuously test my code  
**So that:** I can know if a Pull Request has broken the build  

**Assumptions:**

- We will use GitHub Actions
- Need to tell GitHub Actions that we need a Redis database

**Acceptance Criteria:**

```gherkin
Given I have set up GitHub Actions
When I make a Pull Request
Then my automated tests should run automatically
And if they fail the build will be stopped
```
