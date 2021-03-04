---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/remove-azrouteserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzRouteServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzRouteServer.md
ms.openlocfilehash: 5fc8f30a2ef8a0ee276c9fb7ac3f1e2a503f6ec4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101912350"
---
# <span data-ttu-id="c1585-101">Remove-AzRouteServer</span><span class="sxs-lookup"><span data-stu-id="c1585-101">Remove-AzRouteServer</span></span>

## <span data-ttu-id="c1585-102">簡介</span><span class="sxs-lookup"><span data-stu-id="c1585-102">SYNOPSIS</span></span>
<span data-ttu-id="c1585-103">刪除 Azure RouteServer。</span><span class="sxs-lookup"><span data-stu-id="c1585-103">Deletes an Azure RouteServer.</span></span>

## <span data-ttu-id="c1585-104">語法</span><span class="sxs-lookup"><span data-stu-id="c1585-104">SYNTAX</span></span>

### <span data-ttu-id="c1585-105">RouteServerNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="c1585-105">RouteServerNameParameterSet (Default)</span></span>
```
Remove-AzRouteServer -ResourceGroupName <String> -RouteServerName <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c1585-106">RouteServerInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c1585-106">RouteServerInputObjectParameterSet</span></span>
```
Remove-AzRouteServer -InputObject <PSRouteServer> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c1585-107">RouteServerResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c1585-107">RouteServerResourceIdParameterSet</span></span>
```
Remove-AzRouteServer -ResourceId <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c1585-108">描述</span><span class="sxs-lookup"><span data-stu-id="c1585-108">DESCRIPTION</span></span>
<span data-ttu-id="c1585-109">**Remove-AzRouteServer** Cmdlet 會刪除 Azure RouteServer</span><span class="sxs-lookup"><span data-stu-id="c1585-109">The **Remove-AzRouteServer** cmdlet deletes an Azure RouteServer</span></span>

## <span data-ttu-id="c1585-110">例子</span><span class="sxs-lookup"><span data-stu-id="c1585-110">EXAMPLES</span></span>

### <span data-ttu-id="c1585-111">範例 1</span><span class="sxs-lookup"><span data-stu-id="c1585-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzRouteServer -ResourceGroupName routeServerRG -RouteServerName routeServer
```

### <span data-ttu-id="c1585-112">範例 2</span><span class="sxs-lookup"><span data-stu-id="c1585-112">Example 2</span></span>
```powershell
PS C:\> $routeServerId = '/subscriptions/8c992d64-fce9-426d-b278-85642dfeab03/resourceGroups/routeServerRG/providers/Microsoft.Network/virtualHubs/routeServer'
Remove-AzRouteServer -ResourceId $routeServerId
```

### <span data-ttu-id="c1585-113">範例 3</span><span class="sxs-lookup"><span data-stu-id="c1585-113">Example 3</span></span>
```powershell
PS C:\> $routeServer = Get-AzRouteServer -ResourceGroupName routeServerRG -RouteServerName routeServer
Remove-AzRouteServer -InputObject $routeServer
```

## <span data-ttu-id="c1585-114">參數</span><span class="sxs-lookup"><span data-stu-id="c1585-114">PARAMETERS</span></span>

### <span data-ttu-id="c1585-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c1585-115">-AsJob</span></span>
<span data-ttu-id="c1585-116">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="c1585-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="c1585-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c1585-117">-DefaultProfile</span></span>
<span data-ttu-id="c1585-118">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="c1585-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c1585-119">-強制</span><span class="sxs-lookup"><span data-stu-id="c1585-119">-Force</span></span>
<span data-ttu-id="c1585-120">如果您想要覆寫資源，請勿要求確認</span><span class="sxs-lookup"><span data-stu-id="c1585-120">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="c1585-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c1585-121">-InputObject</span></span>
<span data-ttu-id="c1585-122">路由伺服器輸入物件。</span><span class="sxs-lookup"><span data-stu-id="c1585-122">The route server input object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSRouteServer
Parameter Sets: RouteServerInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c1585-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c1585-123">-PassThru</span></span>
<span data-ttu-id="c1585-124">會返回代表執行此作業之專案的物件。</span><span class="sxs-lookup"><span data-stu-id="c1585-124">Returns an object representing the item on which this operation is being performed.</span></span>

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

### <span data-ttu-id="c1585-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c1585-125">-ResourceGroupName</span></span>
<span data-ttu-id="c1585-126">路由伺服器的資源組名。</span><span class="sxs-lookup"><span data-stu-id="c1585-126">The resource group name of the route server.</span></span>

```yaml
Type: System.String
Parameter Sets: RouteServerNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c1585-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c1585-127">-ResourceId</span></span>
<span data-ttu-id="c1585-128">路由伺服器資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="c1585-128">The route server resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: RouteServerResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c1585-129">-RouteServerName</span><span class="sxs-lookup"><span data-stu-id="c1585-129">-RouteServerName</span></span>
<span data-ttu-id="c1585-130">路由伺服器的名稱。</span><span class="sxs-lookup"><span data-stu-id="c1585-130">The name of the route server.</span></span>

```yaml
Type: System.String
Parameter Sets: RouteServerNameParameterSet
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c1585-131">-確認</span><span class="sxs-lookup"><span data-stu-id="c1585-131">-Confirm</span></span>
<span data-ttu-id="c1585-132">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="c1585-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c1585-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c1585-133">-WhatIf</span></span>
<span data-ttu-id="c1585-134">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="c1585-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c1585-135">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="c1585-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c1585-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c1585-136">CommonParameters</span></span>
<span data-ttu-id="c1585-137">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="c1585-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c1585-138">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c1585-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c1585-139">輸入</span><span class="sxs-lookup"><span data-stu-id="c1585-139">INPUTS</span></span>

### <span data-ttu-id="c1585-140">System.String</span><span class="sxs-lookup"><span data-stu-id="c1585-140">System.String</span></span>

### <span data-ttu-id="c1585-141">Microsoft.Azure.Commands.Network.models.PSRouteServer</span><span class="sxs-lookup"><span data-stu-id="c1585-141">Microsoft.Azure.Commands.Network.Models.PSRouteServer</span></span>

## <span data-ttu-id="c1585-142">輸出</span><span class="sxs-lookup"><span data-stu-id="c1585-142">OUTPUTS</span></span>

### <span data-ttu-id="c1585-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="c1585-143">System.Boolean</span></span>

## <span data-ttu-id="c1585-144">筆記</span><span class="sxs-lookup"><span data-stu-id="c1585-144">NOTES</span></span>

## <span data-ttu-id="c1585-145">相關連結</span><span class="sxs-lookup"><span data-stu-id="c1585-145">RELATED LINKS</span></span>
