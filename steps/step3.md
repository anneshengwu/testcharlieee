# Advanced GitHub Projects with Automations

Welcome to this interactive tutorial on automating GitHub Projects for efficient workflows! This repository will guide you through creating a project board and implementing powerful automations using GitHub Projects V2.

## Step 3: Implement Date-Based Automations
Let's set up automations that run based on dates and time conditions.

### 📋 Task: Set Up Date-Based Automations
1. Navigate to your "Automated Workflow" project
2. Go to project settings (⚙️) > Workflows
3. Create the following date-based automations:
   - When an item's Due Date is today, set Priority to "Critical"
   - When an item's Due Date is within 3 days, set Priority to "High" (if not already Critical)
   - When Status has been "In Progress" for more than 7 days, add a comment requesting an update
   - Create a scheduled workflow that runs weekly to archive items with Status "Completed" for more than 14 days

To create date-based workflows:
- For field conditions, use the "Item field" trigger with date comparisons
- For scheduled workflows, use the "Scheduled" trigger type

Once completed, go to the **Actions** tab and run the "Complete Step 3" workflow to proceed to the next step.

### 📚 The Power of Date-Based Automations
Date-based automations help teams stay on schedule and maintain awareness of approaching deadlines. They can automatically escalate priority as deadlines approach, clean up completed work, and help prevent items from stagnating in any status for too long.

### ⏳ Waiting for you to set up date-based automations...

<!-- STEP: 3 -->