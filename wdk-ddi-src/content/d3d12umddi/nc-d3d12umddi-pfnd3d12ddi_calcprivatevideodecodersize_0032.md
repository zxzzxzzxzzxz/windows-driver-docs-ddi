---
UID: NC:d3d12umddi.PFND3D12DDI_CALCPRIVATEVIDEODECODERSIZE_0032
title: PFND3D12DDI_CALCPRIVATEVIDEODECODERSIZE_0032
author: windows-driver-content
description: Used to calculate the size of a video decoder.
old-location: display\pfnd3d12ddi_calcprivatevideodecodersize_0032.htm
tech.root: display
ms.assetid: 90F05A41-692B-4301-81F3-56035072C8A3
ms.author: windowsdriverdev
ms.date: 4/16/2018
ms.keywords: PFND3D12DDI_CALCPRIVATEVIDEODECODERSIZE_0032, PFND3D12DDI_CALCPRIVATEVIDEODECODERSIZE_0032 entry, PFND3D12DDI_CALCPRIVATEVIDEODECODERSIZE_0032 entry point [Display Devices], d3d12umddi/PFND3D12DDI_CALCPRIVATEVIDEODECODERSIZE_0032, display.pfnd3d12ddi_calcprivatevideodecodersize_0032
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: callback
req.header: d3d12umddi.h
req.include-header:
req.target-type: Windows
req.target-min-winverclnt: Windows 10
req.target-min-winversvr: Windows Server 2016
req.kmdf-ver:
req.umdf-ver:
req.ddi-compliance:
req.unicode-ansi:
req.idl:
req.max-support:
req.namespace:
req.assembly:
req.type-library:
req.lib:
req.dll:
req.irql:
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	UserDefined
api_location:
-	d3d12umddi.h
api_name:
-	PFND3D12DDI_CALCPRIVATEVIDEODECODERSIZE_0032
product:
- Windows
targetos: Windows
req.typenames:
---

# PFND3D12DDI_CALCPRIVATEVIDEODECODERSIZE_0032 callback function


## -description


Used to calculate the size of a video decoder. The D3D runtime allocates memory for storing the drivers CPU object representing the video decoder.


## -parameters




### -param hDrvDevice

The hardware device being processed.


### -param *pArgs

[in] The arguments used to create a video decoder.


## -returns



Returns the size of the video decoder in bytes.



