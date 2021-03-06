---
UID: NC:d3dkmddi.DXGKDDI_SETPOINTERPOSITION
title: DXGKDDI_SETPOINTERPOSITION
author: windows-driver-content
description: The DxgkDdiSetPointerPosition function sets the location and visibility state of the mouse pointer.
old-location: display\dxgkddisetpointerposition.htm
tech.root: display
ms.assetid: b30e4f19-068c-4ab0-a2e9-b1f57592be1c
ms.author: windowsdriverdev
ms.date: 5/10/2018
ms.keywords: DXGKDDI_SETPOINTERPOSITION, DXGKDDI_SETPOINTERPOSITION callback, DmFunctions_1067a75d-aece-48c2-93c1-35465c57c07e.xml, DxgkDdiSetPointerPosition, DxgkDdiSetPointerPosition callback function [Display Devices], d3dkmddi/DxgkDdiSetPointerPosition, display.dxgkddisetpointerposition
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: callback
req.header: d3dkmddi.h
req.include-header: D3dkmddi.h
req.target-type: Desktop
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
req.irql: PASSIVE_LEVEL
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	UserDefined
api_location:
-	d3dkmddi.h
api_name:
-	DxgkDdiSetPointerPosition
product:
- Windows
targetos: Windows
req.typenames: 
---

# DXGKDDI_SETPOINTERPOSITION callback function


## -description


The <i>DxgkDdiSetPointerPosition</i> function sets the location and visibility state of the mouse pointer.


## -parameters




### -param hAdapter [in]

[in] A handle to a context block that is associated with a display adapter. The display miniport driver previously provided this handle to the Microsoft DirectX graphics kernel subsystem in the <i>MiniportDeviceContext</i> output parameter of the <a href="https://msdn.microsoft.com/5fd4046f-54c3-4dfc-8d51-0d9ebcde0bea">DxgkDdiAddDevice</a> function.


### -param pSetPointerPosition [in]

[in] A pointer to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff557660">DXGKARG_SETPOINTERPOSITION</a> structure that describes where and how to display the mouse pointer.


## -returns



<i>DxgkDdiSetPointerPosition</i> returns STATUS_SUCCESS if it succeeds; otherwise, it returns one of the error codes defined in <i>Ntstatus.h</i>.




## -remarks



The DirectX graphics kernel subsystem calls the display miniport driver's <i>DxgkDdiSetPointerPosition</i> function to set the location of the mouse pointer. The <i>DxgkDdiSetPointerPosition</i> function is called independently of all of the other display miniport driver functions. Therefore, a <i>DxgkDdiSetPointerPosition</i> thread can run simultaneously with another display miniport driver thread. However, the system ensures that <i>DxgkDdiSetPointerPosition</i> and <a href="https://msdn.microsoft.com/36b462f7-5bad-4716-8138-af00d20e945b">DxgkDdiSetPointerShape</a> threads cannot run simultaneously. 

If you run a <i>DxgkDdiSetPointerPosition</i> thread simultaneously with another display miniport driver thread, the display miniport driver should be able to program the mouse pointer hardware independently of other activities, such as operations that send a command buffer through direct memory access (DMA) to the graphics hardware, operations that program the graphics hardware by using memory-mapped I/O (MMIO), and so on.

<i>DxgkDdiSetPointerPosition</i> can be called even if the video present network (VidPN) topology that is associated with the <b>VidPnSourceId</b> member of the <a href="https://msdn.microsoft.com/library/windows/hardware/ff557660">DXGKARG_SETPOINTERPOSITION</a> structure that the <i>pSetPointerPosition</i> parameter points to is disabled. In this case, the driver should return STATUS_SUCCESS but should make no changes to the state of the driver or hardware.

<i>DxgkDdiSetPointerPosition</i> should be made pageable.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff557660">DXGKARG_SETPOINTERPOSITION</a>



<a href="https://msdn.microsoft.com/5fd4046f-54c3-4dfc-8d51-0d9ebcde0bea">DxgkDdiAddDevice</a>



<a href="https://msdn.microsoft.com/36b462f7-5bad-4716-8138-af00d20e945b">DxgkDdiSetPointerShape</a>
 

 

