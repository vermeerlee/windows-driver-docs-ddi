---
UID: NS:pointofservicedriverinterface._PosStatisticsHeader
title: _PosStatisticsHeader (pointofservicedriverinterface.h)
description: This structure defines Unified Point of Service (UPOS) standard information about a device. This structure is the header for an incoming statistic.
old-location: pos\posstatisticsheader.htm
tech.root: pos
ms.assetid: 75567f14-07fe-4861-9f78-e4de6d0bb023
ms.date: 02/23/2018
keywords: ["PosStatisticsHeader structure"]
ms.keywords: PosStatisticsHeader, PosStatisticsHeader structure, _PosStatisticsHeader, pointofservicedriverinterface/PosStatisticsHeader, pos.posstatisticsheader
req.header: pointofservicedriverinterface.h
req.include-header: PointOfServiceDriverInterface.h
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
targetos: Windows
req.typenames: PosStatisticsHeader
f1_keywords:
 - _PosStatisticsHeader
 - pointofservicedriverinterface/_PosStatisticsHeader
 - PosStatisticsHeader
 - pointofservicedriverinterface/PosStatisticsHeader
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - PointOfServiceDriverInterface.h
api_name:
 - PosStatisticsHeader
---

# _PosStatisticsHeader structure


## -description

This structure defines Unified Point of Service (UPOS) standard information about a device. This structure is the header for an incoming statistic.

## -struct-fields

### -field EntryCount

Indicates the number of statistics that follow this header.

### -field DeviceInformation

A <a href="/windows-hardware/drivers/ddi/pointofservicecommontypes/ns-pointofservicecommontypes-_posdeviceinformation">PosDeviceInformation</a> structure that contains UPOS standard information about the device, such as its category, manufacturer, and firmware revision.

### -field DataLength

Indicates the length, in bytes, of the **PosStatisticsHeader** and the buffer of <a href="/windows-hardware/drivers/ddi/pointofservicedriverinterface/ns-pointofservicedriverinterface-_posvaluestatisticsentry">PosValueStatisticsEntry</a> that follow this structure in memory.