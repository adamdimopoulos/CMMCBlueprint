# Blueprints
This repository contains the sample Blueprint for CMMC Level 3.  When this Blueprint is assigned to a subscription or management group, the associated CMMC Level 3 artifacts will also be assigned. Please use this sample to test and provide [feedback](https://aka.ms/feedbackazureblueprintcmmc) on the Blueprint prior to the upcoming preview releases.

# Prerequisites
This doc assumes you have a basic understanding of how blueprints work. Additionally, as the policy artifact assigned by this blueprint is also a sample, you must first go to the [PolicyInitiatives](https://github.com/adamdimopoulos/PolicyInitiatives) repo and follow the instructions to deploy the initiative into your desired subscription.  Once that is complete, you can return to this repository to import the Blueprint by following the instructions below:

**Download this repo and save to a desired local folder.**

If you don't alread have it, download the [Az.Blueprint module](https://powershellgallery.com/packages/Az.Blueprint/) from the powershell gallery:
```powershell 
Install-Module -Name Az.Blueprint
```
Simply execute the following powershell command, substituting your own subscriptionid and inputpath: 
```powershell
Import-AzBlueprintWithArtifact -Name CMMC-L3 -SubscriptionId 00000000-0000-0000-0000-000000000000 -InputPath  C:\Blueprints\SampleBlueprint
```
