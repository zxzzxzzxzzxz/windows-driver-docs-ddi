---
UID: NS:d3d10umddi.D3D10DDIARG_TEX1D_SHADERRESOURCEVIEW
title: D3D10DDIARG_TEX1D_SHADERRESOURCEVIEW
author: windows-driver-content
description: The D3D10DDIARG_TEX1D_SHADERRESOURCEVIEW structure describes a one-dimensional (1-D) texture that is used to create a shader resource view in a call to the CreateShaderResourceView function.
old-location: display\d3d10ddiarg_tex1d_shaderresourceview.htm
tech.root: display
ms.assetid: 5cb10ec9-8496-49d1-b8d0-53d8fe7470c5
ms.author: windowsdriverdev
ms.date: 5/10/2018
ms.keywords: D3D10DDIARG_TEX1D_SHADERRESOURCEVIEW, D3D10DDIARG_TEX1D_SHADERRESOURCEVIEW structure [Display Devices], UMDisplayDriver_Dx10param_Structs_804b8de8-55ba-4a68-ba21-ada239882372.xml, d3d10umddi/D3D10DDIARG_TEX1D_SHADERRESOURCEVIEW, display.d3d10ddiarg_tex1d_shaderresourceview
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: d3d10umddi.h
req.include-header: D3d10umddi.h
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
-	d3d10umddi.h
api_name:
-	D3D10DDIARG_TEX1D_SHADERRESOURCEVIEW
product:
- Windows
targetos: Windows
req.typenames: D3D10DDIARG_TEX1D_SHADERRESOURCEVIEW
---

# D3D10DDIARG_TEX1D_SHADERRESOURCEVIEW structure


## -description


The D3D10DDIARG_TEX1D_SHADERRESOURCEVIEW structure describes a one-dimensional (1-D) texture that is used to create a shader resource view in a call to the <a href="https://msdn.microsoft.com/3b1c998d-3fde-4712-ba74-7c8033033182">CreateShaderResourceView</a> function. 


## -struct-fields




### -field MostDetailedMip

[in] The identifier of the most detailed MIP-map. 


### -field FirstArraySlice

[in] The identifier of the first array slice. 


### -field MipLevels

[in] The number of MIP-map levels for the texture. 


### -field ArraySize

[in] The number of array slices for the texture. 


## -remarks



If the <b>MipLevels</b> member is set to -1, the MIP-maps in the texture start from the MIP-map that is set in the <b>MostDetailedMip</b> member. 

If the <b>ArraySize</b> member is set to -1, the array slices in the texture start from the array slice that is set in <b>FirstArraySlice</b> member. 




## -see-also




<a href="https://msdn.microsoft.com/2abf5ca9-974b-40d7-b71c-43c4fb33dd7c">CalcPrivateShaderResourceViewSize</a>



<a href="https://msdn.microsoft.com/3b1c998d-3fde-4712-ba74-7c8033033182">CreateShaderResourceView</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff541708">D3D10DDIARG_CREATESHADERRESOURCEVIEW</a>
 

 

