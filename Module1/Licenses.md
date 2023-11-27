# Assigning Licenses to Users

## Introduction

There are two ways to assign licenses to users, either through group based licensing or with a direct assignment. Wnidows 365 Enterprise provisions a cloud PC to users that meet two criteria.

1. The user has a Windows 365 Enterprise License assigned to them.
2. The user is a member of a group that is targeted by a Provisioning Policy.

## Task

Assign a Windows 365 Enterprise license to a user, using whichever method you prefer.

**Q.** Which method do your customers normally use for license assignment? What do you need to consider when using Groub Based Assignment of licenses?

## Direct License Assignment

Use the Microsoft Admin Center (https://admin.microsoft.com) to assign a license.
1. Navigate to the Admin Center
2. Users -> Active Users
3. Select the user "Megan Bowen"
4. Under "Licenses and apps" select the "Windows 365 Enterprise 2vCPU, 4GB, 128GB" License
5. Save Changes

## Group Based License Assignment

Use the Entra Admin Center (https://entra.microsoft.com) to assign a license to a group
1. Navigate to the Entra Admin Center
2. Groups
3. Select the Group "sg-Engineering"
4. Select Licenses -> Assignments
5. Select the Microsoft 365 E5 **and** the "Windows 365 Enterprise 2 vCPU, 4GB, 128GB"
6. Save changes

Navigate to a member of the group, and check the licenses that are assigned to this user. You will see the E5 and Windows 365 licenses. Note, Intune is a pre-requisite license for Windows 365 Enterprise and without it provisioning will fail.   

## Windows 365 Enterprise

1. Navigate to the Intune Management console (https://intune.microsoft.com)
2. Go to Devices -> Provisioning\Windows 365 -> All Cloud PCs
3. Verify that you see your licensed users, with "Not Provisioned" in the status.

The "Not Provisioned" status is because only condition 1 (user is assigned a license) above is true.


## Learning Resources

[Assigning Licenses in Windows 365](https://learn.microsoft.com/en-us/windows-365/enterprise/assign-licenses)
[Licensing Groups in Microsoft Entra ID](https://learn.microsoft.com/en-us/entra/identity/users/licensing-groups-assign)
