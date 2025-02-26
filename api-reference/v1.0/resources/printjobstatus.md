---
title: printJobStatus resource type
description: Represents the current status of a print job.
author: nilakhan
ms.localizationpriority: medium
ms.subservice: universal-print
doc_type: resourcePageType
ms.date: 08/08/2024
---

# printJobStatus resource type

Namespace: microsoft.graph

Represents the current status of a print job.

## Properties
|Property|Type|Description|
|:---|:---|:---|
|description|String|A human-readable description of the print job's current processing state. Read-only.|
|details|printJobProcessingDetail collection|Additional details for print job state. Valid values are described in the following table. Read-only.|
|isAcquiredByPrinter|Boolean|True if the job was acknowledged by a printer; false otherwise. Read-only.|
|state|printJobProcessingState|The print job's current processing state. Valid values are described in the following table. Read-only.|

### printJobProcessingState values

|Member|Value|Description|
|:---|:---|:---|
|unknown|0|The processing state reported by the printer isn't recognized.|
|pending|1|The print job is pending processing by the printer.|
|processing|2|The print job is currently being processed by the printer.|
|paused|3|The print job has been paused.|
|stopped|4|The print job has been stopped because an issue with the printer needs to be addressed before the job can continue. More information can be found in the printer state resource.|
|completed|5|The print job has completed successfully and no further processing will take place.|
|canceled|6|The print job has been canceled by a user and no further processing will take place.|
|aborted|7|The print job has been aborted by a user or the printer and no further processing will take place.|

### printJobProcessingDetail values

|Member|Value|Description|
|:---|:---|:---|
|uploadPending|0|Document payload hasn't been uploaded.|
|transforming|1|Document payload is being transformed.|
|completedSuccessfully|2|Job has been completed successfully.|
|completedWithWarnings|3|Job has been completed with warnings.|
|completedWithErrors|4|Job has been completed with errors.|
|releaseWait|5|Job is pending to be released.|
|interpreting|6|Job is in 'processing' state, but more specifically, document payload is being interpreted.|

## Relationships

None.

## JSON representation

The following JSON representation shows the resource type.

<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.printJobStatus"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.printJobStatus",
  "state": "String",
  "description": "String",
  "isAcquiredByPrinter": "Boolean",
  "details": [
    "String"
  ]
}
```

