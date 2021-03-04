---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/powershell/module/az.iothub/remove-aziothubroutingendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubRoutingEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubRoutingEndpoint.md
ms.openlocfilehash: 1b14ce37d03e1840336696792493e30701a09bfe
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101913861"
---
# <span data-ttu-id="44dfb-101">Remove-AzIotHubRoutingEndpoint</span><span class="sxs-lookup"><span data-stu-id="44dfb-101">Remove-AzIotHubRoutingEndpoint</span></span>

## <span data-ttu-id="44dfb-102">簡介</span><span class="sxs-lookup"><span data-stu-id="44dfb-102">SYNOPSIS</span></span>
<span data-ttu-id="44dfb-103">刪除 IoT 中樞的端點</span><span class="sxs-lookup"><span data-stu-id="44dfb-103">Delete an endpoint for your IoT Hub</span></span>

## <span data-ttu-id="44dfb-104">語法</span><span class="sxs-lookup"><span data-stu-id="44dfb-104">SYNTAX</span></span>

### <span data-ttu-id="44dfb-105">ResourceSet (預設) </span><span class="sxs-lookup"><span data-stu-id="44dfb-105">ResourceSet (Default)</span></span>
```
Remove-AzIotHubRoutingEndpoint [-ResourceGroupName] <String> [-Name] <String> [-EndpointName <String>]
 [-EndpointType <PSEndpointType>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="44dfb-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="44dfb-106">InputObjectSet</span></span>
```
Remove-AzIotHubRoutingEndpoint [-InputObject] <PSIotHub> [-EndpointName <String>]
 [-EndpointType <PSEndpointType>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="44dfb-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="44dfb-107">ResourceIdSet</span></span>
```
Remove-AzIotHubRoutingEndpoint [-ResourceId] <String> [-EndpointName <String>] [-EndpointType <PSEndpointType>]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="44dfb-108">描述</span><span class="sxs-lookup"><span data-stu-id="44dfb-108">DESCRIPTION</span></span>
<span data-ttu-id="44dfb-109">刪除端點。</span><span class="sxs-lookup"><span data-stu-id="44dfb-109">Delete an endpoint.</span></span> <span data-ttu-id="44dfb-110">請記得刪除任何使用此端點的路由。</span><span class="sxs-lookup"><span data-stu-id="44dfb-110">Remember to delete any routes that use this endpoint.</span></span>

## <span data-ttu-id="44dfb-111">例子</span><span class="sxs-lookup"><span data-stu-id="44dfb-111">EXAMPLES</span></span>

### <span data-ttu-id="44dfb-112">範例 1</span><span class="sxs-lookup"><span data-stu-id="44dfb-112">Example 1</span></span>
```
PS C:\> Remove-AzIotHubRoutingEndpoint -ResourceGroupName "myresourcegroup" -Name "myiothub" -EndpointName E2 -PassThru

True
```

<span data-ttu-id="44dfb-113">從 "myiothub" IoT Hub 刪除端點 "E2"。</span><span class="sxs-lookup"><span data-stu-id="44dfb-113">Delete endpoint "E2" from "myiothub" IoT Hub.</span></span>

## <span data-ttu-id="44dfb-114">參數</span><span class="sxs-lookup"><span data-stu-id="44dfb-114">PARAMETERS</span></span>

### <span data-ttu-id="44dfb-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="44dfb-115">-DefaultProfile</span></span>
<span data-ttu-id="44dfb-116">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="44dfb-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="44dfb-117">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="44dfb-117">-EndpointName</span></span>
<span data-ttu-id="44dfb-118">路由端點的名稱</span><span class="sxs-lookup"><span data-stu-id="44dfb-118">Name of the Routing Endpoint</span></span>

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

### <span data-ttu-id="44dfb-119">-EndpointType</span><span class="sxs-lookup"><span data-stu-id="44dfb-119">-EndpointType</span></span>
<span data-ttu-id="44dfb-120">路由端點的類型</span><span class="sxs-lookup"><span data-stu-id="44dfb-120">Type of the Routing Endpoint</span></span>

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

### <span data-ttu-id="44dfb-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="44dfb-121">-InputObject</span></span>
<span data-ttu-id="44dfb-122">IotHub 物件</span><span class="sxs-lookup"><span data-stu-id="44dfb-122">IotHub Object</span></span>

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

### <span data-ttu-id="44dfb-123">-名稱</span><span class="sxs-lookup"><span data-stu-id="44dfb-123">-Name</span></span>
<span data-ttu-id="44dfb-124">Iot Hub 的名稱</span><span class="sxs-lookup"><span data-stu-id="44dfb-124">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="44dfb-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="44dfb-125">-PassThru</span></span>
<span data-ttu-id="44dfb-126">允許返回布林值物件。</span><span class="sxs-lookup"><span data-stu-id="44dfb-126">Allows to return the boolean object.</span></span> <span data-ttu-id="44dfb-127">根據預設，此 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="44dfb-127">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="44dfb-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="44dfb-128">-ResourceGroupName</span></span>
<span data-ttu-id="44dfb-129">資源組的名稱</span><span class="sxs-lookup"><span data-stu-id="44dfb-129">Name of the Resource Group</span></span>

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

### <span data-ttu-id="44dfb-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="44dfb-130">-ResourceId</span></span>
<span data-ttu-id="44dfb-131">IotHub 資源識別碼</span><span class="sxs-lookup"><span data-stu-id="44dfb-131">IotHub Resource Id</span></span>

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

### <span data-ttu-id="44dfb-132">-確認</span><span class="sxs-lookup"><span data-stu-id="44dfb-132">-Confirm</span></span>
<span data-ttu-id="44dfb-133">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="44dfb-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="44dfb-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="44dfb-134">-WhatIf</span></span>
<span data-ttu-id="44dfb-135">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="44dfb-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="44dfb-136">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="44dfb-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="44dfb-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="44dfb-137">CommonParameters</span></span>
<span data-ttu-id="44dfb-138">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="44dfb-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="44dfb-139">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="44dfb-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="44dfb-140">輸入</span><span class="sxs-lookup"><span data-stu-id="44dfb-140">INPUTS</span></span>

### <span data-ttu-id="44dfb-141">Microsoft.Azure.Commands.management.IotHub.models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="44dfb-141">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="44dfb-142">System.String</span><span class="sxs-lookup"><span data-stu-id="44dfb-142">System.String</span></span>

## <span data-ttu-id="44dfb-143">輸出</span><span class="sxs-lookup"><span data-stu-id="44dfb-143">OUTPUTS</span></span>

### <span data-ttu-id="44dfb-144">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="44dfb-144">System.Boolean</span></span>

## <span data-ttu-id="44dfb-145">筆記</span><span class="sxs-lookup"><span data-stu-id="44dfb-145">NOTES</span></span>

## <span data-ttu-id="44dfb-146">相關連結</span><span class="sxs-lookup"><span data-stu-id="44dfb-146">RELATED LINKS</span></span>
