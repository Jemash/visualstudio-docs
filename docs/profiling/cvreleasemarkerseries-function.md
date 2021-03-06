---
title: "CvReleaseMarkerSeries Function | Microsoft Docs"
ms.custom: ""
ms.date: "11/04/2016"
ms.technology: "vs-ide-debug"
ms.topic: "conceptual"
f1_keywords: 
  - "cvmarkers/CvReleaseMarkerSeries"
helpviewer_keywords: 
  - "CvReleaseMarkerSeries method"
ms.assetid: 3b4711ee-e534-411d-9128-f69cd7932a48
author: "mikejo5000"
ms.author: "mikejo"
manager: douge
ms.workload: 
  - "multiple"
---
# CvReleaseMarkerSeries Function
Releases marker series. Do not use marker series object after releasing otherwise the application might crash. Failure to release marker series causes a memory leak.  
  
## Syntax  
  
```  
HRESULT CvReleaseMarkerSeries(  
   _In_reads_bytes_(16) PCV_MARKERSERIES pMarkerSeries  
);  
```  
  
#### Parameters  
 `pMarkerSeries`  
 Address of provider object variable. Address cannot be NULL, the variable can have any value.  
  
## Return Value  
 S_OK when marker series is successfully released or error code in case there were any errors. Use SUCCEEDED/FAILED macros to check for error condition.  
  
## Requirements  
 **Header:** cvmarkers.h  
  
## See Also  
 [C++ Library Reference](../profiling/cpp-library-reference.md)