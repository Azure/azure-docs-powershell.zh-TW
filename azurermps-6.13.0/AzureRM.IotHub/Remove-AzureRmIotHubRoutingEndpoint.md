---
external help file: Microsoft.Azure.Commands.IotHub.dll-Help.xml
Module Name: AzureRM.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.iothub/remove-azurermiothubroutingendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Remove-AzureRmIotHubRoutingEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Remove-AzureRmIotHubRoutingEndpoint.md
ms.openlocfilehash: 6caad4faec3dd292f902689757b82b90091afcde
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93455304"
---
# <span data-ttu-id="6ccea-101">Remove-AzureRmIotHubRoutingEndpoint</span><span class="sxs-lookup"><span data-stu-id="6ccea-101">Remove-AzureRmIotHubRoutingEndpoint</span></span>

## <span data-ttu-id="6ccea-102">摘要</span><span class="sxs-lookup"><span data-stu-id="6ccea-102">SYNOPSIS</span></span>
<span data-ttu-id="6ccea-103">刪除 IoT 中樞的端點</span><span class="sxs-lookup"><span data-stu-id="6ccea-103">Delete an endpoint for your IoT Hub</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6ccea-104">句法</span><span class="sxs-lookup"><span data-stu-id="6ccea-104">SYNTAX</span></span>

### <span data-ttu-id="6ccea-105">ResourceSet (預設) </span><span class="sxs-lookup"><span data-stu-id="6ccea-105">ResourceSet (Default)</span></span>
```
Remove-AzureRmIotHubRoutingEndpoint [-ResourceGroupName] <String> [-Name] <String> [-EndpointName <String>]
 [-EndpointType <PSEndpointType>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="6ccea-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="6ccea-106">InputObjectSet</span></span>
```
Remove-AzureRmIotHubRoutingEndpoint [-InputObject] <PSIotHub> [-EndpointName <String>]
 [-EndpointType <PSEndpointType>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="6ccea-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="6ccea-107">ResourceIdSet</span></span>
```
Remove-AzureRmIotHubRoutingEndpoint [-ResourceId] <String> [-EndpointName <String>]
 [-EndpointType <PSEndpointType>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="6ccea-108">說明</span><span class="sxs-lookup"><span data-stu-id="6ccea-108">DESCRIPTION</span></span>
<span data-ttu-id="6ccea-109">刪除端點。</span><span class="sxs-lookup"><span data-stu-id="6ccea-109">Delete an endpoint.</span></span> <span data-ttu-id="6ccea-110">請記得刪除使用此端點的任何路由。</span><span class="sxs-lookup"><span data-stu-id="6ccea-110">Remember to delete any routes that use this endpoint.</span></span>

## <span data-ttu-id="6ccea-111">示例</span><span class="sxs-lookup"><span data-stu-id="6ccea-111">EXAMPLES</span></span>

### <span data-ttu-id="6ccea-112">範例1</span><span class="sxs-lookup"><span data-stu-id="6ccea-112">Example 1</span></span>
```
PS C:\> Remove-AzureRmIotHubRoutingEndpoint -ResourceGroupName "myresourcegroup" -Name "myiothub" -EndpointName E2 -PassThru

True
```

<span data-ttu-id="6ccea-113">從 "myiothub" IoT 中樞刪除端點 "E2"。</span><span class="sxs-lookup"><span data-stu-id="6ccea-113">Delete endpoint "E2" from "myiothub" IoT Hub.</span></span>

## <span data-ttu-id="6ccea-114">參數</span><span class="sxs-lookup"><span data-stu-id="6ccea-114">PARAMETERS</span></span>

### <span data-ttu-id="6ccea-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6ccea-115">-DefaultProfile</span></span>
<span data-ttu-id="6ccea-116">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="6ccea-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6ccea-117">-終結點</span><span class="sxs-lookup"><span data-stu-id="6ccea-117">-EndpointName</span></span>
<span data-ttu-id="6ccea-118">路由端點的名稱</span><span class="sxs-lookup"><span data-stu-id="6ccea-118">Name of the Routing Endpoint</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6ccea-119">-EndpointType</span><span class="sxs-lookup"><span data-stu-id="6ccea-119">-EndpointType</span></span>
<span data-ttu-id="6ccea-120">路由端點的類型</span><span class="sxs-lookup"><span data-stu-id="6ccea-120">Type of the Routing Endpoint</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSEndpointType
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6ccea-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6ccea-121">-InputObject</span></span>
<span data-ttu-id="6ccea-122">IotHub 物件</span><span class="sxs-lookup"><span data-stu-id="6ccea-122">IotHub Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub
Parameter Sets: InputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6ccea-123">-名稱</span><span class="sxs-lookup"><span data-stu-id="6ccea-123">-Name</span></span>
<span data-ttu-id="6ccea-124">Iot 中樞的名稱</span><span class="sxs-lookup"><span data-stu-id="6ccea-124">Name of the Iot Hub</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6ccea-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6ccea-125">-PassThru</span></span>
<span data-ttu-id="6ccea-126">允許傳回布林值物件。</span><span class="sxs-lookup"><span data-stu-id="6ccea-126">Allows to return the boolean object.</span></span> <span data-ttu-id="6ccea-127">根據預設，這個 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="6ccea-127">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6ccea-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6ccea-128">-ResourceGroupName</span></span>
<span data-ttu-id="6ccea-129">資源群組的名稱</span><span class="sxs-lookup"><span data-stu-id="6ccea-129">Name of the Resource Group</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6ccea-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6ccea-130">-ResourceId</span></span>
<span data-ttu-id="6ccea-131">IotHub 資源識別碼</span><span class="sxs-lookup"><span data-stu-id="6ccea-131">IotHub Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6ccea-132">-確認</span><span class="sxs-lookup"><span data-stu-id="6ccea-132">-Confirm</span></span>
<span data-ttu-id="6ccea-133">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="6ccea-133">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6ccea-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6ccea-134">-WhatIf</span></span>
<span data-ttu-id="6ccea-135">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="6ccea-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6ccea-136">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="6ccea-136">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6ccea-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6ccea-137">CommonParameters</span></span>
<span data-ttu-id="6ccea-138">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="6ccea-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6ccea-139">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="6ccea-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6ccea-140">輸入</span><span class="sxs-lookup"><span data-stu-id="6ccea-140">INPUTS</span></span>

### <span data-ttu-id="6ccea-141">PSIotHub （IotHub.）。</span><span class="sxs-lookup"><span data-stu-id="6ccea-141">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>
<span data-ttu-id="6ccea-142">System.object</span><span class="sxs-lookup"><span data-stu-id="6ccea-142">System.String</span></span>

## <span data-ttu-id="6ccea-143">輸出</span><span class="sxs-lookup"><span data-stu-id="6ccea-143">OUTPUTS</span></span>

### <span data-ttu-id="6ccea-144">PSRoutingEventHubEndpoint （IotHub.）。</span><span class="sxs-lookup"><span data-stu-id="6ccea-144">Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingEventHubEndpoint</span></span>
<span data-ttu-id="6ccea-145">[System.object]. 清單 `1[[Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingEventHubProperties, Microsoft.Azure.Commands.IotHub, Version=3.1.3.0, Culture=neutral, PublicKeyToken=null]]
Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingServiceBusQueueEndpoint
System.Collections.Generic.List` 1 [IotHub. PSRoutingServiceBusQueueEndpointProperties，IotHub，版本 = 3.1.3.0，Culture = 中性，PublicKeyToken = null]].. List 1 [[]。清單 1 []。 |. 清單 1 []。 | " `1[[Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingServiceBusTopicEndpointProperties, Microsoft.Azure.Commands.IotHub, Version=3.1.3.0, Culture=neutral, PublicKeyToken=null]]
Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingStorageContainerEndpoint
System.Collections.Generic.List` microsoft Azure. IotHub （PSRoutingStorageContainerProperties） IotHub，版本 = 3.1.3.0，Culture = 中立，PublicKeyToken = null]] System. 集合. 清單 ' 1 []。 IotHub，版本 = PSRoutingCustomEndpoint，Culture = 中性，PublicKeyToken = IotHub，Culture = 中立，PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="6ccea-145">System.Collections.Generic.List`1[[Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingEventHubProperties, Microsoft.Azure.Commands.IotHub, Version=3.1.3.0, Culture=neutral, PublicKeyToken=null]]
Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingServiceBusQueueEndpoint
System.Collections.Generic.List`1[[Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingServiceBusQueueEndpointProperties, Microsoft.Azure.Commands.IotHub, Version=3.1.3.0, Culture=neutral, PublicKeyToken=null]] Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingServiceBusTopicEndpoint System.Collections.Generic.List`1[[Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingServiceBusTopicEndpointProperties, Microsoft.Azure.Commands.IotHub, Version=3.1.3.0, Culture=neutral, PublicKeyToken=null]]
Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingStorageContainerEndpoint
System.Collections.Generic.List`1[[Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingStorageContainerProperties, Microsoft.Azure.Commands.IotHub, Version=3.1.3.0, Culture=neutral, PublicKeyToken=null]] System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingCustomEndpoint, Microsoft.Azure.Commands.IotHub, Version=3.1.3.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="6ccea-146">筆記</span><span class="sxs-lookup"><span data-stu-id="6ccea-146">NOTES</span></span>

## <span data-ttu-id="6ccea-147">相關連結</span><span class="sxs-lookup"><span data-stu-id="6ccea-147">RELATED LINKS</span></span>
