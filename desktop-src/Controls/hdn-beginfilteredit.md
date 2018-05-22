---
title: HDN\_BEGINFILTEREDIT notification code
description: Notifies a header control's parent window that a filter edit has begun. This notification code is sent in the form of a WM\_NOTIFY message.
ms.assetid: '93964453-bb94-4127-8ed4-41acb226b8e2'
keywords: ["HDN_BEGINFILTEREDIT notification code Windows Controls"]
topic_type:
- apiref
api_name:
- HDN_BEGINFILTEREDIT
api_location:
- Commctrl.h
api_type:
- HeaderDef
---

# HDN\_BEGINFILTEREDIT notification code

Notifies a header control's parent window that a filter edit has begun. This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.


```C++
HDN_BEGINFILTEREDIT

   pNMHeader = (LPNMHEADER) lParam;
```



## Parameters

<dl> <dt>

*lParam* 
</dt> <dd>

A pointer to an [**NMHEADER**](nmheader.md) structure that contains additional information about the filter that is being edited.

</dd> </dl>

## Return value

No return value.

## Requirements



|                                     |                                                                                       |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Minimum supported client<br/> | Windows�Vista \[desktop apps only\]<br/>                                        |
| Minimum supported server<br/> | Windows Server�2008 \[desktop apps only\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



�

�




