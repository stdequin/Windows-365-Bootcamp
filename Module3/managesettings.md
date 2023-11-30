# Manage Settings for a Windows 365 Cloud PC

## Introduction

Windows 365 Cloud PCs can be managed using Intune Configuration Settings the same as you would a physical PC. In addition, there are specific settings only applicable to Cloud PC's due to the remote connectivity (RDP) of these PC's. These settings may enhance security, or allow for additional granular controls.

For example - you may want to block the users from copying & pasting content from inside their Cloud PC to their local desktop. This can be useful for users you know will consume BYOD scenarios and want to apply additional controls to prevent data leakage.

## Task

1. Create a Settings Catalog policy that changes the RDP settings to block Drive Mapping and Copy & Paste from the local client - assign this to your "sg-Engeering" group.
2. Create a Settings Catalog policy that configures the RDP Idle Session timeout to 15 minutes. Assign this to your "sg-Frontline" group.

## 1. RDP Settings 

Use the Microsoft Intune Admin Center (https://intune.microsoft.com).

1. Devices -> Configuration Profiles
2. Create -> New Policy
3. Platform = "Windows 10 or later", Profile Type = "Settings catalog" -> Create
4. Name = "RDP Settings"
5. Add Settings-> Search for "Device and Resource Redirection"
6. Select "Do not allow clipboard redirection" and "Do not allow drive redirection"
7. Enable both of these settings
8. Next -> Next
9. Assign the policy to your "sg-Engineering" users.
 
## 2. Idle Time Out Settings

Use the Microsoft Intune Admin Center (https://intune.microsoft.com).

1. Devices -> Configuration Profiles
2. Create -> New Policy
3. Platform = "Windows 10 or later", Profile Type = "Settings catalog" -> Create
4. Name = "Frontline Idle Timeout "
5. Add Settings-> Search for "Session time limits"
6. Select "Set time limit for active but idle Remote Desktop Services sessions (User)"
7. Enable the settings and select "15 minutes"
8. Next -> Next
9. Assign the policy to your "sg-Frontline" users.


## Learning Resources

[Point in time restore for Windows 365 Enterprise](https://learn.microsoft.com/en-us/windows-365/enterprise/restore-overview)
