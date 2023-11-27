# Creating a Dynamic Group for Cloud PCs

## Introduction

A Dynamic Group based on a Cloud PC can be useful for assigning policies, or apps to. For example, you may have a Windows Update for Business policy to keep your Cloud PC's up to date. Remember, you can create a dyanmic group of Cloud PCs based on three different membership criteria. 1. The Provisioning Policy Name, 2. All Cloud PCs and 3. All CloudPCs of a particular SKU.

## Task

Create a Dynamic Group based on the Provisioning Policy you created in the previous exercise :-

| Setting | Value |
| -- | -- |
| Group Type | Dynamic |
| Membership | Provisioning Policy Name |


## Creating a Dynamic Group

1. Navigate to the Groups tab inside Intune or Entra
2. Select "New Group" -> Security
3. Enter a group name and description (if required)
4. Select Membership Type "Dynamic Device"
5. Select "Add dynamic query"
6. Select the membership propery "enrollmentProfileName", Operator "equals"
7. Enter the Value - The name of the provisioning profile create
8. Save the Dynamic Query
9. Create the Group

Validate that the group is populated with some provisioned Cloud PCs. (Note - your PC needs to have completed provisioning before membership will update).


## Learning Resources

[Creating a dynamic group containing Cloud PCs](https://learn.microsoft.com/en-gb/windows-365/enterprise/create-dynamic-device-group-all-cloudpcs)
