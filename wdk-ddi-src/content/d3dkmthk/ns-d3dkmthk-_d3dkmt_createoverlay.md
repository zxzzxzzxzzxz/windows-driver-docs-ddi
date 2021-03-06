---
UID: NS:d3dkmthk._D3DKMT_CREATEOVERLAY
title: "_D3DKMT_CREATEOVERLAY"
author: windows-driver-content
description: The D3DKMT_CREATEOVERLAY structure describes overlay hardware.
old-location: display\d3dkmt_createoverlay.htm
tech.root: display
ms.assetid: b020b06c-72e2-4322-a5db-fcfc46db429e
ms.author: windowsdriverdev
ms.date: 5/10/2018
ms.keywords: D3DKMT_CREATEOVERLAY, D3DKMT_CREATEOVERLAY structure [Display Devices], OpenGL_Structs_0e2cd78f-0999-48a3-8a7d-329ddb46b46f.xml, _D3DKMT_CREATEOVERLAY, d3dkmthk/D3DKMT_CREATEOVERLAY, display.d3dkmt_createoverlay
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
-	D3DKMT_CREATEOVERLAY
product:
- Windows
targetos: Windows
req.typenames: D3DKMT_CREATEOVERLAY
---

# _D3DKMT_CREATEOVERLAY structure


## -description


The D3DKMT_CREATEOVERLAY structure describes overlay hardware.


## -struct-fields




### -field VidPnSourceId

[in] The zero-based identification number of the video present source in a path of a video present network (VidPN) topology on which to overlay (that is, the identifier of the primary surface on which to overlay). 


### -field hDevice

[in] A handle to the device that the overlay is associated with.


### -field OverlayInfo

[in] A <a href="https://msdn.microsoft.com/library/windows/hardware/ff544577">D3DDDI_KERNELOVERLAYINFO</a> structure that describes information about the kernel-mode overlay object.


### -field hOverlay

[out] A D3DKMT_HANDLE data type that represents a kernel-mode handle to the kernel-mode overlay object, which represents the overlay hardware in subsequent calls by the OpenGl ICD.


## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff544577">D3DDDI_KERNELOVERLAYINFO</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff546852">D3DKMTCreateOverlay</a>
 

 

