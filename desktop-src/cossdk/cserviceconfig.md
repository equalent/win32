---
Description: Specifies and configures the services that are to be active in the service domain entered when calling either CoCreateActivity or CoEnterServiceDomain.
ms.assetid: c44743a8-8b91-4e2a-9ba4-4cb6ae787999
title: CServiceConfig class
ms.technology: desktop
ms.prod: windows
ms.author: windowssdkdev
ms.topic: interface
ms.date: 05/31/2018
---

# CServiceConfig class

Specifies and configures the services that are to be active in the service domain entered when calling either [**CoCreateActivity**](/windows/desktop/api/ComSvcs/nf-comsvcs-cocreateactivity) or [**CoEnterServiceDomain**](/windows/desktop/api/ComSvcs/nf-comsvcs-coenterservicedomain).

## When to implement

This class is implemented by COM+.



|            |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| CLSID      | CLSID\_CServiceConfig                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| ProgID     | L"COMSVCS.CServiceConfig"                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| Interfaces | [**IServiceComTIIntrinsicsConfig**](/windows/desktop/api/ComSvcs/nn-comsvcs-iservicecomtiintrinsicsconfig)<br/> [**IServiceIISIntrinsicsConfig**](/windows/desktop/api/ComSvcs/nn-comsvcs-iserviceiisintrinsicsconfig)<br/> [**IServiceInheritanceConfig**](/windows/desktop/api/ComSvcs/nn-comsvcs-iserviceinheritanceconfig)<br/> [**IServicePartitionConfig**](/windows/desktop/api/ComSvcs/nn-comsvcs-iservicepartitionconfig)<br/> [**IServiceSxSConfig**](/windows/desktop/api/ComSvcs/nn-comsvcs-iservicesxsconfig)<br/> [**IServiceSynchronizationConfig**](/windows/desktop/api/ComSvcs/nn-comsvcs-iservicesynchronizationconfig)<br/> [**IServiceThreadPoolConfig**](/windows/desktop/api/ComSvcs/nn-comsvcs-iservicethreadpoolconfig)<br/> [**IServiceTrackerConfig**](/windows/desktop/api/ComSvcs/nn-comsvcs-iservicetrackerconfig)<br/> [**IServiceTransactionConfig**](/windows/desktop/api/ComSvcs/nn-comsvcs-iservicetransactionconfig)<br/> |



 

## When to use

Use this class to configure the services that you want to use. [**CoCreateActivity**](/windows/desktop/api/ComSvcs/nf-comsvcs-cocreateactivity) and [**CoEnterServiceDomain**](/windows/desktop/api/ComSvcs/nf-comsvcs-coenterservicedomain) enable you to use the services configured by this class without needing to tie those services to a component before using them.

This class was not designed to be used in Visual Basic.

## Remarks

To create this object, call [**CoCreateInstance**](https://msdn.microsoft.com/library/windows/desktop/ms686615).

Objects instantiated from the **CServiceConfig** class aggregate the free-threaded marshaler so that they can be stored by system runtimes and reused in different apartments.

To configure an individual service, call [**QueryInterface**](https://msdn.microsoft.com/library/windows/desktop/ms682521) for the interface associated with the service and then call methods on that interface to establish the appropriate configuration.

## Requirements



|                                     |                                                                                      |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Minimum supported client<br/> | Windows XP with SP1 \[desktop apps only\]<br/>                                 |
| Minimum supported server<br/> | Windows Server 2003 \[desktop apps only\]<br/>                                 |
| Header<br/>                   | <dl> <dt>ComSvcs.h</dt> </dl> |



## See also

<dl> <dt>

[**CoCreateActivity**](/windows/desktop/api/ComSvcs/nf-comsvcs-cocreateactivity)
</dt> <dt>

[**CoCreateFreeThreadedMarshaler**](https://msdn.microsoft.com/library/windows/desktop/ms694500)
</dt> <dt>

[**CoEnterServiceDomain**](/windows/desktop/api/ComSvcs/nf-comsvcs-coenterservicedomain)
</dt> <dt>

[**CoLeaveServiceDomain**](/windows/desktop/api/ComSvcs/nf-comsvcs-coleaveservicedomain)
</dt> <dt>

[COM+ Services Without Components](com--services-without-components.md)
</dt> </dl>

 

 



