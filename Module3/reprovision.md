# Reprovisioning a Windows 365 Cloud PC

## Introduction

Windows 365 Cloud PCs can be reprovisioned, using the latest settings in the provisioning policy. This is equivilent of rebuilding or reissuing a physical device to an end user. It is useful in scenarios where the Cloud PC is unresponsive, and the restore action has not been able to return the Cloud PC to a good working state. If using a custom image, it can also be used to refresh the Cloud PC with the latest custom image. (Although configuring updates through Intune is preferred).

**Note.** Reprovisioning is a **destructive** process. The current Cloud PC is destroyed (including restore points) and a new PC is created. The PC will have a new computer object.

**Q.** If you have configurations/apps etc applied to groups with direct assignment of computers, what will you need to do after reprovisioning a Cloud PC?

## Task

Reprovision a Cloud PC

## Reprovision a Cloud PC

Use the Microsoft Intune Admin Center (https://intune.microsoft.com).

1. Devices -> Windows 365 -> All Cloud PCs
2. Select the device you want to reprovision
3. Select "Reprovision" from the top actions menu.
4. Acknowledge the warning and select "Yes"
6. Under the "All Cloud PCs" view, refresh the page to see the device is reprovisioning.

## Learning Resources

[Reprovision a Cloud PC](https://learn.microsoft.com/en-us/windows-365/enterprise/reprovision-cloud-pc)
