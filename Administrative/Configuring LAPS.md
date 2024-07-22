## Objective
We wil configure LAPs as a way to manage local admin passwords. This will secure the local administrator account on a remotely managed device.

## Configuration
1. We head over to endpoint.microsoft.com > Endpoint Security > Account Protection
2. Select Create Policy and fill with the following information:
   Platform: Windows 10 and later
   Profile: Local admin password solution (Windows LAPS)
3. click create
4. fill in the name and description
5. in the Configuration Settings tab fill in the following:
   Backup Directory: Backup the password to Azure AD only
   Password Age Days: 30
   Administrator Account Name: aciadmin
   Password complexity: Large Letters + small letters + numbers
6. Click next on scope tag
7. In assignments we will select "Add all users" and "Add all devices" in the Include groups field.
8. Lastly, in the last tab, select create


## Verify LAPS Policy

1. we will be testing with a Vm to see that LAPS works
2. Headover to endpoint.microsoft.com > devices > select a device
3. scroll down to Local Admin password within the Overview pane on the left hand side
4. You should see the passwor for the device
