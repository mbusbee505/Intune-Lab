# Intune Lab

## About This Project

This lab is an end-to-end walkthrough of building a production-style Microsoft endpoint management environment from scratch using **Intune**, **Autopilot**, **Entra ID**, and **Defender for Endpoint**. The goal was to simulate the kind of work a real IT or endpoint admin would do when onboarding users and securing a fleet of devices, both Windows and mobile.

To keep things realistic, I generated a synthetic 25-user dataset with randomized names, departments, and job titles to simulate a small company I called BusbeeCorp. That CSV, along with exported Intune and Entra configurations, all live in this repo so anyone can clone and reuse them in their own tenant.

## What This Lab Covers

- Zero-touch Windows device provisioning with Autopilot and a customized OOBE
- User and group management in Entra ID using dynamic membership rules
- License assignment via both the portal and PowerShell
- App deployment for Chrome, Zoom, Office, and GlobalProtect VPN
- Update rings with a pilot and broad deployment group
- Security baselines, Defender for Endpoint integration, compliance policies, and Conditional Access enforcement
- iOS enrollment using Apple Push Notification certificates and Company Portal
- Android enrollment using Managed Google Play

## Skills Demonstrated

- Microsoft Intune and Autopilot configuration
- Entra ID user/group management and dynamic group rules
- Role-based access and license management
- App lifecycle management across Windows, iOS, and Android
- Endpoint security hardening using baselines and Defender for Endpoint
- Conditional Access policy design
- PowerShell scripting for Microsoft Graph and Intune automation
- Exporting and version-controlling Intune and Entra configurations

## Lab Writeup

Each section below links to a dedicated page with full steps and screenshots.

1. [**Set up the lab environment**](Writeup/01-setting-up-the-lab.md)
   1. Sign up for free trials
   2. Upload users to Entra
   3. Create groups in Entra
   4. Assign licenses to users
2. [**Enroll devices to Intune**](Writeup/02-enrolling-devices.md)
   1. Gather hardware hashes
   2. Create deployment profile
   3. Configure Enrollment Status Page
   4. Confirm OOBE proof of concept
3. [**Improve OOBE experience**](Writeup/03-polishing-oobe.md)
   1. Remove unnecessary user prompts
4. [**Install apps**](Writeup/04-installing-apps.md)
   1. Google Chrome
   2. Zoom
   3. Microsoft Office
   4. GlobalProtect VPN
5. [**Configure update rings**](Writeup/05-creating-update-rings.md)
   1. Pilot group
   2. Broad user group
6. [**Improve security posture**](Writeup/06-securing-devices.md)
   1. Install security baselines
   2. Connect Defender for Endpoint
   3. Create compliance policies
   4. Enforce compliance via Conditional Access
7. [**Set up iPhone enrollments**](Writeup/07-enrolling-iphones.md)
   1. Apple Push Notification certificate
   2. Company Portal app
   3. User login and profile installation
   4. Deploy Intune apps from Company Portal
8. [**Set up Android enrollments**](Writeup/08-enrolling-androids.md)
   1. Connect Managed Google Play
   2. Company Portal login
   3. Deploy Intune apps from Managed Play Store
9. [**Monitor and report**](Writeup/09-monitor-and-report.md)
10. [**Conclusion and artifact export**](Writeup/10-conclusion.md)

## Repo Contents

| Folder / File | What it is |
|---|---|
| `Writeup/` | Step-by-step lab documentation with screenshots |
| `IntuneBackup/` | Exported Intune policies, profiles, and app configs |
| `EntraBackup/` | Exported Entra users, groups, and settings |
| `busbeecorp_user_import.csv` | Synthetic user dataset used to populate the tenant |

> **Note:** In a real environment you would not want to publicly share compliance policies or Conditional Access configurations, as that information could help a threat actor plan around your defenses. The data in this repo is entirely synthetic and the tenant has been deleted.

## Helpful Links

### Admin Portals

- **Intune admin center:** https://intune.microsoft.com
- **Entra admin center:** https://entra.microsoft.com
- **Defender portal:** https://security.microsoft.com

### Microsoft 365 Free Trials

- **Intune free trial:** https://aka.ms/IntuneTrial
- **Entra ID free trial:** https://aka.ms/EntraSuiteTrial
- **Defender for Endpoint P2 trial:** https://www.microsoft.com/security/business/endpoint-security/microsoft-defender-endpoint