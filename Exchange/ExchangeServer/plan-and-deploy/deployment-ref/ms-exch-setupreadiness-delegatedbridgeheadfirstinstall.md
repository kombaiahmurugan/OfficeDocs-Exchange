---
title: "Installation of the first Exchange server in the organization can't be delegated [DelegatedBridgeheadFirstInstall]"
ms.author: dstrome
author: dstrome
manager: serdars
ms.date: 11/17/2014
ms.audience: ITPro
ms.topic: reference
f1_keywords:
- 'ms.exch.setupreadiness.DelegatedBridgeheadFirstInstall'
ms.prod: exchange-server-it-pro
localization_priority: Normal
ms.assetid: bd1dbf09-5465-40fa-8668-ef99f753ba45
description: "Microsoft Exchange Server 2016 Setup can't continue because the logged-on user doesn't have the account permissions that are required to install the first Exchange 2016 server in the organization."
---

# Installation of the first Exchange server in the organization can't be delegated [DelegatedBridgeheadFirstInstall]

Microsoft Exchange Server 2016 Setup can't continue because the logged-on user doesn't have the account permissions that are required to install the first Exchange 2016 server in the organization.
  
Although Exchange 2016 Setup allows using delegation to install successive server roles, Setup requires that the user who is logged on is a member of the Enterprise Admins Windows security group when the first Exchange 2016 server in the organization is installed. This is required because Exchange 2016 Setup creates and configures objects in the Exchange Organization container in Active Directory during installation.
  
> [!NOTE]
> If you haven't prepared the Active Directory schema for Exchange 2016, the logged-on user must also be a member of the Schema Admins Windows security group. Alternately, another user who's a member of the Schema Admins Windows group can prepare the Active Directory schema before Exchange 2016 is installed.
  
To resolve this issue, add the logged-on user as a member of the Enterprise Admins security group. Or, log on to an account that's a member of the Enterprise Admins security group. Then run Exchange 2016 Setup again.
  
Having problems? Ask for help in the Exchange forums. Visit the forums at: [Exchange Server](https://go.microsoft.com/fwlink/p/?linkId=60612), [Exchange Online](https://go.microsoft.com/fwlink/p/?linkId=267542), or [Exchange Online Protection](https://go.microsoft.com/fwlink/p/?linkId=285351).
