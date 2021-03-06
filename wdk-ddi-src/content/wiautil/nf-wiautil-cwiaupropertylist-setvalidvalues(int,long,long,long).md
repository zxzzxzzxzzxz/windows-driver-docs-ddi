---
UID: NF:wiautil.CWiauPropertyList.SetValidValues(INT,LONG,LONG,LONG)
title: CWiauPropertyList::SetValidValues(INT,LONG,LONG,LONG)
author: windows-driver-content
description: The CWiauPropertyList::SetValidValues(flag) method sets the type, as well as default, current, and valid values for a property whose values are defined by a flag.
old-location: image\cwiaupropertylist_setvalidvalues_flag_.htm
tech.root: image
ms.assetid: e61b5bbb-14a8-4dfa-af36-99c5dd1ecc99
ms.author: windowsdriverdev
ms.date: 5/3/2018
ms.keywords: CWiauPropertyList interface [Imaging Devices],SetValidValues method, CWiauPropertyList.SetValidValues, CWiauPropertyList.SetValidValues(INT,LONG,LONG,LONG), CWiauPropertyList::SetValidValues, CWiauPropertyList::SetValidValues(INT  ,LONG  ,LONG  ,LONG  ), CWiauPropertyList::SetValidValues(INT,LONG,LONG,LONG), SetValidValues, SetValidValues method [Imaging Devices], SetValidValues method [Imaging Devices],CWiauPropertyList interface, image.cwiaupropertylist_setvalidvalues_flag_, wiauFncs_11c27970-2fa2-480d-9f60-b12202b9b03c.xml, wiautil/CWiauPropertyList::SetValidValues
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: wiautil.h
req.include-header: Wiautil.h, Wiamindr.h
req.target-type: Desktop
req.target-min-winverclnt: Available in Windows XP and later.
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
-	Wiautil.h
api_name:
-	CWiauPropertyList.SetValidValues
product: Windows
targetos: Windows
req.typenames: 
---

# CWiauPropertyList::SetValidValues(INT,LONG,LONG,LONG)


## -description


The <b>CWiauPropertyList::SetValidValues(</b>flag<b>)</b> method sets the type, as well as default, current, and valid values for a property whose values are defined by a flag. The method also sets the property type to VT_I4 and subtype to WIA_PROP_FLAG (defined in the Microsoft Windows SDK documentation).


## -parameters




### -param index

Specifies the property index. Set this parameter to the value in *<i>pIdx</i> when the <a href="https://msdn.microsoft.com/library/windows/hardware/ff540391">CWiauPropertyList::DefineProperty</a> method returns.


### -param defaultValue

Specifies the default setting of the property on the device.


### -param currentValue

Specifies the current setting of the property on the device.


### -param validFlags

Specifies a value containing all of the valid flags.


## -returns



This method does not return a value.




## -see-also




<a href="https://msdn.microsoft.com/4f11bec0-8ff4-4fa0-824c-71ce9774d5d1">CWiauPropertyList</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff540391">CWiauPropertyList::DefineProperty</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff540403">CWiauPropertyList::SendToWia</a>
 

 

