## Objective
Creating a deployment profile for an Autopilot Deployment.
In the end, out Microsoft 365 will have an Autopilot deployment configures. We will also be creating and configuring a device for an Autopilot Deployment.


## Configuration

1. Within Intune, we head over to Devices > Windows > Windows Enrollment.
2. Select Create profile > Windows PC. Filled out the following information
   ![auto pilot profile](https://github.com/derinp/EnamoradoTech/blob/main/images/autopilot_1.png)
3. Withtin the next step (Out-of-box experience) we changed 2 settings
   
   -Language (Region): English (United State)
   
   -Apply Name Template: YES
     -Name: ETREM1%RAND:4%
   
     Note: For the name this will rename the device to the following ETREMxxxx with the x's being replaced by a random 4 digits.
   ![device naming](https://github.com/derinp/EnamoradoTech/blob/main/images/naming.png)
4. In the Assignments step, well just hit next.
5. Lastly, well hit Create in the Review + Create step.
   ![autopilot config create](https://github.com/derinp/EnamoradoTech/blob/main/images/apcreate.png)
6. Well head back over to https://entra.microsoft.com/ and create a company branding.
7. Under Default sign-in experience we will select Customize.
8. Here we added a background image (looked online for a miami vide themed background)
9. A simple Autopilot Deployment is now ready

## Configure Device for an Autopilot Deployment
I have a spare windows 10 pro device that I will Deploy with Autopilot.

1. I have already reimaged the device, so we will begin from the "selecting country or region" screen on a machine.
2. go through the typical limited set up without internet access. We need to grab the Hardware ID for the machine.
3. Created a profile with ETAdmin account name
4. After profile was configured, we go to the machines updates and pause it for a week (from soem articles i read, its important to do this to verify next step works)
5. On the laptop, we go to Access Work or School and "Export your management log files"
6. Going to the Cabinet File that was generated, I searched for the "Device_Hash(desktop name).csv" file. Put that on a USB
7. Head to endpoint.microsoft.com
8. Within endpoint manager, go to Devices > By Platform > Windows > Enrollment
9. Under Windows Autopilot select "devices"
10. Selected Import and then upload the csv file that we got from the laptops Cabinet file
11. This will take some time to process.

## Deploying the Laptop with Autopilot
1. Opening the command prompt as admin well run the following commands:
> cd sysprep
> 
> sysprep -generalize -oobe -reboo

2. The machine will restart a few times
3. We will now sign in with our Microsoft 365 account.
4. We can Verify Everything worked by going to command prompt and typing "hostname", This should give us something along the lines of "ETREMxxxx" with the x's being numbers.
5. We can also head over to endpoint.microsoft.com. Under devices, we can go to all devices and see the registered device now.
![device naming](https://github.com/derinp/EnamoradoTech/blob/main/images/etrem.png)
