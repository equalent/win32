---
Description: Enables the capture engine to use a decoder that has field-of-use restrictions.
ms.assetid: EDE6D207-FD84-4DEB-9BF5-0952C454B00F
title: MF_CAPTURE_ENGINE_DECODER_MFT_FIELDOFUSE_UNLOCK_Attribute attribute (Mfcaptureengine.h)
ms.topic: reference
ms.date: 05/31/2018
---

# MF\_CAPTURE\_ENGINE\_DECODER\_MFT\_FIELDOFUSE\_UNLOCK\_Attribute attribute

Enables the capture engine to use a decoder that has field-of-use restrictions.

## Data type

**IUnknown\***

## Remarks

The value of this attribute is a pointer to the [**IMFFieldOfUseMFTUnlock**](/windows/desktop/api/mfidl/nn-mfidl-imffieldofusemftunlock) interface, implemented by the caller. The caller's implementation of this interface is expected to perform a handshake with the decoder, as described in [Field of Use Restrictions](field-of-use-restrictions.md). Microsoft Media Foundation does not define the handshake—typically, it would involve some sort of cryptographic exchange.

Internally, the capture engine sets the [**IMFFieldOfUseMFTUnlock**](/windows/desktop/api/mfidl/nn-mfidl-imffieldofusemftunlock) pointer on the decoder by setting the decoder's [MFT\_FIELDOFUSE\_UNLOCK\_Attribute](mft-fieldofuse-unlock-attribute.md) attribute.

## Requirements



|                                     |                                                                                              |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| Minimum supported client<br/> | Windows 8 \[desktop apps only\]<br/>                                                   |
| Minimum supported server<br/> | Windows Server 2012 \[desktop apps only\]<br/>                                         |
| Header<br/>                   | <dl> <dt>Mfcaptureengine.h</dt> </dl> |



## See also

<dl> <dt>

[Alphabetical List of Media Foundation Attributes](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Capture Engine Attributes](capture-engine-attributes.md)
</dt> <dt>

[**IMFCaptureEngine::Initialize**](/windows/desktop/api/mfcaptureengine/nf-mfcaptureengine-imfcaptureengine-initialize)
</dt> </dl>

 

 




