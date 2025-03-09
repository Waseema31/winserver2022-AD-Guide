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
1. In the Add Roles and Features Wizard, click Next on the Before You Begin page.
2. Select "Role-based or feature-based installation", then click Next.
3. Choose the server from the list (it should be selected by default), then click Next.
4. In the Server Roles section:
    - Check Active Directory Domain Services (AD DS).
    - A pop-up will appear—click Add Features.
    - Also, check DNS Server.
5. Click Next until you reach the Confirmation page.
5. Click Install and wait for the installation to complete.

**Screenshot1**
![Step3](/Screenshots/Winserver(step3).png)
**Screenshot2**
![step4](/Screenshots/Step4png.png)
**ScreenShot3**
![step5]()

### Step 4:
After installing Active Directory Domain Services (AD DS), follow these steps to promote the server to a Domain Controller:

1. Click the flag notification icon (⚠️) at the top-right corner.
2. Click "Promote this server to a domain controller".

**ScreenShot**



### Step 5: 