
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
```

- **Permissions**: Account with Teams Communications Administrator role or higher in Microsoft 365.

---

## Installation

### Clone or Download the Repository

Clone the repository:

```bash
git clone https://github.com/yourusername/TeamsSharedCallingManagementTool.git
```

Or download the script file directly from the repository.

### Save the Script

Ensure the script file is saved with a `.ps1` extension, e.g., `TeamsSharedCallingManagementTool.ps1`.

---

## Usage

### Connecting to Microsoft Teams PowerShell

Before running the script, you must connect to Microsoft Teams PowerShell:

```powershell
Connect-MicrosoftTeams
```

Authenticate using an account with the necessary permissions.

### Running the Script

1. Open PowerShell with administrative privileges.
2. Navigate to the directory where the script is located:

   ```powershell
   cd C:\Path\To\Your\Script
   ```

3. Execute the script:

   ```powershell
   .\TeamsSharedCallingManagementTool.ps1
   ```

---

## Using the Tool

### Tab 1: View Policies

1. **Load Shared Calling Policies**:
   - Click "Load Shared Calling Policies" to fetch and display all shared calling policies.
   - The policies are displayed with their associated resource account names, phone numbers, and emergency numbers.

2. **Export to CSV**:
   - After loading the policies, click "Export to CSV" to save the data to a CSV file.

### Tab 2: Create Policy

1. **Enter Policy Details**:
   - **Shared Calling Policy Name**: Enter a unique name for the policy.
   - **Resource Account UPN**: Specify the UPN (email address) of the associated resource account (e.g., an auto attendant).
   - **Emergency Dial Strings**: Enter emergency dial strings, separated by commas (e.g., `911,112`).
   - **Emergency Callback Numbers**: (Optional) Enter emergency callback numbers, separated by commas.
   - **Allow Enhanced Emergency Services**: Check this box if you want to enable enhanced emergency services.

2. **Create Policy**:
   - Click "Create Shared Calling Policy" to create the policy.

### Tab 3: Assign Policy

1. **Load Policies**:
   - Click "Load Policies" to populate the dropdown with available shared calling policies.

2. **Assign to Single User**:
   - Select a policy from the dropdown.
   - Enter the User Principal Name (email) of the user.
   - Click "Assign Policy to User".

3. **Assign to Multiple Users via CSV**:
   - Prepare a CSV file with a column named `UPN` containing user emails.
   - Click "Browse" to select the CSV file.
   - Click "Assign Policy to CSV Users".

### Tab 4: View Users

1. **Load Users with Shared Calling Policy**:
   - Click "Load Users with Shared Calling Policy" to display all users who have a shared calling policy assigned.

2. **Export to CSV**:
   - After loading the users, click "Export to CSV" to save the data to a CSV file.

---

## Troubleshooting

- **No Data Displayed**: Ensure you have the necessary permissions and that data exists in your Microsoft Teams environment.
- **Errors When Loading Data**: Verify that you are connected to Microsoft Teams PowerShell and that your session has not expired.
- **Script Execution Policy**: If you encounter execution policy errors, you may need to adjust your PowerShell execution policy:

   ```powershell
   Set-ExecutionPolicy -ExecutionPolicy RemoteSigned -Scope CurrentUser
   ```

---

## Disclaimer

This script is provided "as is" without warranty of any kind, express or implied. Use at your own risk. The authors and contributors are not responsible for any damage or data loss resulting from the use of this script.

Before using this script in a production environment, thoroughly test it in a controlled setting to ensure it meets your requirements and functions as expected.

---

## Contributing

Contributions are welcome! Please submit a pull request or open an issue to discuss any changes or improvements.

---

## License

This project is licensed under the MIT License.

---

## Contact

Feel free to contact the project authors via the GitHub repository for any questions or suggestions.
