## Objective
We will be creating compliance policies to ensure that the devices meet the organization's requirements.

## Configuration

1. head to endpoint.microsoft.com
2. Go to Devices > Windows > Compliance
3. Create Compliance and populate with the following:
  Platform: Windows 10 or later
4. Create a name and write a description
5. for the compliance settings well require the following:
  -Firewall
  -Antivirus
  -Antispyware
  -Microsoft Defender Antimalware
  -Microsoft Defender Antimalware security intelligence up-to-date
  -Real-time protection
6. On the Actions for noncompliance tab, we'll select Add device to retire list from the Mark device for non-compliant drop-down menu.
7. Select next
8. add all devices
9. The compliance policy is now created
10. well verify that the compliance works


## Testing Compliance

1. spinning up a VM, we are going to join it to the entra environment
2. after joining the VM to the entra environment and the sync is done, we'll sign out of the local admin account and sign in with the Entra admin account
3. Now head over to endpoint.microsoft.com
4. go to Devices > All devices > select the device that was added to the entra environment
5. on the left hand side select Compliance.
6. we can verify that the device shows up as compliant!
![compliance](https://github.com/derinp/EnamoradoTech/blob/main/images/compliance.png)
