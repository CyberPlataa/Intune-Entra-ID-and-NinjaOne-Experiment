# Intune-Entra-ID-and-NinjaOne-Experiment
Creating a homelab using Intune, Entra ID, and NinjaOne to familiarize myself with current cloud technologies. 

Created an Intune and Entra ID account. Took much longer than expected, noted that when starting an account you must go directly to ENTRA and pick up an INTUNE license from there. 

1) Created policies for devices and configured security settings.
   - Broke down device set up/settings into iOS and Windows. Please note that proper configuration of iOS devices will require a specific Apple Business License.   <img width="2484" height="1229" alt="creatingmobiledevicecompliancepolicy" src="https://github.com/user-attachments/assets/bad7dc09-fe7f-468d-b900-6c817280a1e4" />
<img width="883" height="1102" alt="DeviceEnrollmentsetup" src="https://github.com/user-attachments/assets/1366e595-29fc-4b8c-ae20-d135a433d340" />



2) Found a way to create a specific script for Windows devices when they are added to our network. Specifically to delete the bloatware that is normally installed in Windows 11. This is a common occurrence in work environment too. Adding unneccesary programs/Apps kills device performance. (I know there are more specific scripts out there but I am solely focusing on one that I wrote)

   <img width="2265" height="924" alt="Scriptbeingcreatedinplatformscripts" src="https://github.com/user-attachments/assets/a2418cb7-95a0-4aca-bd76-beba7a232e0a" />
<img width="979" height="811" alt="ScreenshotofScript" src="https://github.com/user-attachments/assets/c1836a62-5989-42ee-b8c7-dcfd3a24aa8c" />


3) I accidentally failed sign ins from a specific account several times. Good to know that there was a troubleshooting guide that was attached by Windows. Its a great starting point and nice for referencing.
<img width="2219" height="1274" alt="troubleshootingstepsandguidancefromEntraID" src="https://github.com/user-attachments/assets/b30f9f68-e5cf-4194-85da-8bc6ffe2fbc9" />






<img width="2056" height="982" alt="succesfullysetupPAUL" src="https://github.com/user-attachments/assets/15c9c23a-7c4b-4870-8c33-66632e5b4685" />

^The set up of my first user on the VM was a huge success. After tinkering with MFA, and the hurdles of properly configuring the VM settings I succesfully added my first user to the environment. 

FUTURE STEP: NinjaONE set up

Issues at this point:
VM- Windows 11 required secure boot, TPM 2.0, and 2 core processor to properly configure. Took a second to dig into the VM settings. Haven't used Virtualbox in a while! 
MFA Issues - Did not write down password I had set for one of the USERs, leading me to be unable to sign in on the VM that was set up via virtual box. Reset password lead me nowhere and had to create an entirely new account. 
MDM Authority - I had trouble initally even getting to the log in screen. None of the users had the proper licenses assigned to them. I had to get into the MDM authority to intune. Link wasn't on the main dashboard, and I had to find it through a Microsoft HELP page. 
