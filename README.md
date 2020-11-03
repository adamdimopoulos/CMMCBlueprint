# Blueprints
This repository contains the sample Blueprint for CMMC Level 3.  When this Blueprint is assigned to a subscription or management group, the associated CMMC Level 3 artifacts will also be assigned. 

# Prerequisites
This doc assumes you have a basic understanding of how blueprints work. Additionally, as the policy artifact assigned by this blueprint is also a sample, you must first go to the [PolicyInitiatives](https://github.com/adamdimopoulos/PolicyInitiatives) repo and follow the instructions to deploy the initiative into your desired subscription.  Once that is complete, you can return to this repository to import the Blueprint.

 **If you do not already have it, download the [Az.Blueprint module](https://powershellgallery.com/packages/Az.Blueprint/) from the powershell gallery:**
  ```powershell 
  Install-Module -Name Az.Blueprint
  ```

# Deployment
1. Download this repo and extract to a desired local folder.

3. Execute the following powershell command, substituting your own subscriptionid and inputpath to import the Blueprint into your subscription: 
  ```powershell
  Import-AzBlueprintWithArtifact -Name CMMC-L3 -SubscriptionId 00000000-0000-0000-0000-000000000000 -InputPath  C:\Blueprints\SampleBlueprint
  ```
**You should now see the Blueprint in the portal.**

4. From the Blueprints blade select 'CMMC-L3' > 'Publish Blueprint' > Provide a version and click 'Publish'.  

5. Click 'Assign Blueprint' and enter the required values.

**After a few minutes the Blueprint Assignment should be visible in the Policy > Compliance blade.**

# Next Steps
Please use this sample to test and provide [feedback](https://aka.ms/feedbackazureblueprintcmmc) on the Blueprint prior to the upcoming preview releases.

