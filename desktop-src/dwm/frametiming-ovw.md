---
title: Accessing and Controlling DWM Frame Data
description: This topic discusses the Desktop Window Manager (DWM) APIs that are used for scheduling and media presentation.
ms.assetid: 'e5d010ea-8411-4537-b9f8-6dc84841087a'
keywords: ["Desktop Window Manager (DWM),scheduling and media presentation APIs", "DWM (Desktop Window Manager),scheduling and media presentation APIs", "scheduling and media presentation APIs", "Desktop Window Manager (DWM),accessing frame data", "DWM (Desktop Window Manager),accessing frame data", "accessing frame data", "Desktop Window Manager (DWM),controlling frame data", "DWM (Desktop Window Manager),controlling frame data", "controlling frame data"]
---

# Accessing and Controlling DWM Frame Data

This topic discusses the Desktop Window Manager (DWM) APIs that are used for scheduling and media presentation.

## DWM Frame Timing API

The scheduling and media presentation APIs enable more detailed control of when the desktop image is composited and presented. This is typically needed by media and video playback applications for whom the DWM is running asynchronously with their own presentation schedule, which can lead to sampling artifacts if not tightly controlled.

The scheduling and media presentation functions include the following. Details of their use are found on those pages.

-   [**DwmEnableMMCSS**](dwmenablemmcss.md). Notifies the DWM to enable Multimedia Class Schedule Service (MMCSS) scheduling while the calling process is alive.
-   [**DwmGetCompositionTimingInfo**](dwmgetcompositiontiminginfo.md). Retrieves the current composition timing information.
-   [**DwmModifyPreviousDxFrameDuration**](dwmmodifypreviousdxframeduration.md). Changes the number of refreshes during which the previous frame will be displayed.
-   [**DwmSetDxFrameDuration**](dwmsetdxframeduration.md). Sets the number of refreshes in which to display the presented frame.
-   [**DwmSetPresentParameters**](dwmsetpresentparameters.md). Sets the present parameters for frame composition.

 

 



