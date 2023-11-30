# Making Users local admins on their Cloud PC

## Introduction

Windows 365 can automatically make users local administrators of their Cloud PC. Adding the user to the local admins group happens at provisioning, and can be useful for Power User scenarios, especially when combined with self service functions like restore, and reset.

**Note.** Creating the policy to make a user a local Admin **only** makes then an admin of their own Cloud PC. It does not make them a local admin of other Cloud PCs.

## Task

1. Configure your "sg-Engineering" users to be local administrators of their own Cloud PCs

## 1. Configure the restore points for users

Use the Microsoft Intune Admin Center (https://intune.microsoft.com).

1. Devices -> Windows 365 -> User settings
2. Create a new user setting policy (+Add)
3. Give your policy a name
4. Select "Enable Local Admin"
7. Assign the policy to "sg-engineering"
8. Next -> Create


## Learning Resources

[Assign users as local admins](https://learn.microsoft.com/en-us/windows-365/enterprise/assign-users-as-local-admin)
