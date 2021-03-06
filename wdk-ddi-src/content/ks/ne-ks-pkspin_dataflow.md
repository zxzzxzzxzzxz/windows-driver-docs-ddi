---
UID: NE:ks.PKSPIN_DATAFLOW
title: "*PKSPIN_DATAFLOW"
author: windows-driver-content
description: An instance of the KSPIN_DATAFLOW enumeration is returned by KSPROPERTY_PIN_DATAFLOW.
old-location: stream\kspin_dataflow.htm
tech.root: stream
ms.assetid: feab830d-8079-4051-8974-52905f845765
ms.author: windowsdriverdev
ms.date: 2/23/2018
ms.keywords: "*PKSPIN_DATAFLOW, KSPIN_DATAFLOW, KSPIN_DATAFLOW enumeration [Streaming Media Devices], KSPIN_DATAFLOW_IN, KSPIN_DATAFLOW_OUT, PKSPIN_DATAFLOW, PKSPIN_DATAFLOW enumeration pointer [Streaming Media Devices], ks-struct_2161b89b-ba7c-440a-9006-c3445b392b89.xml, ks/KSPIN_DATAFLOW, ks/KSPIN_DATAFLOW_IN, ks/KSPIN_DATAFLOW_OUT, ks/PKSPIN_DATAFLOW, stream.kspin_dataflow"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
req.header: ks.h
req.include-header: Ks.h
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
-	HeaderDef
api_location:
-	ks.h
api_name:
-	KSPIN_DATAFLOW
product:
- Windows
targetos: Windows
req.typenames: KSPIN_DATAFLOW, *PKSPIN_DATAFLOW
---

# *PKSPIN_DATAFLOW enumeration


## -description


An instance of the KSPIN_DATAFLOW enumeration is returned by <a href="https://msdn.microsoft.com/library/windows/hardware/ff565197">KSPROPERTY_PIN_DATAFLOW</a>.


## -syntax


````
typedef enum  {
  KSPIN_DATAFLOW_IN   = 1,
  KSPIN_DATAFLOW_OUT  = 2
} KSPIN_DATAFLOW, *PKSPIN_DATAFLOW;
````


## -enum-fields




### -field KSPIN_DATAFLOW_IN

Indicates that the pin factory instantiates data sink pins. Such pins can only be connected to data source pins.


### -field KSPIN_DATAFLOW_OUT

Indicates that the pin factory instantiates data source pins. Such pins can only be connected to data sink pins.


## -see-also

<a href="..\ks\ns-ks-kspin_descriptor.md">KSPIN_DESCRIPTOR</a>



<a href="..\ks\ns-ks-_kspin.md">KSPIN</a>



<a href="..\strmini\ns-strmini-_hw_stream_information.md">HW_STREAM_INFORMATION</a>



 

 


