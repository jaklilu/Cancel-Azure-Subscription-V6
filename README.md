# Cancel Azure Subscription

Scripts that create a policy exemption, grant Owner, cancel a subscription, and verify cancelation.

## Required environment variable

Set **`AZURE_SUBSCRIPTION_ID`** to the Azure subscription ID before running either script. The scripts do not hard-code the subscription ID. If the variable is unset or empty, they exit with an error.

### PowerShell

```powershell
$env:AZURE_SUBSCRIPTION_ID = "<subscription-id>"
.\00-CreateExemption&CancelSub.ps1
```

### Python

```bash
export AZURE_SUBSCRIPTION_ID="<subscription-id>"
python "Cancel-Azure-Subscription-Python/CreateExemption&CancelSub v1.py"
```
