# Securing Windows 365 Cloud PCs with a Security Baseline

## Introduction

Windows 365 Security Baselines are a set of policy templates built on best practices and real world implementations, allowing you to quickly implement and help lower security risks. You can assign these policies using the built in Security Baseline feature of Intune, directly to a dynamic group containing your Cloud PCs.

Optionally - you can also adjust the security baseline to remove or add additional settings depending on your customers requirements. This can often be required to comply with local regulatory requirements, for example.

## Task

Assign the Windows 365 Security Baseline to the previous created dynamic group that contains your Cloud PCs.

## Assigning the Security Baseline

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

