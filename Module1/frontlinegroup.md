# Creating a Security Group for Frontline

## Introduction

Windows 365 Frontline provisioning process is slightly different to that of Windows 365 Enterprise. This is because the license is not assigned directly to users, due to the 1:3 users to Cloud PC's ratio, so this assignment is managed by the service as part of provisioning. To demonstrate this, we will first create a security group that has some users in it that we will assign a Windows 365 Frontline Cloud PC to.

## Task

Create a Security Group using the following details:

| Setting | Value |
| -- | -- |
| Group Type | Security |
| Group Name | sg-Frontline | 
| Membership | AdeleV, AlexW, AllanD |

**Q.** Do we need to allocate any Group Based Licenses to this security group?

## Creating a Security Group

1. Navigate to the Groups tab inside Intune or Entra
2. Select "New Group" -> Security
3. Enter a group name and description (if required)
4. Select Membership Type "Assigned"
5. Select "No member assigned"
6. Add in the above members
7. Create the Group

Validate that the group is populated with some provisioned Cloud PCs. (Note - your PC needs to have completed provisioning before membership will update).


