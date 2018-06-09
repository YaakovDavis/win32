---
title: Registry Entries
ms.assetid: f4f8875c-6416-4919-b49b-bcd675efcbd2
description: 
ms.technology: desktop
ms.prod: windows
ms.author: windowssdkdev
ms.topic: article
ms.date: 05/31/2018
---

# Registry Entries

Registry values in the following registry keys control aspects of the functionality of COM:

-   [**HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Classes**](hkey-local-machine-software-classes.md)
-   [**HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\Ole**](hkey-local-machine-software-microsoft-ole.md)
-   [**HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\Windows NT\\CurrentVersion**](hkey-local-machine-software-microsoft-windows-nt-currentversion.md)

As of Windows Server 2003, COM uses only the current process token to decide which registry hive to access, not the thread token. If COM is not able to access the user profile registry hive, it will access the **HKEY\_LOCAL\_MACHINE\\System** hive.

## Related topics

<dl> <dt>

[Registry](https://msdn.microsoft.com/library/windows/desktop/ms724871)
</dt> </dl>

 

 



