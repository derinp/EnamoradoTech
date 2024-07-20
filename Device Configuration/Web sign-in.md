## Web Sign-In and Temporary Access Pass (TAP) Setup
One of our top priorities is implementing web sign-in for devices registered to the Enamorado Tech O365 tenant. This enhancement will significantly streamline IT operations and benefit Enamorado Tech employees.

## Use Cases
Web sign-in and TAPs offer several advantages. Here are two key scenarios:

1. New Machine Setup:
When provisioning a new machine for a user, an IT technician can create a TAP and sign in to the machine using it.
TAPs are secure because they expire after a specified time.
This process simplifies initial setup and ensures security.
2. Password Resets:
If a user forgets their password, an IT technician can issue a TAP to the user.
The user can then sign in with the TAP and update their password.
## Implementation Steps
To achieve this, follow these steps:

1. Create a Security Group:
Establish a security group named “Web Sign-In Enabled.”
Add devices to this group.
2. Policy Configuration:
Create a policy that affects the “Web Sign-In Enabled” group.
Configure the necessary options based on the articles below.
Resources
Learn more about TAPs and web sign-in:

Authentication with Temporary Access Pass
Web Sign-In in Windows
After completing these steps, we are now able to utilize web sign-in on Enamorado Tech O365 tenant machines as indicated by the globe icon on the log in page:
![screenshot of first email.](https://github.com/derinp/EnamoradoTech/blob/main/images/websignin.png)
