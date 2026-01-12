📘Windows 10 Hardening Project(Domain GPO Baseline)

This project demonstrates a full Windows 10 enterprise hardening baseline using Active Directory,Group Policy, and a Windows Server 2019 Domain Controller.

The Goal was to secure a Windows 10 workstation by applying industry-standard security controls across the OS,Network stack, and identity layer.

This Project is designed for Cyberseurity, IT Support, and System Administrations portfolios.

🛠️Lab Environment

  -Windows Server 2019(Domain Controller)
  
  -Windows 10 Client(Domain Joined)
  
  -Oracle VirtualBox
  
  -Group Policy Management Console
  
  -PowerShell

🛡️Hardening Controls Implemented

Each control was configured through domain-based Group Policy Objects(GPOs)and verified on the Windows 10 Client

 1. Firewall Enforcement

     - Enabled Windows Defender Firewall(Domain,Private)

     - Block Inbound, allow outbound

     - Enabled logging for dropped packets

2. SMBv1 Disabled

   - Verified via Powershell:


          Get-WindowsOptionalFeature -Online -FeatureName SMB1Protocol

3. RDP Hardening

   - Enforced Network Level Authentication(NLA)
   - Restricted RDP access to Domain Admins only

4. Deny Local Accounts RDP

   Added:

   - Local Account

   - Local Account and Administrators Group

   - Guests
   to Deny log on through Remote Desktop Services

5. LLMNR Disabled

    - "Turn off multicast name resolution"=Enabled

6. IPv6 Transition Technologies Disabled

    - Teredo=Disabled

    - 6to4=Disabled

    - ISATAP=Disabled

    - IP-HTTPS=Disabled

7. Guest Account Disabled & Renamed

    - Guest account disabled

    - Renamed to Guest-Disabled

8. Anynomous SID Enumeration Disabled

    - Allow anonymous SID/Name translation=Disabled
    - Do not allow anonymous enumeration of SAM accounts and shares= Enabled

9. AutoRun & AutoPlay Disabled

    - Turn off Autoplay= Enabled > All drives

10. SmartScreen Enabled

    - Configure Windows Defender SmartScreen= Enabled > Warn and prevent bypass

   



📂 Project Structure













