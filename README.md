# Crypto-Harden-GPO
A series of powershell-command scripts that create GPO's that help with hardening the crypto settings on target Windows systems within an AD domain

Based the commands off the hardening script available from https://www.hass.de/content/setup-microsoft-windows-or-iis-ssl-perfect-forward-secrecy-and-tls-12

That hass.de script seems intended for use on single/individual servers - wanted to see if I could base the same changes for use into a GPO that could be applied to a mass of systems within an Active Directory domain.

---

There are four scripts in this collection:

-) A base script that is used to set the main crypto settings (enabling/disabling various cryptographic functions) - this is intended to apply to all reasonably possible targets

-) Three cipher-order scheme scripts, each targeted to a subset of Windows system types, based on OS-age groupings

--) One that targets older systems (Windows Server 2008, 2008R2, 2012, 2012R2)

--) One that targets middle-aged systems (Windows 10, Windows Server 2016, 2019)

--) One that targets newer systems (Windows 11, Windows 2022 or higher)

The base script should be tested/used at minimum, followed by at least one of the cipher-order scheme scripts, depending on the target machines in scope within your organization.

---

Procedures:

-) Download the relevant scripts

-) Review them

-) Edit the variables within the scripts to set the (GPO) Policy Name, Domain and Server.  Save your changes

-) Use/Run the relevant/updated scripts to create the new named GPO's within your targeted domain

-) Review the newly created GPO objects and ensure that they look "clean"

-) Link the GPO to a test environment.  Test, test again and when you think you're done testing, test one more time.  This change *can* break things if you haven't prepared.

-) Move on to other environments if/when you feel safe/comfortable enough to do so.

