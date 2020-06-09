+++
author = "Rick Neeft"
title = "Remove SharePoint Online Site With PowerShell"
date = "2018-02-21"
description = "Removing a Site collection in the admin page in SharePoint takes 30 days to be removed. With PowerShell this can be faster."
tags = [
    "sharepoint",
    "powershell",
    "how-to"
]
+++
Removing a Site collection in the admin page in SharePoint takes 30 days to be removed. With PowerShell this can be faster.

```
PS C:\> import-module Microsoft.Online.Sharepoint.PowerShell
PS C:\> connect-sposervice –url https://<site>-admin.sharepoint.com
PS C:\> remove-sposite –identity <site-collection> -nowait
```
