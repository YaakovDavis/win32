---
title: WM\_GETTITLEBARINFOEX message
description: Sent to request extended title bar information. A window receives this message through its WindowProc function.
ms.assetid: 0760dbf1-5b20-471c-bfd9-b8d28b52074b
keywords:
- WM_GETTITLEBARINFOEX message Menus and Other Resources
topic_type:
- apiref
api_name:
- WM_GETTITLEBARINFOEX
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.technology: desktop
ms.prod: windows
ms.author: windowssdkdev
ms.topic: article
ms.date: 05/31/2018
---

# WM\_GETTITLEBARINFOEX message

Sent to request extended title bar information. A window receives this message through its [**WindowProc**](https://msdn.microsoft.com/library/windows/desktop/ms633573) function.


```C++
#define WM_GETTITLEBARINFOEX            0x033F
```



## Parameters

<dl> <dt>

*wParam* 
</dt> <dd>

This parameter is not used and must be 0.

</dd> <dt>

*lParam* 
</dt> <dd>

A pointer to a [**TITLEBARINFOEX**](https://msdn.microsoft.com/library/windows/desktop/aa969233) structure. The message sender is responsible for allocating memory for this structure. Set the **cbSize** member of this structure to `sizeof(TITLEBARINFOEX)` before passing this structure with the message.

</dd> </dl>

## Remarks

The following example shows how the message receiver casts an **LPARAM** value to retrieve the [**TITLEBARINFOEX**](https://msdn.microsoft.com/library/windows/desktop/aa969233) structure.

`TITLEBARINFOEX *ptinfo = (TITLEBARINFOEX *)lParam;`

## Requirements



|                                     |                                                                                                          |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Minimum supported client<br/> | Windows Vista \[desktop apps only\]<br/>                                                           |
| Minimum supported server<br/> | Windows Server 2008 \[desktop apps only\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser.h (include Windows.h)</dt> </dl> |



## See also

<dl> <dt>

[Menus Overview](menus.md)
</dt> </dl>

 

 




