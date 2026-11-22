# Cancel Azure Subscription

Scripts that create a policy exemption, grant Owner, cancel a subscription, and verify cancelation.

## Required environment variables

Set these before running either script. The scripts do not hard-code Azure IDs. If a variable is unset or empty, they exit with an error.

| Variable | Purpose |
| --- | --- |
| `AZURE_SUBSCRIPTION_ID` | Azure subscription ID |
| `AZURE_USER_OBJECT_ID` | User object ID granted Owner |
| `AZURE_MANAGEMENT_GROUP_ID` | Management group ID in the policy assignment path |

### PowerShell

```powershell
$env:AZURE_SUBSCRIPTION_ID = "<subscription-id>"
$env:AZURE_USER_OBJECT_ID = "<user-object-id>"
$env:AZURE_MANAGEMENT_GROUP_ID = "<management-group-id>"
.\00-CreateExemption&CancelSub.ps1
```

### Python

```bash
export AZURE_SUBSCRIPTION_ID="<subscription-id>"
export AZURE_USER_OBJECT_ID="<user-object-id>"
export AZURE_MANAGEMENT_GROUP_ID="<management-group-id>"
python "Cancel-Azure-Subscription-Python/CreateExemption&CancelSub v1.py"
```
