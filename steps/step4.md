# Advanced GitHub Projects with Automations

Welcome to this interactive tutorial on automating GitHub Projects for efficient workflows! This repository will guide you through creating a project board and implementing powerful automations using GitHub Projects V2.

## Step 4: Advanced Automation with GitHub Actions Integration
For our final step, let's connect GitHub Actions to our Project Board for even more powerful automations.

### 📋 Task: Set Up GitHub Actions Integration
1. Create a new file in your repository at `.github/workflows/project-automation.yml`
2. Add the following GitHub Actions workflow:
   ```yaml
   name: Project Automation
   
   on:
     issues:
       types: [opened, labeled, unlabeled]
     pull_request:
       types: [opened, ready_for_review]
   
   jobs:
     project_automation:
       runs-on: ubuntu-latest
       steps:
         - uses: actions/add-to-project@v0.4.0
           with:
             project-url: https://github.com/users/YOUR_USERNAME/projects/YOUR_PROJECT_NUMBER
             github-token: ${{ secrets.GITHUB_TOKEN }}
         - name: Add labels based on paths
           if: github.event_name == 'pull_request'
           uses: actions/github-script@v6
           with:
             script: |
               const payload = context.payload;
               const pr = payload.pull_request;
               
               // Example: Add a "frontend" label if PR changes files in the frontend directory
               if (pr.changed_files && pr.changed_files.some(file => file.filename.startsWith('frontend/'))) {
                 github.rest.issues.addLabels({
                   issue_number: pr.number,
                   owner: context.repo.owner,
                   repo: context.repo.repo,
                   labels: ['frontend']
                 });
               }