---
external help file: Microsoft.Azure.Commands.IotHub.dll-Help.xml
Module Name: AzureRM.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.iothub/set-azurermiothub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Set-AzureRmIotHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Set-AzureRmIotHub.md
ms.openlocfilehash: a9005819bb78e5393f3a617dd18886309d3defc1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93626451"
---
# <span data-ttu-id="4b600-101">Set-AzureRmIotHub</span><span class="sxs-lookup"><span data-stu-id="4b600-101">Set-AzureRmIotHub</span></span>

## <span data-ttu-id="4b600-102">摘要</span><span class="sxs-lookup"><span data-stu-id="4b600-102">SYNOPSIS</span></span>
<span data-ttu-id="4b600-103">更新 IotHub 的屬性。</span><span class="sxs-lookup"><span data-stu-id="4b600-103">Updates the properties of an IotHub.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4b600-104">句法</span><span class="sxs-lookup"><span data-stu-id="4b600-104">SYNTAX</span></span>

### <span data-ttu-id="4b600-105">UpdateSku (預設) </span><span class="sxs-lookup"><span data-stu-id="4b600-105">UpdateSku (Default)</span></span>
```
Set-AzureRmIotHub -ResourceGroupName <String> -Name <String> -SkuName <PSIotHubSku> [-Units <Int64>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4b600-106">UpdateEventHubEndpointProperties</span><span class="sxs-lookup"><span data-stu-id="4b600-106">UpdateEventHubEndpointProperties</span></span>
```
Set-AzureRmIotHub -ResourceGroupName <String> -Name <String> -EventHubRetentionTimeInDays <Int64>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4b600-107">UpdateFileUploadProperties</span><span class="sxs-lookup"><span data-stu-id="4b600-107">UpdateFileUploadProperties</span></span>
```
Set-AzureRmIotHub -ResourceGroupName <String> -Name <String> [-FileUploadStorageConnectionString <String>]
 [-FileUploadContainerName <String>] [-FileUploadSasUriTtl <TimeSpan>] [-FileUploadNotificationTtl <TimeSpan>]
 [-FileUploadNotificationMaxDeliveryCount <Int32>] -EnableFileUploadNotifications <Boolean>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4b600-108">UpdateCloudToDeviceProperties</span><span class="sxs-lookup"><span data-stu-id="4b600-108">UpdateCloudToDeviceProperties</span></span>
```
Set-AzureRmIotHub -ResourceGroupName <String> -Name <String> -CloudToDevice <PSCloudToDeviceProperties>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4b600-109">UpdateOperationsMonitoringProperties</span><span class="sxs-lookup"><span data-stu-id="4b600-109">UpdateOperationsMonitoringProperties</span></span>
```
Set-AzureRmIotHub -ResourceGroupName <String> -Name <String>
 -OperationsMonitoringProperties <PSOperationsMonitoringProperties> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4b600-110">UpdateRoutingProperties</span><span class="sxs-lookup"><span data-stu-id="4b600-110">UpdateRoutingProperties</span></span>
```
Set-AzureRmIotHub -ResourceGroupName <String> -Name <String> [-RoutingProperties <PSRoutingProperties>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4b600-111">UpdateRouteProperties</span><span class="sxs-lookup"><span data-stu-id="4b600-111">UpdateRouteProperties</span></span>
```
Set-AzureRmIotHub -ResourceGroupName <String> -Name <String>
 [-Routes <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Management.IotHub.Models.PSRouteMetadata]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4b600-112">UpdateFallbackRouteProperty</span><span class="sxs-lookup"><span data-stu-id="4b600-112">UpdateFallbackRouteProperty</span></span>
```
Set-AzureRmIotHub -ResourceGroupName <String> -Name <String> [-FallbackRoute <PSFallbackRouteMetadata>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4b600-113">說明</span><span class="sxs-lookup"><span data-stu-id="4b600-113">DESCRIPTION</span></span>
<span data-ttu-id="4b600-114">更新 IotHub 的屬性。</span><span class="sxs-lookup"><span data-stu-id="4b600-114">Updates the properties of an IotHub.</span></span>

## <span data-ttu-id="4b600-115">示例</span><span class="sxs-lookup"><span data-stu-id="4b600-115">EXAMPLES</span></span>

### <span data-ttu-id="4b600-116">範例1更新 sku</span><span class="sxs-lookup"><span data-stu-id="4b600-116">Example 1 Update the sku</span></span>
```
PS C:\> Set-AzureRmIotHub -ResourceGroupName "myresourcegroup" -Name "myiothub" -SkuName S1 -Units 5
```

<span data-ttu-id="4b600-117">針對名稱為 "myiothub" 的 IotHub，將 sku 更新為 S1，並將單位更新為5</span><span class="sxs-lookup"><span data-stu-id="4b600-117">Update the sku to S1 and units to 5 for the IotHub named "myiothub"</span></span>

### <span data-ttu-id="4b600-118">範例2更新 eventhub 屬性</span><span class="sxs-lookup"><span data-stu-id="4b600-118">Example 2 Update the eventhub properties</span></span>
```
PS C:\> Set-AzureRmIotHub -ResourceGroupName "myresourcegroup" -Name "myiothub" -EventHubRetentionTimeInDays 4
```

<span data-ttu-id="4b600-119">針對名稱為 "myiothub" 的 IotHub，將 [遙測] 和 [operationsmonitoringevents] 事件的保留時間更新為4天</span><span class="sxs-lookup"><span data-stu-id="4b600-119">Update the retention time in days to 4 for both the telemetry and operationsmonitoringevents events for the IotHub named "myiothub"</span></span>

## <span data-ttu-id="4b600-120">參數</span><span class="sxs-lookup"><span data-stu-id="4b600-120">PARAMETERS</span></span>

### <span data-ttu-id="4b600-121">-CloudToDevice</span><span class="sxs-lookup"><span data-stu-id="4b600-121">-CloudToDevice</span></span>
<span data-ttu-id="4b600-122">雲端 to device 命令佇列的屬性。</span><span class="sxs-lookup"><span data-stu-id="4b600-122">The properties for the cloud to device command queue.</span></span> 

```yaml
Type: PSCloudToDeviceProperties
Parameter Sets: UpdateCloudToDeviceProperties
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4b600-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4b600-123">-DefaultProfile</span></span>
<span data-ttu-id="4b600-124">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="4b600-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4b600-125">-EnableFileUploadNotifications</span><span class="sxs-lookup"><span data-stu-id="4b600-125">-EnableFileUploadNotifications</span></span>
<span data-ttu-id="4b600-126">此標誌指定是否應針對檔案上傳啟用通知。</span><span class="sxs-lookup"><span data-stu-id="4b600-126">Flag that specifies whether notifications should be enabled for file upload.</span></span> 

```yaml
Type: Boolean
Parameter Sets: UpdateFileUploadProperties
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4b600-127">-EventHubRetentionTimeInDays</span><span class="sxs-lookup"><span data-stu-id="4b600-127">-EventHubRetentionTimeInDays</span></span>
<span data-ttu-id="4b600-128">保留時間（天）。</span><span class="sxs-lookup"><span data-stu-id="4b600-128">Retention time in days.</span></span> 

```yaml
Type: Int64
Parameter Sets: UpdateEventHubEndpointProperties
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4b600-129">-FallbackRoute</span><span class="sxs-lookup"><span data-stu-id="4b600-129">-FallbackRoute</span></span>
<span data-ttu-id="4b600-130">路由的備用路線</span><span class="sxs-lookup"><span data-stu-id="4b600-130">Fallback Route for Routing</span></span>

```yaml
Type: PSFallbackRouteMetadata
Parameter Sets: UpdateFallbackRouteProperty
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4b600-131">-FileUploadContainerName</span><span class="sxs-lookup"><span data-stu-id="4b600-131">-FileUploadContainerName</span></span>
<span data-ttu-id="4b600-132">要上傳檔案的容器名稱。</span><span class="sxs-lookup"><span data-stu-id="4b600-132">The name of the container to upload the files to.</span></span>

```yaml
Type: String
Parameter Sets: UpdateFileUploadProperties
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4b600-133">-FileUploadNotificationMaxDeliveryCount</span><span class="sxs-lookup"><span data-stu-id="4b600-133">-FileUploadNotificationMaxDeliveryCount</span></span>
<span data-ttu-id="4b600-134">檔案上傳通知的最大傳遞數。</span><span class="sxs-lookup"><span data-stu-id="4b600-134">The maximum delivery count for file upload notifications.</span></span>  

```yaml
Type: Int32
Parameter Sets: UpdateFileUploadProperties
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4b600-135">-FileUploadNotificationTtl</span><span class="sxs-lookup"><span data-stu-id="4b600-135">-FileUploadNotificationTtl</span></span>
<span data-ttu-id="4b600-136">檔案上傳通知佇列中郵件的存留時間值。</span><span class="sxs-lookup"><span data-stu-id="4b600-136">Time to live value for the messages in the file upload notification queue.</span></span> 

```yaml
Type: TimeSpan
Parameter Sets: UpdateFileUploadProperties
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4b600-137">-FileUploadSasUriTtl</span><span class="sxs-lookup"><span data-stu-id="4b600-137">-FileUploadSasUriTtl</span></span>
<span data-ttu-id="4b600-138">針對檔案上傳所產生的 SAS Uri 的存留時間。</span><span class="sxs-lookup"><span data-stu-id="4b600-138">Time to live for the for the SAS Uri thats generated for file upload.</span></span> 

```yaml
Type: TimeSpan
Parameter Sets: UpdateFileUploadProperties
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4b600-139">-FileUploadStorageConnectionString</span><span class="sxs-lookup"><span data-stu-id="4b600-139">-FileUploadStorageConnectionString</span></span>
<span data-ttu-id="4b600-140">要上傳檔案的儲存空間連接字串。</span><span class="sxs-lookup"><span data-stu-id="4b600-140">The storage connection string to upload the files to.</span></span> 

```yaml
Type: String
Parameter Sets: UpdateFileUploadProperties
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4b600-141">-名稱</span><span class="sxs-lookup"><span data-stu-id="4b600-141">-Name</span></span>
<span data-ttu-id="4b600-142">IotHub 的名稱</span><span class="sxs-lookup"><span data-stu-id="4b600-142">Name of the IotHub</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4b600-143">-OperationsMonitoringProperties</span><span class="sxs-lookup"><span data-stu-id="4b600-143">-OperationsMonitoringProperties</span></span>
<span data-ttu-id="4b600-144">與作業監視相關的屬性。</span><span class="sxs-lookup"><span data-stu-id="4b600-144">The properties related to operations monitoring.</span></span> 

```yaml
Type: PSOperationsMonitoringProperties
Parameter Sets: UpdateOperationsMonitoringProperties
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4b600-145">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4b600-145">-ResourceGroupName</span></span>
<span data-ttu-id="4b600-146">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="4b600-146">Resource Group Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4b600-147">-路線</span><span class="sxs-lookup"><span data-stu-id="4b600-147">-Routes</span></span>
<span data-ttu-id="4b600-148">要新增以進行路由的路由</span><span class="sxs-lookup"><span data-stu-id="4b600-148">Routes to be added for Routing</span></span>

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

### <span data-ttu-id="4b600-149">-RoutingProperties</span><span class="sxs-lookup"><span data-stu-id="4b600-149">-RoutingProperties</span></span>
<span data-ttu-id="4b600-150">將訊息路由至外部端點的路由屬性</span><span class="sxs-lookup"><span data-stu-id="4b600-150">The Routing properties for routing messages to external endpoints</span></span> 

```yaml
Type: PSRoutingProperties
Parameter Sets: UpdateRoutingProperties
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4b600-151">-SkuName</span><span class="sxs-lookup"><span data-stu-id="4b600-151">-SkuName</span></span>
<span data-ttu-id="4b600-152">Sku 的名稱。</span><span class="sxs-lookup"><span data-stu-id="4b600-152">Name of the Sku.</span></span>

```yaml
Type: PSIotHubSku
Parameter Sets: UpdateSku
Aliases: 
Accepted values: F1, S1, S2, S3

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4b600-153">單位</span><span class="sxs-lookup"><span data-stu-id="4b600-153">-Units</span></span>
<span data-ttu-id="4b600-154">單位數量</span><span class="sxs-lookup"><span data-stu-id="4b600-154">Number of Units</span></span>

```yaml
Type: Int64
Parameter Sets: UpdateSku
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4b600-155">-確認</span><span class="sxs-lookup"><span data-stu-id="4b600-155">-Confirm</span></span>
<span data-ttu-id="4b600-156">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="4b600-156">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4b600-157">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4b600-157">-WhatIf</span></span>
<span data-ttu-id="4b600-158">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="4b600-158">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4b600-159">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="4b600-159">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4b600-160">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4b600-160">CommonParameters</span></span>
<span data-ttu-id="4b600-161">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="4b600-161">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4b600-162">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="4b600-162">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4b600-163">輸入</span><span class="sxs-lookup"><span data-stu-id="4b600-163">INPUTS</span></span>

### <span data-ttu-id="4b600-164">System.object</span><span class="sxs-lookup"><span data-stu-id="4b600-164">System.String</span></span>
<span data-ttu-id="4b600-165">IotHub PSCloudToDeviceProperties IotHub....... PSOperationsMonitoringProperties</span><span class="sxs-lookup"><span data-stu-id="4b600-165">Microsoft.Azure.Commands.Management.IotHub.Models.PSCloudToDeviceProperties Microsoft.Azure.Commands.Management.IotHub.Models.PSOperationsMonitoringProperties</span></span>

## <span data-ttu-id="4b600-166">輸出</span><span class="sxs-lookup"><span data-stu-id="4b600-166">OUTPUTS</span></span>

### <span data-ttu-id="4b600-167">PSIotHub （IotHub.）。</span><span class="sxs-lookup"><span data-stu-id="4b600-167">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

## <span data-ttu-id="4b600-168">筆記</span><span class="sxs-lookup"><span data-stu-id="4b600-168">NOTES</span></span>

## <span data-ttu-id="4b600-169">相關連結</span><span class="sxs-lookup"><span data-stu-id="4b600-169">RELATED LINKS</span></span>

