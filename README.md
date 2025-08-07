# Power Platform Capacity Monitor

A Power Automate Flow that sends weekly Teams notifications about your tenant-level storage capacity in Microsoft Power Platform.

## 📊 What the Flow Does

Once set up, the Flow:
1. Runs on a weekly schedule
2. Collects tenant-level capacity information
3. Formats data into a readable Teams message
4. Posts capacity information to your specified Teams channel

## ✅ Prerequisites

- **Microsoft Power Automate** - Any license that allows cloud flows
- **Microsoft Teams** - Where notifications will be delivered
- **Power Platform for Admins V2 connector** - Requires:
  - Power Platform administrator or Global administrator role
  - Power Platform Per User/Per App license or equivalent

## 🚀 Installation

1. **Download**
   - Download the ZIP file from this repository

2. **Select Environment**
   - Navigate to [Power Automate](https://make.powerautomate.com)
   - In the environment selector (top-right), choose the environment where you want to install the Flow

3. **Import**
   - Go to **My flows** → **Import** → **Import package (Legacy)**
   - Select the downloaded ZIP file
   - In the **Review package content** screen:
     - To the right of PPAC Storage Capacity, ensure the Import Setup is set to "Create as new"
     - For **Related resources**, select "Create as new" if connections do not already exist. Otherwise, you can choose "Select during import"
     - If "Create as new" is selected, the connectors that should be setup are: Microsoft Teams and Power Platform for Admins V2
       - For the Power Platform for Admins V2 connector, choose your preferred authentication type: OAuth or service principal
   - Click **Import** to begin the import process
   - Wait for the "Import is complete" success message

4. **Configure Connections**
   - Open the imported Flow in edit mode
   - **Microsoft Teams Connection:**
     - Locate the "Post a message in a chat or channel" action
     - Select the Team and Channel where notifications should be sent
     - Ensure your account has posting permissions to this channel
   - **Power Platform for Admins V2 Connection:**
     - Find the "Get tenant settings" and capacity-related actions
     - Connect using an account with Power Platform admin privileges
     - Test this connection to verify proper access to tenant information
   - Save the Flow

5. **Turn on the Flow**
   - After saving, return to the Flow details page
   - Look for the toggle switch at the top of the page
   - Click the "Turn on" button
   - The Flow is now active and will run according to the scheduled recurrence
