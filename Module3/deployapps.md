# Deploying Apps to a Windows 365 Cloud PC

## Introduction

Windows 365 Cloud PCs are managed in Intune the same as physical PCs would be. This allows you to leverage new or existing policies for application deployment to those Cloud PC's, which Intune will manage the deploment of.

## Task

Deploy a modern store app (Adobe Acrobat Reader) using Intune to your Cloud PC's. (Use the device group created in the previous exercise).

## Deploying the Store App

Use the Microsoft Intune Admin Center (https://intune.microsoft.com).

1. Apps -> Windows -> Add
2. Select App Type "Microsoft Store App (new)"
3. Search the Microsot Store App (new) catalog and find "Adobe Acrobat Reader" -> Next
4. Assign the app as Required to the Dynamic Cloud PC group you created earlier.
5. Select next on the Scope Tags page
6. On the Assignments page, select "Add Groups" and select the dynamic group you created in Module 1.
7. Next -> Create

You can come back to the app later and check the Device Install status for your Cloud PCs

## Learning Resources

[Deploying Windows Apps using Microsoft Intune](https://learn.microsoft.com/en-us/mem/intune/apps/apps-windows-10-app-deploy)
