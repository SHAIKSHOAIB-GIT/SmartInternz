# ServiceNow Workflow Documentation

## Step 1: Create Users
1. Navigate to **All → User Administration → Users**.
2. Click **New** and fill in details (Name, User ID, Email).
3. Save.

## Step 2: Create Groups
1. Navigate to **All → User Administration → Groups**.
2. Click **New**, name the group, assign roles if needed.
3. Save.

## Step 3: Assign Roles
1. Open the group record.
2. Add roles (e.g., `itil`, `custom_role_certificate`).
3. Save.

## Step 4: Create ACL Rules
1. Navigate to **All → System Security → Access Control (ACL)**.
2. Click **New**, choose table and field restrictions.
3. Assign roles.

## Step 5: Configure Flow Designer
1. Navigate to **All → Flow Designer**.
2. Create a new flow:
   - **Trigger:** When incident is created.
   - **Condition:** If issue equals “Unable to login to platform”.
   - **Action:** Assign to **Platform Support** group.
3. Save and activate.

## Step 6: Testing
1. Create a new incident matching the condition.
2. Verify the ticket is auto-assigned to the correct group.
