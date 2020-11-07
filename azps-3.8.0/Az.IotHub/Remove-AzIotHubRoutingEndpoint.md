---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/remove-aziothubroutingendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubRoutingEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubRoutingEndpoint.md
ms.openlocfilehash: f162bf5f22ab435dd0d340bfd96db1ae616ccc96
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93957358"
---
# <span data-ttu-id="76d85-101">Remove-AzIotHubRoutingEndpoint</span><span class="sxs-lookup"><span data-stu-id="76d85-101">Remove-AzIotHubRoutingEndpoint</span></span>

## <span data-ttu-id="76d85-102">摘要</span><span class="sxs-lookup"><span data-stu-id="76d85-102">SYNOPSIS</span></span>
<span data-ttu-id="76d85-103">刪除 IoT 中樞的端點</span><span class="sxs-lookup"><span data-stu-id="76d85-103">Delete an endpoint for your IoT Hub</span></span>

## <span data-ttu-id="76d85-104">句法</span><span class="sxs-lookup"><span data-stu-id="76d85-104">SYNTAX</span></span>

### <span data-ttu-id="76d85-105">ResourceSet (預設) </span><span class="sxs-lookup"><span data-stu-id="76d85-105">ResourceSet (Default)</span></span>
```
Remove-AzIotHubRoutingEndpoint [-ResourceGroupName] <String> [-Name] <String> [-EndpointName <String>]
 [-EndpointType <PSEndpointType>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="76d85-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="76d85-106">InputObjectSet</span></span>
```
Remove-AzIotHubRoutingEndpoint [-InputObject] <PSIotHub> [-EndpointName <String>]
 [-EndpointType <PSEndpointType>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="76d85-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="76d85-107">ResourceIdSet</span></span>
```
Remove-AzIotHubRoutingEndpoint [-ResourceId] <String> [-EndpointName <String>] [-EndpointType <PSEndpointType>]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="76d85-108">說明</span><span class="sxs-lookup"><span data-stu-id="76d85-108">DESCRIPTION</span></span>
<span data-ttu-id="76d85-109">刪除端點。</span><span class="sxs-lookup"><span data-stu-id="76d85-109">Delete an endpoint.</span></span> <span data-ttu-id="76d85-110">請記得刪除使用此端點的任何路由。</span><span class="sxs-lookup"><span data-stu-id="76d85-110">Remember to delete any routes that use this endpoint.</span></span>

## <span data-ttu-id="76d85-111">示例</span><span class="sxs-lookup"><span data-stu-id="76d85-111">EXAMPLES</span></span>

### <span data-ttu-id="76d85-112">範例1</span><span class="sxs-lookup"><span data-stu-id="76d85-112">Example 1</span></span>
```
PS C:\> Remove-AzIotHubRoutingEndpoint -ResourceGroupName "myresourcegroup" -Name "myiothub" -EndpointName E2 -PassThru

True
```

<span data-ttu-id="76d85-113">從 "myiothub" IoT 中樞刪除端點 "E2"。</span><span class="sxs-lookup"><span data-stu-id="76d85-113">Delete endpoint "E2" from "myiothub" IoT Hub.</span></span>

## <span data-ttu-id="76d85-114">參數</span><span class="sxs-lookup"><span data-stu-id="76d85-114">PARAMETERS</span></span>

### <span data-ttu-id="76d85-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="76d85-115">-DefaultProfile</span></span>
<span data-ttu-id="76d85-116">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="76d85-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="76d85-117">-終結點</span><span class="sxs-lookup"><span data-stu-id="76d85-117">-EndpointName</span></span>
<span data-ttu-id="76d85-118">路由端點的名稱</span><span class="sxs-lookup"><span data-stu-id="76d85-118">Name of the Routing Endpoint</span></span>

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

### <span data-ttu-id="76d85-119">-EndpointType</span><span class="sxs-lookup"><span data-stu-id="76d85-119">-EndpointType</span></span>
<span data-ttu-id="76d85-120">路由端點的類型</span><span class="sxs-lookup"><span data-stu-id="76d85-120">Type of the Routing Endpoint</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSEndpointType
Parameter Sets: (All)
Aliases:
Accepted values: EventHub, ServiceBusQueue, ServiceBusTopic, AzureStorageContainer

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="76d85-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="76d85-121">-InputObject</span></span>
<span data-ttu-id="76d85-122">IotHub 物件</span><span class="sxs-lookup"><span data-stu-id="76d85-122">IotHub Object</span></span>

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

### <span data-ttu-id="76d85-123">-名稱</span><span class="sxs-lookup"><span data-stu-id="76d85-123">-Name</span></span>
<span data-ttu-id="76d85-124">Iot 中樞的名稱</span><span class="sxs-lookup"><span data-stu-id="76d85-124">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="76d85-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="76d85-125">-PassThru</span></span>
<span data-ttu-id="76d85-126">允許傳回布林值物件。</span><span class="sxs-lookup"><span data-stu-id="76d85-126">Allows to return the boolean object.</span></span> <span data-ttu-id="76d85-127">根據預設，這個 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="76d85-127">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="76d85-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="76d85-128">-ResourceGroupName</span></span>
<span data-ttu-id="76d85-129">資源群組的名稱</span><span class="sxs-lookup"><span data-stu-id="76d85-129">Name of the Resource Group</span></span>

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

### <span data-ttu-id="76d85-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="76d85-130">-ResourceId</span></span>
<span data-ttu-id="76d85-131">IotHub 資源識別碼</span><span class="sxs-lookup"><span data-stu-id="76d85-131">IotHub Resource Id</span></span>

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

### <span data-ttu-id="76d85-132">-確認</span><span class="sxs-lookup"><span data-stu-id="76d85-132">-Confirm</span></span>
<span data-ttu-id="76d85-133">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="76d85-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="76d85-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="76d85-134">-WhatIf</span></span>
<span data-ttu-id="76d85-135">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="76d85-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="76d85-136">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="76d85-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="76d85-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="76d85-137">CommonParameters</span></span>
<span data-ttu-id="76d85-138">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="76d85-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="76d85-139">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="76d85-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="76d85-140">輸入</span><span class="sxs-lookup"><span data-stu-id="76d85-140">INPUTS</span></span>

### <span data-ttu-id="76d85-141">PSIotHub （IotHub.）。</span><span class="sxs-lookup"><span data-stu-id="76d85-141">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="76d85-142">System.object</span><span class="sxs-lookup"><span data-stu-id="76d85-142">System.String</span></span>

## <span data-ttu-id="76d85-143">輸出</span><span class="sxs-lookup"><span data-stu-id="76d85-143">OUTPUTS</span></span>

### <span data-ttu-id="76d85-144">System.object</span><span class="sxs-lookup"><span data-stu-id="76d85-144">System.Boolean</span></span>

## <span data-ttu-id="76d85-145">筆記</span><span class="sxs-lookup"><span data-stu-id="76d85-145">NOTES</span></span>

## <span data-ttu-id="76d85-146">相關連結</span><span class="sxs-lookup"><span data-stu-id="76d85-146">RELATED LINKS</span></span>
