# PowerShell Commands
---

##### Install and Configure

`Install-Module -Name MicrosoftPowerBIMgmt`

`Update-Module -Name MicrosoftPowerBIMgmt`

##### Install separately

`Install-Module -Name MicrosoftPowerBIMgmt.Workspaces`

`Install-Module -Name MicrosoftPowerBIMgmt.Admin`

`Install-Module -Name MicrosoftPowerBIMgmt.Capacities`

`Install-Module -Name MicrosoftPowerBIMgmt.Data Module`

`Install-Module -Name MicrosoftPowerBIMgmt.Profile`

`Install-Module -Name MicrosoftPowerBIMgmt.Reports`

##### Get List of modules
`Get-Module MicrosoftPowerBIMgmt* -ListAvailable`


##### Uninstall module
`Get-Module MicrosoftPowerBIMgmt* -ListAvailable | Uninstall-Module -Force`

##### Authenticate
`Connect-PowerBIServiceAccount`   
`Login-PowerBIServiceAccount`
`Login-PowerBI`


##### Get Workspace for user
`Get-PowerBIWorkspace`

##### Show all Workspaces for Tenant Admin
`Get-PowerBIWorkspace -Scope Organization -All`


##### Update Workspace
`Set-PowerBIWorkspace -Scope Organization -Id "4b4896c1-b155-4f5c-bb8b-c406f39c3279" -Name "New Name" -Description "New Description"`


##### Add user to workspace
`Add-PowerBIWorkspaceUser -Scope Organization -Id 4b4896c1-b155-4f5c-bb8b-c406f39c3279 -UserEmailAddress alexw@girishmvp.onmicrosoft.com -AccessRight Contributor`

##### View Deleted Workspace
`Get-PowerBIWorkspace -Scope Organization -Deleted -All`


##### Restore Deleted Workspace
`Restore-PowerBIWorkspace -Id "7b27d839-e34c-4645-8880-b82f380d66cf" -RestoredName "Girish UAT Workspace" -AdminEmailAddress "girishuppal@girishmvp.onmicrosoft.com"`


##### Recover Orphaned Workspace
`Get-PowerBIWorkspace -Scope Organization -Orphaned -All`


##### Get Reports
`Get-PowerBIReport`

#####  Get Dashboard
`Get-PowerBIDashboard`

##### Power BI Import
`Get-PowerBIImport`

##### Create new Report
`New-PowerBIReport -Path 'C:\girish\code\power-bi\pbi-demo-001\Alpha.pbix' -Name 'Giri Report'`

`New-PowerBIReport -Path 'C:\girish\code\power-bi\pbi-demo-001\Alpha.pbix' -Name 'New Report' -WorkspaceId 7b27d839-e34c-4645-8880-b82f380d66cf`

##### Export Power BI Report
`Export-PowerBIReport -Id 7af36d1d-6c80-4a1c-b67f-721cc45c5b16 -OutFile 'c:\car.pbix'`