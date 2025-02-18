# Prerequisites for Onboarding Microsoft Sentinel
**1)  Azure Subscription:** You need an active Azure subscription to deploy and use Microsoft Sentinel. You can use Pay-as-you-go or Azure Enterprise Agreement (EA) subscriptions.

**2) Azure Active Directory (AAD) Tenant:** A Azure Active Directory (AAD) tenant is required for user authentication and authorization. Ensure you have appropriate permissions (typically, Global Administrator or Security Reader role).

**3) Log Analytics Workspace:** Microsoft Sentinel is built on Log Analytics, so you must create a Log Analytics Workspace in the Azure region where you want to deploy Sentinel. The Log Analytics Workspace will store your security data, alerts, and logs.

**4) Permissions for Microsoft Sentinel Deployment:** You must have sufficient permissions to onboard Microsoft Sentinel, such as: Contributor or Owner role for the Log Analytics workspace. Security Administrator or Global Administrator for accessing security services in Azure.

**5) Supported Data Sources:** Prepare a list of data sources (e.g., Azure services, on-premise systems, firewalls, endpoints) that you plan to connect to Sentinel. Supported sources include Azure Security Center, Office 365, DNS logs, firewalls, and third-party integrations.

**6) Azure Monitor Integration (Optional):** If you want to collect and analyze performance and diagnostic data, you may need to configure Azure Monitor alongside Sentinel.
This helps in integrating monitoring data like logs and metrics from resources in your environment.

**7) Automation and Playbooks (Optional):** For incident response automation, you need access to Azure Logic Apps to create playbooks. Logic Apps allow you to automate response actions such as notifying teams or blocking IP addresses when a security threat is detected.

**8) Microsoft Defender (Optional but Recommended):** For advanced threat detection and defense capabilities, you can integrate Microsoft Defender with Sentinel. Microsoft Defender helps detect potential threats across your resources and provides deeper insights for security monitoring.

**9) Network Connectivity:** Ensure that network connectivity to Azure resources and data sources is properly configured. If needed, set up VPN or ExpressRoute for secure connectivity, especially for on-premises data sources.

## Microsoft Sentinel Onboarding Process in the infrastructure

### Enable Microsoft Sentinel

1. Sign in to **Azure Portal**.
2. Go to **Microsoft Sentinel** and click **+ Add**.
3. Select your **Log Analytics workspace**.
4. Click **Enable Microsoft Sentinel**.

OR

## Custom Deployment: ARM Template for Sentinel Deployment

### Create sentinel-deployment.json with
``` json
{
  "$schema": "https://schema.management.azure.com/schemas/2019-04-01/deploymentTemplate.json#",
  "contentVersion": "1.0.0.0",
  "resources": [
    {
      "type": "Microsoft.OperationalInsights/workspaces/providers",
      "apiVersion": "2021-10-01",
      "name": "[concat(parameters('sentinel-ws'), '/Microsoft.SecurityInsights')]",
      "properties": {}
    }
  ]
}
```
