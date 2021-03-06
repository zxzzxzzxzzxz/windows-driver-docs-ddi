---
UID: NS:d3dkmthk._D3DKMT_SETCONTEXTSCHEDULINGPRIORITY
title: "_D3DKMT_SETCONTEXTSCHEDULINGPRIORITY"
author: windows-driver-content
description: The D3DKMT_SETCONTEXTSCHEDULINGPRIORITY structure describes parameters for setting scheduling priority for a device context.
old-location: display\d3dkmt_setcontextschedulingpriority.htm
tech.root: display
ms.assetid: 879c7117-080a-4056-b94f-6462b370f434
ms.author: windowsdriverdev
ms.date: 5/10/2018
ms.keywords: D3DKMT_SETCONTEXTSCHEDULINGPRIORITY, D3DKMT_SETCONTEXTSCHEDULINGPRIORITY structure [Display Devices], OpenGL_Structs_d0a33042-237e-469f-93af-f6031cf54098.xml, _D3DKMT_SETCONTEXTSCHEDULINGPRIORITY, d3dkmthk/D3DKMT_SETCONTEXTSCHEDULINGPRIORITY, display.d3dkmt_setcontextschedulingpriority
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: d3dkmthk.h
req.include-header: D3dkmthk.h
req.target-type: Windows
req.target-min-winverclnt: Available in Windows Vista and later versions of the Windows operating systems.
req.target-min-winversvr: 
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
-	HeaderDef
api_location:
-	d3dkmthk.h
api_name:
-	D3DKMT_SETCONTEXTSCHEDULINGPRIORITY
product:
- Windows
targetos: Windows
req.typenames: D3DKMT_SETCONTEXTSCHEDULINGPRIORITY
---

# _D3DKMT_SETCONTEXTSCHEDULINGPRIORITY structure


## -description


The D3DKMT_SETCONTEXTSCHEDULINGPRIORITY structure describes parameters for setting scheduling priority for a device context. 


## -struct-fields




### -field hContext

[in] A D3DKMT_HANDLE data type that represents the kernel-mode handle to the device context that scheduling priority is set on.


### -field Priority

[in] The priority level to set for the device context.


## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff547163">D3DKMTSetContextSchedulingPriority</a>
 

 

