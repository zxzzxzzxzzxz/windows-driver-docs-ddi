---
UID: NF:portabledevicetypes.IPortableDeviceValues.GetKeyValue
title: IPortableDeviceValues::GetKeyValue
author: windows-driver-content
description: Retrieves a PROPERTYKEY value (type VT_UNKNOWN) that is specified by a key.
old-location: wpddk\iportabledevicevalues_getkeyvalue.htm
tech.root: wpd_dk
ms.assetid: 00d0f564-05ab-4f87-8477-efedc172e296
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: GetKeyValue, GetKeyValue method, GetKeyValue method,IPortableDeviceValues interface, IPortableDeviceValues interface,GetKeyValue method, IPortableDeviceValues.GetKeyValue, IPortableDeviceValues::GetKeyValue, IPortableDeviceValuesGetKeyValue, portabledevicetypes/IPortableDeviceValues::GetKeyValue, wpddk.iportabledevicevalues_getkeyvalue
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: portabledevicetypes.h
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
-	PortableDeviceTypes.h
api_name:
-	IPortableDeviceValues.GetKeyValue
product: Windows
targetos: Windows
req.typenames: 
---

# IPortableDeviceValues::GetKeyValue


## -description



Retrieves a <b>PROPERTYKEY</b> value (type VT_UNKNOWN) that is specified by a key.




## -parameters




### -param key [in]

A <b>REFPROPERTYKEY</b> key that specifies the item to retrieve.


### -param pValue [out]

Pointer to the retrieved <b>PROPERTYKEY</b> value.


## -returns



The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>DISP_E_TYPEMISMATCH</b></dt>
</dl>
</td>
<td width="60%">
The property specified by <i>key</i> is not a <b>PROPERTYKEY</b> type.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>HRESULT_FROM_WIN32(ERROR_NOT_FOUND)</b></dt>
</dl>
</td>
<td width="60%">
The property specified by <i>key</i> is not in the collection.

</td>
</tr>
</table>
 




## -remarks



None.




## -see-also




<a href="https://msdn.microsoft.com/4a97301a-12cc-442f-a080-446ec9e1e245">IPortableDeviceValues Interface</a>



<a href="https://msdn.microsoft.com/4c8ccaa6-a99e-42b5-9044-fe11d17e9aa7">IPortableDeviceValues::SetKeyValue</a>
 

 

