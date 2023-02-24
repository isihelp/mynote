# mynote


### GET DISTRIBUTION GROUP OWNER LISTS AND EMAIL

```
Get-DistributionGroup DL-Field* | Select PrimarySMTPAddress, @{n= "ManagedBy"; e={$_.ManagedBy | foreach {(Get-Mailbox $_).PrimarySMTPAddress}}}
```
