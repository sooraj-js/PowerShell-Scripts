# PowerShell-Scripts
This PowerShell script helps extract key details of any installed software, including:

DisplayName
DisplayVersion
InstallDate
Publisher
InstallLocation
PSPath
QuietUninstallString
UninstallString

Typically, we manually navigate through the Registry:
HKEY_LOCAL_MACHINE > Software > Microsoft > Windows > CurrentVersion > Uninstall
Or, HKEY_LOCAL_MACHINE > Software > WOW6432Node > Microsoft > Windows > CurrentVersion > Uninstall
to locate the relevant registry entries for installed software details.

Instead, this PowerShell script simplifies the process by fetching all required details in one go.

In the third row of the script, modify the software name in:
Where-Object {$_.DisplayName -like "*C++*"}
For example, use "*Google*" to filter results for Google Chrome, or modify it accordingly for other software.
