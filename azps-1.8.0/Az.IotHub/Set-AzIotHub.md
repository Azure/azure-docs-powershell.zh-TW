---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/set-aziothub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHub.md
ms.openlocfilehash: ca7fe171e95d87dd054f0dac27e1a5ccd07396a3
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93787477"
---
# <span data-ttu-id="fe851-101">Set-AzIotHub</span><span class="sxs-lookup"><span data-stu-id="fe851-101">Set-AzIotHub</span></span>

## <span data-ttu-id="fe851-102">摘要</span><span class="sxs-lookup"><span data-stu-id="fe851-102">SYNOPSIS</span></span>
<span data-ttu-id="fe851-103">更新 IotHub 的屬性。</span><span class="sxs-lookup"><span data-stu-id="fe851-103">Updates the properties of an IotHub.</span></span>

## <span data-ttu-id="fe851-104">句法</span><span class="sxs-lookup"><span data-stu-id="fe851-104">SYNTAX</span></span>

### <span data-ttu-id="fe851-105">UpdateSku (預設) </span><span class="sxs-lookup"><span data-stu-id="fe851-105">UpdateSku (Default)</span></span>
```
Set-AzIotHub -ResourceGroupName <String> -Name <String> -SkuName <PSIotHubSku> [-Units <Int64>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fe851-106">UpdateEventHubEndpointProperties</span><span class="sxs-lookup"><span data-stu-id="fe851-106">UpdateEventHubEndpointProperties</span></span>
```
Set-AzIotHub -ResourceGroupName <String> -Name <String> -EventHubRetentionTimeInDays <Int64>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fe851-107">UpdateFileUploadProperties</span><span class="sxs-lookup"><span data-stu-id="fe851-107">UpdateFileUploadProperties</span></span>
```
Set-AzIotHub -ResourceGroupName <String> -Name <String> [-FileUploadStorageConnectionString <String>]
 [-FileUploadContainerName <String>] [-FileUploadSasUriTtl <TimeSpan>] [-FileUploadNotificationTtl <TimeSpan>]
 [-FileUploadNotificationMaxDeliveryCount <Int32>] -EnableFileUploadNotifications <Boolean>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fe851-108">UpdateCloudToDeviceProperties</span><span class="sxs-lookup"><span data-stu-id="fe851-108">UpdateCloudToDeviceProperties</span></span>
```
Set-AzIotHub -ResourceGroupName <String> -Name <String> -CloudToDevice <PSCloudToDeviceProperties>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fe851-109">UpdateOperationsMonitoringProperties</span><span class="sxs-lookup"><span data-stu-id="fe851-109">UpdateOperationsMonitoringProperties</span></span>
```
Set-AzIotHub -ResourceGroupName <String> -Name <String>
 -OperationsMonitoringProperties <PSOperationsMonitoringProperties> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fe851-110">UpdateRoutingProperties</span><span class="sxs-lookup"><span data-stu-id="fe851-110">UpdateRoutingProperties</span></span>
```
Set-AzIotHub -ResourceGroupName <String> -Name <String> [-RoutingProperties <PSRoutingProperties>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fe851-111">UpdateRouteProperties</span><span class="sxs-lookup"><span data-stu-id="fe851-111">UpdateRouteProperties</span></span>
```
Set-AzIotHub -ResourceGroupName <String> -Name <String>
 [-Routes <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Management.IotHub.Models.PSRouteMetadata]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fe851-112">UpdateFallbackRouteProperty</span><span class="sxs-lookup"><span data-stu-id="fe851-112">UpdateFallbackRouteProperty</span></span>
```
Set-AzIotHub -ResourceGroupName <String> -Name <String> [-FallbackRoute <PSFallbackRouteMetadata>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fe851-113">說明</span><span class="sxs-lookup"><span data-stu-id="fe851-113">DESCRIPTION</span></span>
<span data-ttu-id="fe851-114">更新 IotHub 的屬性。</span><span class="sxs-lookup"><span data-stu-id="fe851-114">Updates the properties of an IotHub.</span></span>

## <span data-ttu-id="fe851-115">示例</span><span class="sxs-lookup"><span data-stu-id="fe851-115">EXAMPLES</span></span>

### <span data-ttu-id="fe851-116">範例1更新 sku</span><span class="sxs-lookup"><span data-stu-id="fe851-116">Example 1 Update the sku</span></span>
```
PS C:\> Set-AzIotHub -ResourceGroupName "myresourcegroup" -Name "myiothub" -SkuName S1 -Units 5
```

<span data-ttu-id="fe851-117">針對名稱為 "myiothub" 的 IotHub，將 sku 更新為 S1，並將單位更新為5</span><span class="sxs-lookup"><span data-stu-id="fe851-117">Update the sku to S1 and units to 5 for the IotHub named "myiothub"</span></span>

### <span data-ttu-id="fe851-118">範例2更新 eventhub 屬性</span><span class="sxs-lookup"><span data-stu-id="fe851-118">Example 2 Update the eventhub properties</span></span>
```
PS C:\> Set-AzIotHub -ResourceGroupName "myresourcegroup" -Name "myiothub" -EventHubRetentionTimeInDays 4
```

<span data-ttu-id="fe851-119">針對名稱為 "myiothub" 的 IotHub，將 [遙測] 和 [operationsmonitoringevents] 事件的保留時間更新為4天</span><span class="sxs-lookup"><span data-stu-id="fe851-119">Update the retention time in days to 4 for both the telemetry and operationsmonitoringevents events for the IotHub named "myiothub"</span></span>

## <span data-ttu-id="fe851-120">參數</span><span class="sxs-lookup"><span data-stu-id="fe851-120">PARAMETERS</span></span>

### <span data-ttu-id="fe851-121">-CloudToDevice</span><span class="sxs-lookup"><span data-stu-id="fe851-121">-CloudToDevice</span></span>
<span data-ttu-id="fe851-122">雲端 to device 命令佇列的屬性。</span><span class="sxs-lookup"><span data-stu-id="fe851-122">The properties for the cloud to device command queue.</span></span> 

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

### <span data-ttu-id="fe851-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fe851-123">-DefaultProfile</span></span>
<span data-ttu-id="fe851-124">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="fe851-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="fe851-125">-EnableFileUploadNotifications</span><span class="sxs-lookup"><span data-stu-id="fe851-125">-EnableFileUploadNotifications</span></span>
<span data-ttu-id="fe851-126">此標誌指定是否應針對檔案上傳啟用通知。</span><span class="sxs-lookup"><span data-stu-id="fe851-126">Flag that specifies whether notifications should be enabled for file upload.</span></span> 

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

### <span data-ttu-id="fe851-127">-EventHubRetentionTimeInDays</span><span class="sxs-lookup"><span data-stu-id="fe851-127">-EventHubRetentionTimeInDays</span></span>
<span data-ttu-id="fe851-128">保留時間（天）。</span><span class="sxs-lookup"><span data-stu-id="fe851-128">Retention time in days.</span></span> 

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

### <span data-ttu-id="fe851-129">-FallbackRoute</span><span class="sxs-lookup"><span data-stu-id="fe851-129">-FallbackRoute</span></span>
<span data-ttu-id="fe851-130">路由的備用路線</span><span class="sxs-lookup"><span data-stu-id="fe851-130">Fallback Route for Routing</span></span>

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

### <span data-ttu-id="fe851-131">-FileUploadContainerName</span><span class="sxs-lookup"><span data-stu-id="fe851-131">-FileUploadContainerName</span></span>
<span data-ttu-id="fe851-132">要上傳檔案的容器名稱。</span><span class="sxs-lookup"><span data-stu-id="fe851-132">The name of the container to upload the files to.</span></span>

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

### <span data-ttu-id="fe851-133">-FileUploadNotificationMaxDeliveryCount</span><span class="sxs-lookup"><span data-stu-id="fe851-133">-FileUploadNotificationMaxDeliveryCount</span></span>
<span data-ttu-id="fe851-134">檔案上傳通知的最大傳遞數。</span><span class="sxs-lookup"><span data-stu-id="fe851-134">The maximum delivery count for file upload notifications.</span></span>  

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

### <span data-ttu-id="fe851-135">-FileUploadNotificationTtl</span><span class="sxs-lookup"><span data-stu-id="fe851-135">-FileUploadNotificationTtl</span></span>
<span data-ttu-id="fe851-136">檔案上傳通知佇列中郵件的存留時間值。</span><span class="sxs-lookup"><span data-stu-id="fe851-136">Time to live value for the messages in the file upload notification queue.</span></span> 

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

### <span data-ttu-id="fe851-137">-FileUploadSasUriTtl</span><span class="sxs-lookup"><span data-stu-id="fe851-137">-FileUploadSasUriTtl</span></span>
<span data-ttu-id="fe851-138">針對檔案上傳所產生的 SAS Uri 的存留時間。</span><span class="sxs-lookup"><span data-stu-id="fe851-138">Time to live for the for the SAS Uri thats generated for file upload.</span></span> 

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

### <span data-ttu-id="fe851-139">-FileUploadStorageConnectionString</span><span class="sxs-lookup"><span data-stu-id="fe851-139">-FileUploadStorageConnectionString</span></span>
<span data-ttu-id="fe851-140">要上傳檔案的儲存空間連接字串。</span><span class="sxs-lookup"><span data-stu-id="fe851-140">The storage connection string to upload the files to.</span></span> 

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

### <span data-ttu-id="fe851-141">-名稱</span><span class="sxs-lookup"><span data-stu-id="fe851-141">-Name</span></span>
<span data-ttu-id="fe851-142">IotHub 的名稱</span><span class="sxs-lookup"><span data-stu-id="fe851-142">Name of the IotHub</span></span>

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

### <span data-ttu-id="fe851-143">-OperationsMonitoringProperties</span><span class="sxs-lookup"><span data-stu-id="fe851-143">-OperationsMonitoringProperties</span></span>
<span data-ttu-id="fe851-144">與作業監視相關的屬性。</span><span class="sxs-lookup"><span data-stu-id="fe851-144">The properties related to operations monitoring.</span></span> 

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSOperationsMonitoringProperties
Parameter Sets: UpdateOperationsMonitoringProperties
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe851-145">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fe851-145">-ResourceGroupName</span></span>
<span data-ttu-id="fe851-146">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="fe851-146">Resource Group Name</span></span>

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

### <span data-ttu-id="fe851-147">-路線</span><span class="sxs-lookup"><span data-stu-id="fe851-147">-Routes</span></span>
<span data-ttu-id="fe851-148">要新增以進行路由的路由</span><span class="sxs-lookup"><span data-stu-id="fe851-148">Routes to be added for Routing</span></span>

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

### <span data-ttu-id="fe851-149">-RoutingProperties</span><span class="sxs-lookup"><span data-stu-id="fe851-149">-RoutingProperties</span></span>
<span data-ttu-id="fe851-150">將訊息路由至外部端點的路由屬性</span><span class="sxs-lookup"><span data-stu-id="fe851-150">The Routing properties for routing messages to external endpoints</span></span> 

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

### <span data-ttu-id="fe851-151">-SkuName</span><span class="sxs-lookup"><span data-stu-id="fe851-151">-SkuName</span></span>
<span data-ttu-id="fe851-152">Sku 的名稱。</span><span class="sxs-lookup"><span data-stu-id="fe851-152">Name of the Sku.</span></span>

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

### <span data-ttu-id="fe851-153">單位</span><span class="sxs-lookup"><span data-stu-id="fe851-153">-Units</span></span>
<span data-ttu-id="fe851-154">單位數量</span><span class="sxs-lookup"><span data-stu-id="fe851-154">Number of Units</span></span>

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

### <span data-ttu-id="fe851-155">-確認</span><span class="sxs-lookup"><span data-stu-id="fe851-155">-Confirm</span></span>
<span data-ttu-id="fe851-156">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="fe851-156">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fe851-157">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fe851-157">-WhatIf</span></span>
<span data-ttu-id="fe851-158">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="fe851-158">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fe851-159">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="fe851-159">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fe851-160">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fe851-160">CommonParameters</span></span>
<span data-ttu-id="fe851-161">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="fe851-161">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fe851-162">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="fe851-162">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fe851-163">輸入</span><span class="sxs-lookup"><span data-stu-id="fe851-163">INPUTS</span></span>

### <span data-ttu-id="fe851-164">System.object</span><span class="sxs-lookup"><span data-stu-id="fe851-164">System.String</span></span>

## <span data-ttu-id="fe851-165">輸出</span><span class="sxs-lookup"><span data-stu-id="fe851-165">OUTPUTS</span></span>

### <span data-ttu-id="fe851-166">PSIotHub （IotHub.）。</span><span class="sxs-lookup"><span data-stu-id="fe851-166">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

## <span data-ttu-id="fe851-167">筆記</span><span class="sxs-lookup"><span data-stu-id="fe851-167">NOTES</span></span>

## <span data-ttu-id="fe851-168">相關連結</span><span class="sxs-lookup"><span data-stu-id="fe851-168">RELATED LINKS</span></span>
