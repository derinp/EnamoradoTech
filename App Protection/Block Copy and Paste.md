## Objective
We will be implementing some DLP solutions in order to secure our proprietary data. We will focus on locking down all core microsoft apps on mobile devices.
The reasons we are looking to lock down copying pasting as as follows:
1. Data security: This will help protect sensitive information from being transferred to unauthorized or less secure applications.
2. Compliance: We will ensure that data handling complies with industry regulations and organizational policies.
3. Protect intellectual Propert: We want to prevent our information getting into the wrong hands.
4. Minimizing data leakage: Blocking copying and pasting between apps will reduce the amount of accidental data leaving our organization.

This highlights the importance of such a policy that will allow us to have a secure and compliant IT environment.

## Implementation
The very first thing we need to do is create a group in which all mobile devices will be added to called "DLP mobile devices." Once the group is created and devices added we will do the following:

1. Head over to endpoint.microsoft.com
2. Apps > App protection policies
3. select on "create policy"
4. Configure data transfer settings under the Data protection step, Restrict cut, copy, and paste between apps to "policy managed apps"
5. Under Access requirment, well require uses to set a 4 digit pin to the cor emicrosoft apps
6. In the assignments tab we will assign the "DLP mobile devices" group.
7. review and create.

We will follow the steps from 3-7 1 more time for andriod devices.
