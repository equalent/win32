---
title: Retrieving the Ripping Interface
description: Retrieving the Ripping Interface
ms.assetid: '760610eb-e356-4b50-b865-53557ba9b815'
keywords: ["Windows Media Player,CD ripping", "Windows Media Player object model,CD ripping", "object model,CD ripping", "Windows Media Player ActiveX control,CD ripping", "ActiveX control,CD ripping", "Windows Media Player Mobile ActiveX control,CD ripping", "Windows Media Player Mobile,CD ripping", "CD ripping,IWMPCdromRip interface", "ripping CDs,IWMPCdromRip interface", "IWMPCdromRip interface"]
---

# Retrieving the Ripping Interface

To enumerate the CD drives on the user's computer, use the **IWMPCdromCollection** interface. Retrieve a pointer to this interface by calling [IWMPCore::get\_cdromCollection](iwmpcore-get-cdromcollection.md).

By using the [get\_count](iwmpcdromcollection-get-count.md) and [item](iwmpcdromcollection-item.md) methods, you can iterate the collection to retrieve an [IWMPCdrom](iwmpcdrom.md) interface for each CD drive on the user's computer.

The **IWMPCdrom** interface represents an individual CD drive. Before you begin ripping a CD, you must first call **QueryInterface** through an **IWMPCdrom** pointer to retrieve the [IWMPCdromRip](iwmpcdromrip.md) interface.

The following code example demonstrates how to retrieve an interface for ripping a CD from a specific drive:


```C++
HRESULT CMainDlg::GetCdromDriveCount (long &amp;lDriveCount)
{
    HRESULT hr = m_spPlayer->get_cdromCollection(&amp;m_spCdromCollection);

    // Get the number of CDROM drives.
    if (SUCCEEDED(hr))
    {
        hr = m_spCdromCollection->get_count(&amp;lDriveCount);
    }

    return hr;
}

// lIndex refers to the index of the current drive,
// which must be less than the value retrieved by
// GetCdromDriveCount above.
HRESULT CMainDlg::GetCdromRipInterface (long lIndex)
{
    // Get the IWMPCdrom interface.
    m_spCdrom.Release();
    HRESULT hr = m_spCdromCollection->item(lIndex, &amp;m_spCdrom);
    if (SUCCEEDED(hr))
    {
        // Get the IWMPCdromRip interface.
        m_spCdromRip.Release();
        hr = m_spCdrom->QueryInterface(&amp;m_spCdromRip);
    }

    return hr;
}

```



## Related topics

<dl> <dt>

[**Ripping a CD**](ripping-a-cd.md)
</dt> <dt>

[**Starting the Rip Process**](starting-the-rip-process.md)
</dt> <dt>

[**Retrieving the Rip Status**](retrieving-the-rip-status.md)
</dt> <dt>

[**Selecting Items for Ripping**](selecting-items-for-ripping.md)
</dt> <dt>

[**IWMPCdromCollection Interface**](iwmpcdromcollection.md)
</dt> </dl>

 

 



