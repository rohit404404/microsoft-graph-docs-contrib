---
description: "Automatically generated file. DO NOT MODIFY"
---

```php

<?php
use Microsoft\Graph\Beta\GraphServiceClient;
use Microsoft\Graph\Beta\Generated\Drives\Item\Items\Item\Copy\CopyRequestBuilderPostRequestConfiguration;
use Microsoft\Graph\Beta\Generated\Drives\Item\Items\Item\Copy\CopyPostRequestBody;
use Microsoft\Graph\Beta\Generated\Models\ItemReference;


$graphServiceClient = new GraphServiceClient($tokenRequestContext, $scopes);

$requestBody = new CopyPostRequestBody();
$parentReference = new ItemReference();
$parentReference->setDriveId('b!s8RqPCGh0ESQS2EYnKM0IKS3lM7GxjdAviiob7oc5pXv_0LiL-62Qq3IXyrXnEop');
$parentReference->setId('DCD0D3AD-8989-4F23-A5A2-2C086050513F');
$requestBody->setParentReference($parentReference);
$requestBody->setChildrenOnly(true);
$requestConfiguration = new CopyRequestBuilderPostRequestConfiguration();
$queryParameters = CopyRequestBuilderPostRequestConfiguration::createQueryParameters();
$queryParameters->@microsoftgraphconflictBehavior = "replace";
$requestConfiguration->queryParameters = $queryParameters;


$result = $graphServiceClient->drives()->byDriveId('drive-id')->items()->byDriveItemId('driveItem-id')->copy()->post($requestBody, $requestConfiguration)->wait();

```