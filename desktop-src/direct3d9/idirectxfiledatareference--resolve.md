﻿---
Description: 'Resolves data references. Deprecated.'
ms.assetid: 'e8cf6e5d-c9b2-4a47-b058-24282dc65e74'
title: 'IDirectXFileDataReference::Resolve method'
---

# IDirectXFileDataReference::Resolve method

Resolves data references. Deprecated.

## Syntax


```C++
HRESULT Resolve(
  [out, retval] LPDIRECTXFILEDATA *ppDataObj
);
```



## Parameters

<dl> <dt>

*ppDataObj* \[out, retval\]
</dt> <dd>

Type: **[**LPDIRECTXFILEDATA**](idirectxfiledata.md)\***

Address of a pointer to an [**IDirectXFileData**](idirectxfiledata.md) interface, representing the returned file data object.

</dd> </dl>

## Return value

Type: **[**HRESULT**](455d07e9-52c3-4efb-a9dc-2955cbfd38cc)**

If the method succeeds, the return value is DXFILE\_OK. If the method fails, the return value can be one of the following values: DXFILEERR\_BADVALUE, DXFILEERR\_NOTFOUND.

## Requirements



|                    |                                                                                       |
|--------------------|---------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>DXFile.h</dt> </dl>   |
| Library<br/> | <dl> <dt>D3dxof.lib</dt> </dl> |



## See also

<dl> <dt>

[IDirectXFileDataReference](idirectxfiledatareference.md)
</dt> </dl>

 

 



