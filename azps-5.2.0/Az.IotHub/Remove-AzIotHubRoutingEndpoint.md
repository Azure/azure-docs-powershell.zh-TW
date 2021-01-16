---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/remove-aziothubroutingendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubRoutingEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubRoutingEndpoint.md
ms.openlocfilehash: f162bf5f22ab435dd0d340bfd96db1ae616ccc96
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98281332"
---
# <span data-ttu-id="46ede-101">Remove-AzIotHubRoutingEndpoint</span><span class="sxs-lookup"><span data-stu-id="46ede-101">Remove-AzIotHubRoutingEndpoint</span></span>

## <span data-ttu-id="46ede-102">摘要</span><span class="sxs-lookup"><span data-stu-id="46ede-102">SYNOPSIS</span></span>
<span data-ttu-id="46ede-103">刪除 IoT 中樞的端點</span><span class="sxs-lookup"><span data-stu-id="46ede-103">Delete an endpoint for your IoT Hub</span></span>

## <span data-ttu-id="46ede-104">句法</span><span class="sxs-lookup"><span data-stu-id="46ede-104">SYNTAX</span></span>

### <span data-ttu-id="46ede-105">ResourceSet (預設) </span><span class="sxs-lookup"><span data-stu-id="46ede-105">ResourceSet (Default)</span></span>
```
Remove-AzIotHubRoutingEndpoint [-ResourceGroupName] <String> [-Name] <String> [-EndpointName <String>]
 [-EndpointType <PSEndpointType>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="46ede-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="46ede-106">InputObjectSet</span></span>
```
Remove-AzIotHubRoutingEndpoint [-InputObject] <PSIotHub> [-EndpointName <String>]
 [-EndpointType <PSEndpointType>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="46ede-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="46ede-107">ResourceIdSet</span></span>
```
Remove-AzIotHubRoutingEndpoint [-ResourceId] <String> [-EndpointName <String>] [-EndpointType <PSEndpointType>]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="46ede-108">說明</span><span class="sxs-lookup"><span data-stu-id="46ede-108">DESCRIPTION</span></span>
<span data-ttu-id="46ede-109">刪除端點。</span><span class="sxs-lookup"><span data-stu-id="46ede-109">Delete an endpoint.</span></span> <span data-ttu-id="46ede-110">請記得刪除使用此端點的任何路由。</span><span class="sxs-lookup"><span data-stu-id="46ede-110">Remember to delete any routes that use this endpoint.</span></span>

## <span data-ttu-id="46ede-111">示例</span><span class="sxs-lookup"><span data-stu-id="46ede-111">EXAMPLES</span></span>

### <span data-ttu-id="46ede-112">範例1</span><span class="sxs-lookup"><span data-stu-id="46ede-112">Example 1</span></span>
```
PS C:\> Remove-AzIotHubRoutingEndpoint -ResourceGroupName "myresourcegroup" -Name "myiothub" -EndpointName E2 -PassThru

True
```

<span data-ttu-id="46ede-113">從 "myiothub" IoT 中樞刪除端點 "E2"。</span><span class="sxs-lookup"><span data-stu-id="46ede-113">Delete endpoint "E2" from "myiothub" IoT Hub.</span></span>

## <span data-ttu-id="46ede-114">參數</span><span class="sxs-lookup"><span data-stu-id="46ede-114">PARAMETERS</span></span>

### <span data-ttu-id="46ede-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="46ede-115">-DefaultProfile</span></span>
<span data-ttu-id="46ede-116">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="46ede-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="46ede-117">-終結點</span><span class="sxs-lookup"><span data-stu-id="46ede-117">-EndpointName</span></span>
<span data-ttu-id="46ede-118">路由端點的名稱</span><span class="sxs-lookup"><span data-stu-id="46ede-118">Name of the Routing Endpoint</span></span>

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

### <span data-ttu-id="46ede-119">-EndpointType</span><span class="sxs-lookup"><span data-stu-id="46ede-119">-EndpointType</span></span>
<span data-ttu-id="46ede-120">路由端點的類型</span><span class="sxs-lookup"><span data-stu-id="46ede-120">Type of the Routing Endpoint</span></span>

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

### <span data-ttu-id="46ede-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="46ede-121">-InputObject</span></span>
<span data-ttu-id="46ede-122">IotHub 物件</span><span class="sxs-lookup"><span data-stu-id="46ede-122">IotHub Object</span></span>

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

### <span data-ttu-id="46ede-123">-名稱</span><span class="sxs-lookup"><span data-stu-id="46ede-123">-Name</span></span>
<span data-ttu-id="46ede-124">Iot 中樞的名稱</span><span class="sxs-lookup"><span data-stu-id="46ede-124">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="46ede-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="46ede-125">-PassThru</span></span>
<span data-ttu-id="46ede-126">允許傳回布林值物件。</span><span class="sxs-lookup"><span data-stu-id="46ede-126">Allows to return the boolean object.</span></span> <span data-ttu-id="46ede-127">根據預設，這個 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="46ede-127">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="46ede-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="46ede-128">-ResourceGroupName</span></span>
<span data-ttu-id="46ede-129">資源群組的名稱</span><span class="sxs-lookup"><span data-stu-id="46ede-129">Name of the Resource Group</span></span>

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

### <span data-ttu-id="46ede-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="46ede-130">-ResourceId</span></span>
<span data-ttu-id="46ede-131">IotHub 資源識別碼</span><span class="sxs-lookup"><span data-stu-id="46ede-131">IotHub Resource Id</span></span>

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

### <span data-ttu-id="46ede-132">-確認</span><span class="sxs-lookup"><span data-stu-id="46ede-132">-Confirm</span></span>
<span data-ttu-id="46ede-133">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="46ede-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="46ede-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="46ede-134">-WhatIf</span></span>
<span data-ttu-id="46ede-135">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="46ede-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="46ede-136">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="46ede-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="46ede-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="46ede-137">CommonParameters</span></span>
<span data-ttu-id="46ede-138">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="46ede-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="46ede-139">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="46ede-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="46ede-140">輸入</span><span class="sxs-lookup"><span data-stu-id="46ede-140">INPUTS</span></span>

### <span data-ttu-id="46ede-141">PSIotHub （IotHub.）。</span><span class="sxs-lookup"><span data-stu-id="46ede-141">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="46ede-142">System.object</span><span class="sxs-lookup"><span data-stu-id="46ede-142">System.String</span></span>

## <span data-ttu-id="46ede-143">輸出</span><span class="sxs-lookup"><span data-stu-id="46ede-143">OUTPUTS</span></span>

### <span data-ttu-id="46ede-144">System.object</span><span class="sxs-lookup"><span data-stu-id="46ede-144">System.Boolean</span></span>

## <span data-ttu-id="46ede-145">筆記</span><span class="sxs-lookup"><span data-stu-id="46ede-145">NOTES</span></span>

## <span data-ttu-id="46ede-146">相關連結</span><span class="sxs-lookup"><span data-stu-id="46ede-146">RELATED LINKS</span></span>
