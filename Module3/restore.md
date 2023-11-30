# Restore a Windows 365 Cloud PC

## Introduction

Windows 365 Cloud PCs can be restored to a previous point-in-time snapshot. The system automatically takes 4 long term restore points (1 every 7 days - non configurable), as well as up to 10 admin configured restore points, depending on the snapshot interval specified. For example, a restore point every 4 hours, would create 10 restore points going back a maximum of 40 hours. It is also possible to allow end users to restore their own Cloud PC - useful for power user scenarios.

**Q.** What should you consider before performing a restore on a Cloud PC, and if a restore fails, what next?

## Task

1. Configure the restore points of every 12 hours, and allow the users of the "sg-Engineering" group to perform their own restore.
2. Create a manual snapshot of a Cloud PC

## 1. Configure the restore points for users

Use the Microsoft Intune Admin Center (https://intune.microsoft.com).

1. Devices -> Windows 365 -> User settings
2. Create a new user setting policy (+Add)
3. Give your policy a name
4. Select "Enable users to initiate restore service"
5. Specify the "frequency of restore-point service" to 12 hours.
6. Next
7. Assign the policy to "sg-engineering"
8. Next -> Create

## 2. Create a manual snapshot of a cloud PC.

1. Devices -> Windows 365 -> All Cloud PCs
2. Select a Cloud PC
3. Select "Restore Points" from the left hand menu.
4. Select "Create Restore Points" -> Yes
5. Check back on the PC later to see the restore point has been created.

During a restore the Cloud PC is shut down, restored, and powered back on. Ensure that you do the action out of hours, or when the user is not using their Cloud PC to prevent data loss.

## Learning Resources

[Point in time restore for Windows 365 Enterprise](https://learn.microsoft.com/en-us/windows-365/enterprise/restore-overview)
