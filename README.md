# Microsoft CMMC Acceleration Program
This resource is part of the Microsoft Cybersecurity Maturity Model Certification (CMMC) Acceleration Program. Go [here](https://aka.ms/CMMCResponse) to learn more about the program.

# Azure Blueprint for CMMC Level 3 (Preview)
This repository contains a sample Azure Blueprint for CMMC Level 3.  When this Blueprint is assigned to a subscription or management group, the associated CMMC Level 3 artifacts will also be assigned.

>DISCLAIMER: _The Azure Blueprint for CMMC Level 3 is based upon available information to date and is provided as a sample resource only. Microsoft is not a CMMC accrediting body and thus cannot guarantee any outcome under the formal CMMC review process._

## Prerequisites
1. You must first deploy the related [Policy Initative](https://github.com/adamdimopoulos/PolicyInitiatives) into your target subscription before applying this sample Blueprint. Do not proceed until this step is completed.

2. You should have a basic understanding of [Azure Blueprints](https://azure.microsoft.com/en-us/services/blueprints/) before applying this sample. Do not apply this Blueprint in any production subscription without first understanding and accepting the potential impact.

3. Install the [Az.Blueprint](https://powershellgallery.com/packages/Az.Blueprint/) PowerShell cmdlet, if not already installed.
  ```powershell 
  Install-Module -Name Az.Blueprint
  ```

## Deployment
1. Download this repo and extract to a local folder.

2. Execute the following PowerShell command to import the Blueprint into your subscription. Substitute your own SubscriptionId and InputPath.
  ```powershell
  Import-AzBlueprintWithArtifact -Name CMMC-L3 -SubscriptionId 00000000-0000-0000-0000-000000000000 -InputPath  C:\Blueprints\SampleBlueprint
  ```
3. Browse to the Azure Portal and open the **Blueprints** blade. You should see the sample Blueprint if the above command was successful.

4. From the Blueprints blade select **CMMC-L3** > **Publish Blueprint** > **Provide a version** and click **Publish**.  

5. Click **Assign Blueprint** and enter the required values.

**After a few minutes the Blueprint Assignment should be visible in the Policy > Compliance blade.**

## Next Steps
Please review all aspects of the Blueprint and provide [feedback](https://aka.ms/feedbackazureblueprintcmmc).
