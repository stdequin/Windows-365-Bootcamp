# Assigning Licenses to Users

## Introduction

There are two ways to assign licenses to users, either through group based licensing or with a direct assignment. Wnidows 365 Enterprise provisions a cloud PC to users that meet two criteria.

1. The user has a Windows 365 Enterprise License assigned to them.
2. The user is a member of a group that is targeted by a Provisioning Policy.

## Direct License Assignment

Use the Microsoft Admin Center (https://admin.microsoft.com) to assign a license 

## Group Based License Assignment

## Windows 365 Enterprise

1. Navigate to the Intune Management console (https://intune.microsoft.com)
2. Go to Devices -> Provisioning\Windows 365 -> All Cloud PCs
3. Verify that you see your licensed user, with "Not Provisioned" in their status.

The "Not Provisioned" status is because only condition 1 (user is assigned a license) above is true.


## Learning Resources

[Assigning Licenses in Windows 365](https://learn.microsoft.com/en-us/windows-365/enterprise/assign-licenses)
[Licensing Groups in Microsoft Entra ID](https://learn.microsoft.com/en-us/entra/identity/users/licensing-groups-assign)
