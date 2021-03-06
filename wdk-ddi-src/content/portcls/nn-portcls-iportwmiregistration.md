---
UID: NN:portcls.IPortWMIRegistration
title: IPortWMIRegistration
author: windows-driver-content
description: The IPortWMIRegistration interface is provided in Windows 7 and later versions of Windows. This interface allows the miniport driver to coordinate Event Tracing for Windows (ETW) registration between PortCls and the miniport driver.
old-location: audio\iportwmiregistration.htm
tech.root: audio
ms.assetid: 0fb18e82-4853-459f-b8d3-4841ca3d8301
ms.author: windowsdriverdev
ms.date: 5/8/2018
ms.keywords: IPortWMIRegistration, IPortWMIRegistration interface [Audio Devices], IPortWMIRegistration interface [Audio Devices],described, audio.iportwmiregistration, audmp-routines_c7591b25-80f3-4d0e-ac6b-bc1dea55adb1.xml, portcls/IPortWMIRegistration
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: portcls.h
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
-	COM
api_location:
-	portcls.h
api_name:
-	IPortWMIRegistration
product:
- Windows
targetos: Windows
req.typenames: 
---

# IPortWMIRegistration interface


## -description


The <code>IPortWMIRegistration</code> interface is provided in Windows 7 and later versions of Windows. This interface allows the miniport driver to coordinate Event Tracing for Windows (ETW) registration between PortCls and the miniport driver.

ETW provides a mechanism to trace and log events that are raised by user-mode applications and kernel-mode drivers. For more information about ETW, see <a href="https://msdn.microsoft.com/library/windows/hardware/dn938554">Event Tracing for Windows</a> and <a href="http://go.microsoft.com/fwlink/p/?linkid=154129">Improve Debugging And Performance Tuning With ETW</a>.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IPortWMIRegistration</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IPortWMIRegistration</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IPortWMIRegistration</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/ff536937">IPortWMIRegistration::RegisterWMIProvider</a>
</td>
<td align="left" width="63%">
The <code>RegisterWMIProvider</code> method registers the <a href="https://msdn.microsoft.com/library/windows/hardware/dn938554">Event Tracing for Windows</a> (ETW) capability of the miniport driver with PortCls.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/ff536940">IPortWMIRegistration::UnregisterWMIProvider</a>
</td>
<td align="left" width="63%">
The <code>UnregisterWMIProvider</code> method unregisters the <a href="https://msdn.microsoft.com/library/windows/hardware/dn938554">Event Tracing for Windows</a> (ETW) interface that was previously registered with a call to the RegisterWMIProvider method. The unregistration disables the ETW registration with PortCls.

</td>
</tr>
</table> 

