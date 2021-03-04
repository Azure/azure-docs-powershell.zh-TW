---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/powershell/module/az.iothub/set-aziothub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHub.md
ms.openlocfilehash: 5be94896aeb4217e3c2f9da700e0f59032473296
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101911954"
---
# <span data-ttu-id="dd369-101">Set-AzIotHub</span><span class="sxs-lookup"><span data-stu-id="dd369-101">Set-AzIotHub</span></span>

## <span data-ttu-id="dd369-102">簡介</span><span class="sxs-lookup"><span data-stu-id="dd369-102">SYNOPSIS</span></span>
<span data-ttu-id="dd369-103">更新 IotHub 的屬性。</span><span class="sxs-lookup"><span data-stu-id="dd369-103">Updates the properties of an IotHub.</span></span>

## <span data-ttu-id="dd369-104">語法</span><span class="sxs-lookup"><span data-stu-id="dd369-104">SYNTAX</span></span>

### <span data-ttu-id="dd369-105">UpdateSKU (預設) </span><span class="sxs-lookup"><span data-stu-id="dd369-105">UpdateSku (Default)</span></span>
```
Set-AzIotHub -ResourceGroupName <String> -Name <String> -SkuName <PSIotHubSku> [-Units <Int64>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dd369-106">UpdateEventHubEndpointProperties</span><span class="sxs-lookup"><span data-stu-id="dd369-106">UpdateEventHubEndpointProperties</span></span>
```
Set-AzIotHub -ResourceGroupName <String> -Name <String> -EventHubRetentionTimeInDays <Int64>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dd369-107">UpdateFileUploadProperties</span><span class="sxs-lookup"><span data-stu-id="dd369-107">UpdateFileUploadProperties</span></span>
```
Set-AzIotHub -ResourceGroupName <String> -Name <String> [-FileUploadStorageConnectionString <String>]
 [-FileUploadContainerName <String>] [-FileUploadSasUriTtl <TimeSpan>] [-FileUploadNotificationTtl <TimeSpan>]
 [-FileUploadNotificationMaxDeliveryCount <Int32>] -EnableFileUploadNotifications <Boolean>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dd369-108">UpdateCloudToDeviceProperties</span><span class="sxs-lookup"><span data-stu-id="dd369-108">UpdateCloudToDeviceProperties</span></span>
```
Set-AzIotHub -ResourceGroupName <String> -Name <String> -CloudToDevice <PSCloudToDeviceProperties>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dd369-109">UpdateRoutingProperties</span><span class="sxs-lookup"><span data-stu-id="dd369-109">UpdateRoutingProperties</span></span>
```
Set-AzIotHub -ResourceGroupName <String> -Name <String> [-RoutingProperties <PSRoutingProperties>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dd369-110">UpdateRouteProperties</span><span class="sxs-lookup"><span data-stu-id="dd369-110">UpdateRouteProperties</span></span>
```
Set-AzIotHub -ResourceGroupName <String> -Name <String>
 [-Routes <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Management.IotHub.Models.PSRouteMetadata]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dd369-111">UpdateFallbackRouteProperty</span><span class="sxs-lookup"><span data-stu-id="dd369-111">UpdateFallbackRouteProperty</span></span>
```
Set-AzIotHub -ResourceGroupName <String> -Name <String> [-FallbackRoute <PSFallbackRouteMetadata>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dd369-112">描述</span><span class="sxs-lookup"><span data-stu-id="dd369-112">DESCRIPTION</span></span>
<span data-ttu-id="dd369-113">更新 IotHub 的屬性。</span><span class="sxs-lookup"><span data-stu-id="dd369-113">Updates the properties of an IotHub.</span></span>

## <span data-ttu-id="dd369-114">例子</span><span class="sxs-lookup"><span data-stu-id="dd369-114">EXAMPLES</span></span>

### <span data-ttu-id="dd369-115">範例 1 更新 SKU</span><span class="sxs-lookup"><span data-stu-id="dd369-115">Example 1 Update the sku</span></span>
```
PS C:\> Set-AzIotHub -ResourceGroupName "myresourcegroup" -Name "myiothub" -SkuName S1 -Units 5
```

<span data-ttu-id="dd369-116">針對名為"myiothub" 的 IotHub，將 SKU 更新為 S1 且單位為 5</span><span class="sxs-lookup"><span data-stu-id="dd369-116">Update the sku to S1 and units to 5 for the IotHub named "myiothub"</span></span>

### <span data-ttu-id="dd369-117">範例 2 更新 eventhub 屬性</span><span class="sxs-lookup"><span data-stu-id="dd369-117">Example 2 Update the eventhub properties</span></span>
```
PS C:\> Set-AzIotHub -ResourceGroupName "myresourcegroup" -Name "myiothub" -EventHubRetentionTimeInDays 4
```

<span data-ttu-id="dd369-118">將名為"myiothub" 的 IotHub 遙測保留時間以天數更新為 4</span><span class="sxs-lookup"><span data-stu-id="dd369-118">Update the retention time of telemetry in days to 4 for the IotHub named "myiothub"</span></span>

## <span data-ttu-id="dd369-119">參數</span><span class="sxs-lookup"><span data-stu-id="dd369-119">PARAMETERS</span></span>

### <span data-ttu-id="dd369-120">-CloudToDevice</span><span class="sxs-lookup"><span data-stu-id="dd369-120">-CloudToDevice</span></span>
<span data-ttu-id="dd369-121">雲端到裝置命令佇列的屬性。</span><span class="sxs-lookup"><span data-stu-id="dd369-121">The properties for the cloud to device command queue.</span></span> 

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSCloudToDeviceProperties
Parameter Sets: UpdateCloudToDeviceProperties
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd369-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dd369-122">-DefaultProfile</span></span>
<span data-ttu-id="dd369-123">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="dd369-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd369-124">-EnableFileUploadNotifications</span><span class="sxs-lookup"><span data-stu-id="dd369-124">-EnableFileUploadNotifications</span></span>
<span data-ttu-id="dd369-125">指定是否應該啟用檔案上傳通知的標號。</span><span class="sxs-lookup"><span data-stu-id="dd369-125">Flag that specifies whether notifications should be enabled for file upload.</span></span> 

```yaml
Type: System.Boolean
Parameter Sets: UpdateFileUploadProperties
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd369-126">-EventHubRetentionTimeInDays</span><span class="sxs-lookup"><span data-stu-id="dd369-126">-EventHubRetentionTimeInDays</span></span>
<span data-ttu-id="dd369-127">保留時間 ，以天數表示。</span><span class="sxs-lookup"><span data-stu-id="dd369-127">Retention time in days.</span></span> 

```yaml
Type: System.Int64
Parameter Sets: UpdateEventHubEndpointProperties
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd369-128">-FallbackRoute</span><span class="sxs-lookup"><span data-stu-id="dd369-128">-FallbackRoute</span></span>
<span data-ttu-id="dd369-129">路由的後背路由</span><span class="sxs-lookup"><span data-stu-id="dd369-129">Fallback Route for Routing</span></span>

```yaml
Type: Microsoft.Azure.Management.IotHub.Models.PSFallbackRouteMetadata
Parameter Sets: UpdateFallbackRouteProperty
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd369-130">-FileUploadContainerName</span><span class="sxs-lookup"><span data-stu-id="dd369-130">-FileUploadContainerName</span></span>
<span data-ttu-id="dd369-131">要上傳檔案的容器名稱。</span><span class="sxs-lookup"><span data-stu-id="dd369-131">The name of the container to upload the files to.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateFileUploadProperties
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd369-132">-FileUploadNotificationMaxDeliveryCount</span><span class="sxs-lookup"><span data-stu-id="dd369-132">-FileUploadNotificationMaxDeliveryCount</span></span>
<span data-ttu-id="dd369-133">檔案上傳通知的最大傳遞計數。</span><span class="sxs-lookup"><span data-stu-id="dd369-133">The maximum delivery count for file upload notifications.</span></span>  

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: UpdateFileUploadProperties
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd369-134">-FileUploadNotificationTtl</span><span class="sxs-lookup"><span data-stu-id="dd369-134">-FileUploadNotificationTtl</span></span>
<span data-ttu-id="dd369-135">檔案上傳通知佇列中郵件的即時值時間。</span><span class="sxs-lookup"><span data-stu-id="dd369-135">Time to live value for the messages in the file upload notification queue.</span></span> 

```yaml
Type: System.TimeSpan
Parameter Sets: UpdateFileUploadProperties
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd369-136">-FileUploadSasUriTtl</span><span class="sxs-lookup"><span data-stu-id="dd369-136">-FileUploadSasUriTtl</span></span>
<span data-ttu-id="dd369-137">上傳檔案時產生的 SAS Uri 使用時間。</span><span class="sxs-lookup"><span data-stu-id="dd369-137">Time to live for the for the SAS Uri thats generated for file upload.</span></span> 

```yaml
Type: System.TimeSpan
Parameter Sets: UpdateFileUploadProperties
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd369-138">-FileUploadStorageConnectionString</span><span class="sxs-lookup"><span data-stu-id="dd369-138">-FileUploadStorageConnectionString</span></span>
<span data-ttu-id="dd369-139">要上傳檔案的儲存空間連接字串。</span><span class="sxs-lookup"><span data-stu-id="dd369-139">The storage connection string to upload the files to.</span></span> 

```yaml
Type: System.String
Parameter Sets: UpdateFileUploadProperties
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd369-140">-名稱</span><span class="sxs-lookup"><span data-stu-id="dd369-140">-Name</span></span>
<span data-ttu-id="dd369-141">IotHub 的名稱</span><span class="sxs-lookup"><span data-stu-id="dd369-141">Name of the IotHub</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dd369-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dd369-142">-ResourceGroupName</span></span>
<span data-ttu-id="dd369-143">資源組名</span><span class="sxs-lookup"><span data-stu-id="dd369-143">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dd369-144">-路由</span><span class="sxs-lookup"><span data-stu-id="dd369-144">-Routes</span></span>
<span data-ttu-id="dd369-145">要新增路由進行路由</span><span class="sxs-lookup"><span data-stu-id="dd369-145">Routes to be added for Routing</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Management.IotHub.Models.PSRouteMetadata]
Parameter Sets: UpdateRouteProperties
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd369-146">-RoutingProperties</span><span class="sxs-lookup"><span data-stu-id="dd369-146">-RoutingProperties</span></span>
<span data-ttu-id="dd369-147">將郵件路由至外部端點的路由屬性</span><span class="sxs-lookup"><span data-stu-id="dd369-147">The Routing properties for routing messages to external endpoints</span></span> 

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingProperties
Parameter Sets: UpdateRoutingProperties
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd369-148">-SKUName</span><span class="sxs-lookup"><span data-stu-id="dd369-148">-SkuName</span></span>
<span data-ttu-id="dd369-149">SKU 的名稱。</span><span class="sxs-lookup"><span data-stu-id="dd369-149">Name of the Sku.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubSku
Parameter Sets: UpdateSku
Aliases:
Accepted values: F1, S1, S2, S3, B1, B2, B3

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd369-150">-單位</span><span class="sxs-lookup"><span data-stu-id="dd369-150">-Units</span></span>
<span data-ttu-id="dd369-151">單位數</span><span class="sxs-lookup"><span data-stu-id="dd369-151">Number of Units</span></span>

```yaml
Type: System.Int64
Parameter Sets: UpdateSku
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd369-152">-確認</span><span class="sxs-lookup"><span data-stu-id="dd369-152">-Confirm</span></span>
<span data-ttu-id="dd369-153">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="dd369-153">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd369-154">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dd369-154">-WhatIf</span></span>
<span data-ttu-id="dd369-155">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="dd369-155">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dd369-156">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="dd369-156">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd369-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dd369-157">CommonParameters</span></span>
<span data-ttu-id="dd369-158">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="dd369-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dd369-159">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="dd369-159">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dd369-160">輸入</span><span class="sxs-lookup"><span data-stu-id="dd369-160">INPUTS</span></span>

### <span data-ttu-id="dd369-161">System.String</span><span class="sxs-lookup"><span data-stu-id="dd369-161">System.String</span></span>

## <span data-ttu-id="dd369-162">輸出</span><span class="sxs-lookup"><span data-stu-id="dd369-162">OUTPUTS</span></span>

### <span data-ttu-id="dd369-163">Microsoft.Azure.Commands.management.IotHub.models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="dd369-163">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

## <span data-ttu-id="dd369-164">筆記</span><span class="sxs-lookup"><span data-stu-id="dd369-164">NOTES</span></span>

## <span data-ttu-id="dd369-165">相關連結</span><span class="sxs-lookup"><span data-stu-id="dd369-165">RELATED LINKS</span></span>
