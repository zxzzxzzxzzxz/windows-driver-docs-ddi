---
UID: NF:wdm.KeIsExecutingDpc
title: KeIsExecutingDpc function
author: windows-driver-content
description: Checks whether a DPC is being executed on current processor.
ms.assetid: b75e1f85-98c7-47b1-bb12-b4c76127e8c4
ms.author: windowsdriverdev
ms.date: 
ms.topic: function
ms.keywords: KeIsExecutingDpc
req.header: wdm.h
req.include-header:
req.target-type:
req.target-min-winverclnt: Windows 10, version 1803
req.target-min-winversvr:
req.kmdf-ver:
req.umdf-ver:
req.lib:
req.dll:
req.irql: DISPATCH_LEVEL
req.ddi-compliance:
req.unicode-ansi:
req.idl:
req.max-support:
req.namespace:
req.assembly:
req.type-library: 
topic_type: 
-	apiref
api_type: 
-	DllExport
api_location: 
-	NtosKrnl.exe
api_name: 
-	KeIsExecutingDpc
product: Windows
targetos: Windows

---

# KeIsExecutingDpc function


## -description

Checks whether a DPC is being executed on current processor.

## -parameters


## -returns
This function returns a non-zero value if a DPC is currently being executed on the current processor. Otherwise, retunrs zero. 

## -remarks

## -see-also