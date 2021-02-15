---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azrouteserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzRouteServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzRouteServer.md
ms.openlocfilehash: 2b50d49c108408e1639b5f5f490c2aaafc7bbd82
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100134875"
---
# <span data-ttu-id="1afdd-101">Remove-AzRouteServer</span><span class="sxs-lookup"><span data-stu-id="1afdd-101">Remove-AzRouteServer</span></span>

## <span data-ttu-id="1afdd-102">摘要</span><span class="sxs-lookup"><span data-stu-id="1afdd-102">SYNOPSIS</span></span>
<span data-ttu-id="1afdd-103">刪除 Azure RouteServer。</span><span class="sxs-lookup"><span data-stu-id="1afdd-103">Deletes an Azure RouteServer.</span></span>

## <span data-ttu-id="1afdd-104">句法</span><span class="sxs-lookup"><span data-stu-id="1afdd-104">SYNTAX</span></span>

### <span data-ttu-id="1afdd-105">RouteServerNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="1afdd-105">RouteServerNameParameterSet (Default)</span></span>
```
Remove-AzRouteServer -ResourceGroupName <String> -RouteServerName <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1afdd-106">RouteServerInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="1afdd-106">RouteServerInputObjectParameterSet</span></span>
```
Remove-AzRouteServer -InputObject <PSRouteServer> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1afdd-107">RouteServerResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="1afdd-107">RouteServerResourceIdParameterSet</span></span>
```
Remove-AzRouteServer -ResourceId <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1afdd-108">說明</span><span class="sxs-lookup"><span data-stu-id="1afdd-108">DESCRIPTION</span></span>
<span data-ttu-id="1afdd-109">**AzRouteServer** Cmdlet 會刪除 Azure RouteServer</span><span class="sxs-lookup"><span data-stu-id="1afdd-109">The **Remove-AzRouteServer** cmdlet deletes an Azure RouteServer</span></span>

## <span data-ttu-id="1afdd-110">示例</span><span class="sxs-lookup"><span data-stu-id="1afdd-110">EXAMPLES</span></span>

### <span data-ttu-id="1afdd-111">範例1</span><span class="sxs-lookup"><span data-stu-id="1afdd-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzRouteServer -ResourceGroupName routeServerRG -RouteServerName routeServer
```

### <span data-ttu-id="1afdd-112">範例2</span><span class="sxs-lookup"><span data-stu-id="1afdd-112">Example 2</span></span>
```powershell
PS C:\> $routeServerId = '/subscriptions/8c992d64-fce9-426d-b278-85642dfeab03/resourceGroups/routeServerRG/providers/Microsoft.Network/virtualHubs/routeServer'
Remove-AzRouteServer -ResourceId $routeServerId
```

### <span data-ttu-id="1afdd-113">範例3</span><span class="sxs-lookup"><span data-stu-id="1afdd-113">Example 3</span></span>
```powershell
PS C:\> $routeServer = Get-AzRouteServer -ResourceGroupName routeServerRG -RouteServerName routeServer
Remove-AzRouteServer -InputObject $routeServer
```

## <span data-ttu-id="1afdd-114">參數</span><span class="sxs-lookup"><span data-stu-id="1afdd-114">PARAMETERS</span></span>

### <span data-ttu-id="1afdd-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1afdd-115">-AsJob</span></span>
<span data-ttu-id="1afdd-116">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="1afdd-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="1afdd-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1afdd-117">-DefaultProfile</span></span>
<span data-ttu-id="1afdd-118">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="1afdd-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1afdd-119">-Force</span><span class="sxs-lookup"><span data-stu-id="1afdd-119">-Force</span></span>
<span data-ttu-id="1afdd-120">若要覆寫資源，請不要要求確認</span><span class="sxs-lookup"><span data-stu-id="1afdd-120">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="1afdd-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1afdd-121">-InputObject</span></span>
<span data-ttu-id="1afdd-122">[路由伺服器] 輸入物件。</span><span class="sxs-lookup"><span data-stu-id="1afdd-122">The route server input object.</span></span>

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

### <span data-ttu-id="1afdd-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1afdd-123">-PassThru</span></span>
<span data-ttu-id="1afdd-124">傳回代表執行此作業之專案的物件。</span><span class="sxs-lookup"><span data-stu-id="1afdd-124">Returns an object representing the item on which this operation is being performed.</span></span>

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

### <span data-ttu-id="1afdd-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1afdd-125">-ResourceGroupName</span></span>
<span data-ttu-id="1afdd-126">路由伺服器的資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="1afdd-126">The resource group name of the route server.</span></span>

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

### <span data-ttu-id="1afdd-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1afdd-127">-ResourceId</span></span>
<span data-ttu-id="1afdd-128">[路由伺服器] 資源 Id。</span><span class="sxs-lookup"><span data-stu-id="1afdd-128">The route server resource Id.</span></span>

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

### <span data-ttu-id="1afdd-129">-RouteServerName</span><span class="sxs-lookup"><span data-stu-id="1afdd-129">-RouteServerName</span></span>
<span data-ttu-id="1afdd-130">路由伺服器的名稱。</span><span class="sxs-lookup"><span data-stu-id="1afdd-130">The name of the route server.</span></span>

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

### <span data-ttu-id="1afdd-131">-確認</span><span class="sxs-lookup"><span data-stu-id="1afdd-131">-Confirm</span></span>
<span data-ttu-id="1afdd-132">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="1afdd-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1afdd-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1afdd-133">-WhatIf</span></span>
<span data-ttu-id="1afdd-134">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="1afdd-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1afdd-135">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="1afdd-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1afdd-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1afdd-136">CommonParameters</span></span>
<span data-ttu-id="1afdd-137">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="1afdd-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1afdd-138">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="1afdd-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1afdd-139">輸入</span><span class="sxs-lookup"><span data-stu-id="1afdd-139">INPUTS</span></span>

### <span data-ttu-id="1afdd-140">System.object</span><span class="sxs-lookup"><span data-stu-id="1afdd-140">System.String</span></span>

### <span data-ttu-id="1afdd-141">PSRouteServer 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="1afdd-141">Microsoft.Azure.Commands.Network.Models.PSRouteServer</span></span>

## <span data-ttu-id="1afdd-142">輸出</span><span class="sxs-lookup"><span data-stu-id="1afdd-142">OUTPUTS</span></span>

### <span data-ttu-id="1afdd-143">System.object</span><span class="sxs-lookup"><span data-stu-id="1afdd-143">System.Boolean</span></span>

## <span data-ttu-id="1afdd-144">筆記</span><span class="sxs-lookup"><span data-stu-id="1afdd-144">NOTES</span></span>

## <span data-ttu-id="1afdd-145">相關連結</span><span class="sxs-lookup"><span data-stu-id="1afdd-145">RELATED LINKS</span></span>
