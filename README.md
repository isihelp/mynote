# mynote
#



## How to get distribution group owner name

! GET DISTRIBUTION GROUP OWNER LISTS AND EMAIL

```
Clear-Host
$DistGroupName = Read-Host "[ Enter Distribution Group Name (Ex: DL-Name*) ]"
Get-DistributionGroup $DistGroupName | Select PrimarySMTPAddress, @{n= "ManagedBy"; e={$_.ManagedBy | foreach {(Get-Mailbox $_).PrimarySMTPAddress}}}

```
