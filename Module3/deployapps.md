# Deploying Apps to a Windows 365 Cloud PC

## Introduction

Windows 365 Cloud PCs are managed in Intune the same as physical PCs would be. This allows you to leverage new or existing policies for application deployment to those Cloud PC's, which Intune will manage the deploment of.

## Task

Deploy a modern store app (Adobe Acrobat Reader) using Intune to your Cloud PC's. (Use the device group created in the previous exercise).

## Deploying the Store App

Use the Microsoft Intune Admin Center (https://intune.microsoft.com).
1. Open Endpoint Security
2. Select Security Baselines -> Windows 365 Security Baseline
3. Select "Create Profile" and enter a name of your choice.
4. Select next on the configuration settings page. (Note - if you wanted to adjust the policy recommendations, you could do so here).
5. Select next on the Scope Tags page
6. On the Assignments page, select "Add Groups" and select the dynamic group you created in Module 1.
7. Select Create

You can come back to the properties of the security baseline later, and see under the Monitor tab, the state of the policies applying to the Cloud PCs

## Learning Resources

[Deploying Security Baslines](https://learn.microsoft.com/en-us/windows-365/enterprise/deploy-security-baselines)
