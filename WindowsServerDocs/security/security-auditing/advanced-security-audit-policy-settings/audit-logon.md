---
title: Audit Logon
description: "Windows Server Security"
ms.custom: na
ms.prod: windows-server-threshold
ms.reviewer: na
ms.suite: na
ms.technology: security-auditing
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 39524637-dd7b-438a-8639-50206d68226a
author: coreyp-at-msft
ms.author: coreyp
manager: dongill
ms.date: 10/12/2016
---
# Audit Logon

>Applies To: Windows Server&reg; 2016, Windows Server&reg; 2012 R2, Windows Server&reg; 2012

This topic for the IT professional describes the Advanced Security Audit policy setting, **Audit Logon**, which determines whether the operating system generates audit events when a user attempts to log on to a computer.

These events are related to the creation of logon sessions and occur on the computer that was accessed. For an interactive logon, events are generated on the computer that was logged on to. For a network logon, such as accessing a share, events are generated on the computer that hosts the resource that was accessed.

The following events are recorded:

-   Logon success and failure.

-   Logon attempts by using explicit credentials. This event is generated when a process attempts to log on an account by explicitly specifying that account's credentials. This most commonly occurs in batch configurations such as scheduled tasks, or when using the Runas command.

-   Security identifiers (SIDs) are filtered.

Logon events are essential to tracking user activity and detecting potential attacks.

Event volume: Low on a client computer; medium on a domain controller or network server

Default: Success for client computers; success and failure for servers

If this policy setting is configured, the following events appear on computers running the supported versions of the Windows operating system as designated in the **Applies To** list at the beginning of this topic, in addition to Windows Server 2008 and Windows Vista.

|Event ID|Event message|
|------|---------|
|4624|An account was successfully logged on.|
|4625|An account failed to log on.|
|4648|A logon was attempted using explicit credentials.|
|4675|SIDs were filtered.|

## Related resource
[Advanced Security Audit Policy Settings](../advanced-security-audit-policy-settings.md)

