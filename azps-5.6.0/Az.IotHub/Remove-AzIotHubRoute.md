---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/powershell/module/az.iothub/remove-aziothubroute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubRoute.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubRoute.md
ms.openlocfilehash: 0ce0a651444bd30a1bf6c766083b0a8584c5cd71
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101913193"
---
# <span data-ttu-id="5603a-101">Remove-AzIotHubRoute</span><span class="sxs-lookup"><span data-stu-id="5603a-101">Remove-AzIotHubRoute</span></span>

## <span data-ttu-id="5603a-102">簡介</span><span class="sxs-lookup"><span data-stu-id="5603a-102">SYNOPSIS</span></span>
<span data-ttu-id="5603a-103">刪除 IoT 中心中的路由</span><span class="sxs-lookup"><span data-stu-id="5603a-103">Delete a route in IoT Hub</span></span>

## <span data-ttu-id="5603a-104">語法</span><span class="sxs-lookup"><span data-stu-id="5603a-104">SYNTAX</span></span>

### <span data-ttu-id="5603a-105">ResourceSet (預設) </span><span class="sxs-lookup"><span data-stu-id="5603a-105">ResourceSet (Default)</span></span>
```
Remove-AzIotHubRoute [-ResourceGroupName] <String> [-Name] <String> [-RouteName <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5603a-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="5603a-106">InputObjectSet</span></span>
```
Remove-AzIotHubRoute [-InputObject] <PSIotHub> [-RouteName <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5603a-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="5603a-107">ResourceIdSet</span></span>
```
Remove-AzIotHubRoute [-ResourceId] <String> [-RouteName <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5603a-108">描述</span><span class="sxs-lookup"><span data-stu-id="5603a-108">DESCRIPTION</span></span>
<span data-ttu-id="5603a-109">刪除端點的路由</span><span class="sxs-lookup"><span data-stu-id="5603a-109">Delete a routes to an endpoint</span></span>

## <span data-ttu-id="5603a-110">例子</span><span class="sxs-lookup"><span data-stu-id="5603a-110">EXAMPLES</span></span>

### <span data-ttu-id="5603a-111">範例 1</span><span class="sxs-lookup"><span data-stu-id="5603a-111">Example 1</span></span>
```
PS C:\> Remove-AzIotHubRoute -ResourceGroupName "myresourcegroup" -Name "myiothub" -RouteName R1 -PassThru

True
```

<span data-ttu-id="5603a-112">從 "myiothub" IoT 中心刪除路由 "R1"。</span><span class="sxs-lookup"><span data-stu-id="5603a-112">Delete route "R1" from "myiothub" IoT Hub.</span></span>

## <span data-ttu-id="5603a-113">參數</span><span class="sxs-lookup"><span data-stu-id="5603a-113">PARAMETERS</span></span>

### <span data-ttu-id="5603a-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5603a-114">-DefaultProfile</span></span>
<span data-ttu-id="5603a-115">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="5603a-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5603a-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5603a-116">-InputObject</span></span>
<span data-ttu-id="5603a-117">IotHub 物件</span><span class="sxs-lookup"><span data-stu-id="5603a-117">IotHub Object</span></span>

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

### <span data-ttu-id="5603a-118">-名稱</span><span class="sxs-lookup"><span data-stu-id="5603a-118">-Name</span></span>
<span data-ttu-id="5603a-119">Iot Hub 的名稱</span><span class="sxs-lookup"><span data-stu-id="5603a-119">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="5603a-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5603a-120">-PassThru</span></span>
<span data-ttu-id="5603a-121">允許返回布林值物件。</span><span class="sxs-lookup"><span data-stu-id="5603a-121">Allows to return the boolean object.</span></span> <span data-ttu-id="5603a-122">根據預設，此 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="5603a-122">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="5603a-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5603a-123">-ResourceGroupName</span></span>
<span data-ttu-id="5603a-124">資源組的名稱</span><span class="sxs-lookup"><span data-stu-id="5603a-124">Name of the Resource Group</span></span>

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

### <span data-ttu-id="5603a-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5603a-125">-ResourceId</span></span>
<span data-ttu-id="5603a-126">IotHub 資源識別碼</span><span class="sxs-lookup"><span data-stu-id="5603a-126">IotHub Resource Id</span></span>

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

### <span data-ttu-id="5603a-127">-RouteName</span><span class="sxs-lookup"><span data-stu-id="5603a-127">-RouteName</span></span>
<span data-ttu-id="5603a-128">路線名稱</span><span class="sxs-lookup"><span data-stu-id="5603a-128">Name of the Route</span></span>

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

### <span data-ttu-id="5603a-129">-確認</span><span class="sxs-lookup"><span data-stu-id="5603a-129">-Confirm</span></span>
<span data-ttu-id="5603a-130">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="5603a-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5603a-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5603a-131">-WhatIf</span></span>
<span data-ttu-id="5603a-132">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="5603a-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5603a-133">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="5603a-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5603a-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5603a-134">CommonParameters</span></span>
<span data-ttu-id="5603a-135">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="5603a-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5603a-136">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="5603a-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5603a-137">輸入</span><span class="sxs-lookup"><span data-stu-id="5603a-137">INPUTS</span></span>

### <span data-ttu-id="5603a-138">Microsoft.Azure.Commands.management.IotHub.models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="5603a-138">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="5603a-139">System.String</span><span class="sxs-lookup"><span data-stu-id="5603a-139">System.String</span></span>

## <span data-ttu-id="5603a-140">輸出</span><span class="sxs-lookup"><span data-stu-id="5603a-140">OUTPUTS</span></span>

### <span data-ttu-id="5603a-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="5603a-141">System.Boolean</span></span>

## <span data-ttu-id="5603a-142">筆記</span><span class="sxs-lookup"><span data-stu-id="5603a-142">NOTES</span></span>

## <span data-ttu-id="5603a-143">相關連結</span><span class="sxs-lookup"><span data-stu-id="5603a-143">RELATED LINKS</span></span>
