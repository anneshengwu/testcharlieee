# Advanced GitHub Projects with Automations

## Step 2: Set Up Item-Based Automations
Now that you've created your project with custom fields, let's configure automations that trigger when items change.

### 📋 Task: Configure Item-Based Automations
1. Navigate to your "Automated Workflow" project
2. Click the project settings menu (⚙️) in the top-right
3. Select "Workflows" from the left sidebar
4. Create the following automations:
   - When an issue is closed, set Status to "Completed"
   - When a pull request is opened, set Status to "Under Review"
   - When an issue or PR has "high" in its title, set Priority to "High"
   - When an item's Status changes to "In Progress", add the current user as the Assignee

To create a workflow:
- Click "New workflow"
- Choose "Item added to project" or "Item field changed" as the trigger
- Set up the conditions and actions as described above
- Save the workflow

Once completed, go to the **Actions** tab and run the "Complete Step 2" workflow to proceed to the next step.

### 📚 What are Item-Based Automations?
Item-based automations trigger when items (issues or PRs) are added to your project or when their field values change. These automations help ensure your project stays up-to-date automatically as work progresses, reducing manual updates and ensuring consistency.

### ⏳ Waiting for you to set up item-based automations...

<!-- STEP: 2 -->