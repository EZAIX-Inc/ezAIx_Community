# Microsoft Teams Shared Calling Management Tool

This PowerShell script provides a graphical user interface (GUI) to manage Microsoft Teams Shared Calling policies, assign them to users, and export relevant data to CSV files. It simplifies the management of shared calling policies, resource accounts, and user assignments within your Microsoft Teams environment.

---

## Features
- **View Shared Calling Policies**: Load and display all shared calling policies along with their associated resource accounts, phone numbers, and emergency numbers.
- **Create Shared Calling Policies**: Create new shared calling policies by specifying policy details and associated resource accounts.
- **Assign Policies to Users**: Assign shared calling policies to individual users or multiple users via a CSV file.
- **View Users with Policies**: Display all users who have a shared calling policy assigned, along with their shared calling and voice routing policies.
- **Export Data to CSV**: Export the displayed policies and users data to CSV files for reporting or further analysis.

---

## Prerequisites
- **PowerShell Version**: PowerShell 5.1 or later.
- **Microsoft Teams PowerShell Module**: Latest version installed.

```powershell
Install-Module -Name MicrosoftTeams -Force
