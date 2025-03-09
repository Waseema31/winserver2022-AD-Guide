## Step by Step guide

### Step 1:
Deployed Windows server on VirtualBox from the below link
    [Windows server 2022](https://www.microsoft.com/en-us/evalcenter/download-windows-server-2022)

I have given 8GB Base Memory and 4CPU,Below is the Screenshot of my Firstboot after Deployment.
![First Boot ScreenShot](/Screenshots/Windowsserver2022(first%20boot).png)

### Step 2: Open "Roles and Features" in Server Manager
After the Deployment
1. Open **Server Manager**.
2. Click **Manage** on the toolbar.
3. Select **"Add Roles and Features"**.
4. Follow the wizard to install Active Directory and DNS.

**Screenshot:**  
![Roles and Features](/Screenshots/winserver(step1).png)


### Step 3: Adding AD DS and DNS Roles
1. In the Add Roles and Features Wizard, clicked Next on the Before You Begin page.
2. Selected "Role-based or feature-based installation", then click Next.
3. I Choose the server from the list (it should be selected by default), then click Next.
4. In the Server Roles section:
    - Check Active Directory Domain Services (AD DS).
    - A pop-up will appear—click Add Features.
    - Also, check DNS Server.
5. Clicked Next until you reach the Confirmation page.
5. Clicked Install and wait for the installation to complete.

**Screenshot1**
![Step3](/Screenshots/Winserver(step3).png)
**Screenshot2**
![step4](/Screenshots/Step4png.png)
**ScreenShot3**
![step5](/Screenshots/step5.png)

### Step 4:
After installing Active Directory Domain Services (AD DS), follow these steps to promote the server to a Domain Controller:

1. Clicked the flag notification icon (⚠️) at the top-right corner.
2. Clicked "Promote this server to a domain controller".

**ScreenShot**
![step6](/Screenshots/step6.png)


### Step 5: Deployment Configuration
In the Deployment Configuration window:
1. Select **Add a new forest** (since this is the first Domain Controller).
2. Entered Root Domain Name as HOME.CORP and then
Clicked Next.

**ScreenShot**
![step7](/Screenshots/step7.png)

### Step 6:
1. I made sure Domain Name System (DNS) is checked.
2. Entered a DSRM password (used for directory services recovery).
3. Clicked Next.
4. A warning about delegation—ignore it and clicked Next.
5. i left The NetBIOS domain name as suggested and clicked Next.
6. I left the database, log files, and SYSVOL paths as default. Click Next.
7. Reviewed the summary and clicked Install.
8. Once installation is complete, the server has automatically restarted.

**Screenshot**
![step8](/Screenshots/step8.png)
**Restarting windows server**
![restart](/Screenshots/Restarting.png)


***Now that my Windows Server 2022 is set up as a Domain Controller, I will join my Windows 10 client machine to the domain.***