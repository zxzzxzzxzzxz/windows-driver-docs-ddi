---
UID: NC:d3dkmddi.DXGKDDI_SETTARGETGAMMA
title: DXGKDDI_SETTARGETGAMMA
author: windows-driver-content
description: Allows the gamma LUT to be set on a path which is identified by the target id.Note  This is functionally equivalent to the DxgkDdi_UpdateActiveVidPnPresentPath in previous WDDM versions if only the D3DKMDT_GAMMA_RAMP field is changed. .
old-location: display\dxgkddi_settargetgamma.htm
tech.root: display
ms.assetid: 658EA0AA-80FC-4A45-B2EF-DFE928917E7B
ms.author: windowsdriverdev
ms.date: 5/10/2018
ms.keywords: DXGKDDI_SETTARGETGAMMA, DXGKDDI_SETTARGETGAMMA callback, DXGKDDI_SETTARGETGAMMA callback function [Display Devices], d3dkmddi/DXGKDDI_SETTARGETGAMMA, display.dxgkddi_settargetgamma
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: callback
req.header: d3dkmddi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
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
-	UserDefined
api_location:
-	d3dkmddi.h
api_name:
-	DXGKDDI_SETTARGETGAMMA
product:
- Windows
targetos: Windows
req.typenames: 
---

# DXGKDDI_SETTARGETGAMMA callback function


## -description


Allows the gamma LUT to be set on a path which is identified by the target id.<div class="alert"><b>Note</b>  This is functionally equivalent to the DxgkDdi_UpdateActiveVidPnPresentPath in previous WDDM versions if only the D3DKMDT_GAMMA_RAMP field is changed.</div>
<div> </div>



## -parameters




### -param hAdapter [in]

A handle that identifies the adapter.


### -param pSetTargetGammaArg [in]

A pointer to a <a href="https://msdn.microsoft.com/94BA40BD-3B56-44EF-BAD4-49556E68C550">DXGKARG_SETTARGETGAMMA</a> structure that provides the target id to be modified and provides the gamma ramp to be set.


## -returns



If this routine succeeds, it returns STATUS_SUCCESS. 

<div class="alert"><b>Note</b>  WDDM 2.2 has cap bits for each type of supported gamma ramp so unsupported types will be skipped by the OS. Therefore, if the type is supported there should be no reason to fail the call other than unavoidable failures like monitor unplug.</div>
<div> </div>



## -remarks



This function is always called at PASSIVE level so the supporting code should be made pageable.



