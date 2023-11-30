# Reprovisioning a Windows 365 Cloud PC

## Introduction

Windows 365 Cloud PCs can be reprovisioned, using the latest settings in the provisioning policy. This is equivilent of rebuilding or reissuing a physical device to an end user. It is useful in scenarios where the Cloud PC is unresponsive, and the restore action has not been able to return the Cloud PC to a good working state.

## Task

Resize the Cloud PC to

**Q.** If you manually assign a new license to the user you want to resize, what is the admin and end user experience?

**Note** If your licenses were assigned using a Group Based License assignment, then the Resize process is different. Please see [Resize a Cloud PC with a group based license](https://learn.microsoft.com/en-us/windows-365/enterprise/resize-cloud-pc#resize-a-single-cloud-pc-provisioned-with-a-group-based-license)

## Resizing a Cloud PC

Use the Microsoft Intune Admin Center (https://intune.microsoft.com).

1. Devices -> Windows 365 -> All Cloud PCs
2. Select the device ou want to resize
3. Select "Resize" from the top actions menu.
4. Select the specification you want to resize to (2vCPU, 8GB, 256GB)
5. Select Resize
6. Under the "All Cloud PCs" view, refresh the page to see the device is resizing.

During a resize the Cloud PC is shut down, resized, and powered back on. Ensure that you do the action out of hours, or when the user is not using their Cloud PC to prevent data loss.

**Q.** Can you resize back down to the 2vCPU,4GB,128GB specification?

## Learning Resources

[Resize a Cloud PC](https://learn.microsoft.com/en-us/windows-365/enterprise/resize-cloud-pc)
