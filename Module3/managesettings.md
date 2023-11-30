# Manage Settings for a Windows 365 Cloud PC

## Introduction

Windows 365 Cloud PCs can be managed using Intune Configuration Settings the same as you would a physical PC. In addition, there are specific settings only applicable to Cloud PC's due to the remote connectivity (RDP) of these PC's. These settings may enhance security, or allow for additional granular controls.

For example - you may want to block the users from copying & pasting content from inside their Cloud PC to their local desktop. This can be useful for users you know will consume BYOD scenarios and want to apply additional controls to prevent data leakage.

## Task

1. Create a Settings Catalog policy that changes the RDP settings to block Drive Mapping and Copy & Paste from the local client - assign this to your "sg-Engeering" group.

| Setting | Value |
| -- | -- |
| Configuration Profile | Settings Catalog |
| Admin Template | Device and Resource Redirection | 
| Settings | Do not allow clipboard = Enabled </br> Do not allow drive redirection = Enabled |
| Assignment | sg-Engineering |
  
2. Create a Settings Catalog policy that configures the RDP Idle Session timeout to 15 minutes. Assign this to your "sg-Frontline" group.

| Setting | Value |
| -- | -- |
| Configuration Profile | Settings Catalog |
| Admin Template | Session Time Limits | 
| Settings | Set time limit for active but idle Remote Desktop Services sessions (User) = 15 Minutes |
| Assignment | sg-Frontline |

3. Create a Settings Catalog policy that sets OneDrive to silently sign in with the logged on user.

| Setting | Value |
| -- | -- |
| Configuration Profile | Settings Catalog |
| Admin Template | OneDrive | 
| Settings | Silently sign in users to the OneDrive sync app with their Windows credentials = Enabled |
| Assignment | sg-Frontline </br> sg-Engineering |

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

## 3. OneDrive Silent Config

Use the Microsoft Intune Admin Center (https://intune.microsoft.com).

1. Devices -> Configuration Profiles
2. Create -> New Policy
3. Platform = "Windows 10 or later", Profile Type = "Settings catalog" -> Create
4. Name = "OneDrive Configuration"
5. Add Settings-> Search for "OneDrive"
6. Select "Silently sign in users to the OneDrive sync app with their Windows credentials" = Enabled
7. Enable the setting
8. Next -> Next
9. Assign the policy to your "sg-Frontline" and "sg-Engineering" users.

## Learning Resources

[Set idle session limits for Windows 365 Frontlie](https://learn.microsoft.com/en-us/windows-365/enterprise/frontline-cloud-pc-session-time-limits)

[Manage RDP redirections for Cloud PCs](https://learn.microsoft.com/en-us/windows-365/enterprise/manage-rdp-device-redirections)

[Configuring Optimal M365 Experience for Cloud Native Endpoints](https://learn.microsoft.com/en-us/mem/solutions/cloud-native-endpoints/cloud-native-windows-endpoints#step-8---configure-settings-for-an-optimal-microsoft-365-experience)
