---
title: WM\_ADSPROP\_NOTIFY\_EXIT message
description: An Active Directory property sheet extension sends the WM\_ADSPROP\_NOTIFY\_EXIT message to the notification object when the notification object is no longer required.
audience: developer
author: REDMOND\\markl
manager: REDMOND\\mbaldwin
ms.assetid: 'b0f58c73-8953-412d-b801-bf34967fe0b4'
ms.prod: 'windows-server-dev'
ms.technology: 'active-directory-domain-services'
ms.tgt_platform: multiple
keywords: ["WM_ADSPROP_NOTIFY_EXIT message Active Directory"]
topic_type:
- apiref
api_name:
- WM_ADSPROP_NOTIFY_EXIT
api_location:
- Adsprop.h
api_type:
- HeaderDef
---

# WM\_ADSPROP\_NOTIFY\_EXIT message

An Active Directory property sheet extension sends the **WM\_ADSPROP\_NOTIFY\_EXIT** message to the notification object when the notification object is no longer required.


```C++
WM_ADSPROP_NOTIFY_EXIT

    WPARAM wParam
    LPARAM lParam
    
```



## Parameters

<dl> <dt>

*hwnd* 
</dt> <dd>

The handle of the notification object. To obtain this handle, call [**ADsPropCreateNotifyObj**](adspropcreatenotifyobj.md).

</dd> <dt>

*wParam* 
</dt> <dd>

Not used.

</dd> <dt>

*lParam* 
</dt> <dd>

Not used.

</dd> </dl>

## Return value

This message has no return value.

## Remarks

The notification object will delete itself in response to this message. When this message has been sent, the notification object handle should be considered invalid.

## Requirements



|                                     |                                                                                      |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Minimum supported client<br/> | Windows�Vista<br/>                                                             |
| Minimum supported server<br/> | Windows Server�2008<br/>                                                       |
| Header<br/>                   | <dl> <dt>Adsprop.h</dt> </dl> |



## See also

<dl> <dt>

[**ADsPropCreateNotifyObj**](adspropcreatenotifyobj.md)
</dt> <dt>

[Messages in Active Directory Domain Services](messages-in-active-directory-domain-services.md)
</dt> </dl>

�

�




