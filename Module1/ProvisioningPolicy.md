# Creating a Provisioning Policy

## Introduction

A Provisioning Policy is a configuration in Windows 365 that defines what Cloud PC's to create for which users. The Provisioning policy defines the License Type,Join Type, Region, Language, Image, and Users.

## Task

Create a provisioning policy with the following settings :-

| Setting | Value |
| -- | -- |
| License Type | Enterprise |
| Join Type | Microsoft Entra Join |
| Network | Microsoft hosted network |
| Geography | European Union |
| Region | Automatic |
| Use Entra single sign-on | Yes |
| Image | Gallery (Windows 11 Enterprise + M365 Apps |
| License Type | Enterprise |
| Language & Region | German |
| Assignment | sg-Engineering |

**Q.** What is the preferred method Join and Networking method, and why?

**Q.** When creating a provisioning policy, what is the advantage to select the "Geography" only, and not specify a "Region"?

**Q.** What happens to the gallery image each month, and what does this mean to existing, and newly provisioned Cloud PCs?

## Creating a Windows 365 Enterprise Provisioning Policy

1. Navigate to the Intune Management console (https://intune.microsoft.com)
2. Go to Devices -> Provisioning\Windows 365 -> Provisioning Policies
3. Select "Create Policy"
4. Enter a name for your policy, and a description if required.
5. Select the License Type "Enterprise"
6. Select the Join Type "Microsoft Entra Join"
7. Selet the Network as "Microsoft Hosted"
8. Select geography as "European Union"
9. Select the Region as "Automatic" - this is recommended to allow the SaaS service to use the most appropriate region based on capacity and service availability.
10. User Microsoft Entra Single sign-on. - This removes the second prompt from the user when connecting. (1st Prompt Entra Directory, 2nd Prompt the Cloud PC)
11. Next
12. Select Image as Gallery - "Windows 11 Enterprise + M365 Apps" - This is the default and recommended to then layer on config and apps in Intune, this image is updated monthly for newly provisioned PC's. Existing PCs will be updated using WufB.
13. Next
14. Select the Language & Region as "German" - This applies language and region settings during provisioning for the Operating System **and** Microsoft 365 Apps.
15. Next
16. Assign the Policy to the "sg-Engineering" group.
17. Under the "All Cloud PC's" tab, monitor to check that provisioning has started for licensed members of this group.


## Learning Resources

[Provisioning in Windows 365](https://learn.microsoft.com/en-gb/windows-365/enterprise/provisioning)

