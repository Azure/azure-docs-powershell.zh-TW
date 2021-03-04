---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/update-azrouteserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzRouteServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzRouteServer.md
ms.openlocfilehash: 3cb1fe0fb72182e22c4f7653de26f356ecd823ed
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101901826"
---
# <span data-ttu-id="7884e-101">Update-AzRouteServer</span><span class="sxs-lookup"><span data-stu-id="7884e-101">Update-AzRouteServer</span></span>

## <span data-ttu-id="7884e-102">簡介</span><span class="sxs-lookup"><span data-stu-id="7884e-102">SYNOPSIS</span></span>
<span data-ttu-id="7884e-103">更新 Azure RouteServer。</span><span class="sxs-lookup"><span data-stu-id="7884e-103">Update an Azure RouteServer.</span></span>

## <span data-ttu-id="7884e-104">語法</span><span class="sxs-lookup"><span data-stu-id="7884e-104">SYNTAX</span></span>

### <span data-ttu-id="7884e-105">RouteServerNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="7884e-105">RouteServerNameParameterSet (Default)</span></span>
```
Update-AzRouteServer -ResourceGroupName <String> -RouteServerName <String> [-AllowBranchToBranchTraffic]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7884e-106">RouteServerResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="7884e-106">RouteServerResourceIdParameterSet</span></span>
```
Update-AzRouteServer [-AllowBranchToBranchTraffic] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7884e-107">描述</span><span class="sxs-lookup"><span data-stu-id="7884e-107">DESCRIPTION</span></span>
<span data-ttu-id="7884e-108">**Update-AzRouteServer** Cmdlet 將分支到分支流量切換到 Azure RouteServer。</span><span class="sxs-lookup"><span data-stu-id="7884e-108">The **Update-AzRouteServer** cmdlet switches the branch-to-branch traffic to an Azure RouteServer.</span></span>

## <span data-ttu-id="7884e-109">例子</span><span class="sxs-lookup"><span data-stu-id="7884e-109">EXAMPLES</span></span>

### <span data-ttu-id="7884e-110">範例 1</span><span class="sxs-lookup"><span data-stu-id="7884e-110">Example 1</span></span>
```powershell
PS C:\>  Update-AzRouteServer -ResourceGroupName $rgname -RouteServerName $routeServerName -AllowBranchToBranchTraffic
```
<span data-ttu-id="7884e-111">若要針對路由伺服器啟用分支至分支流量。</span><span class="sxs-lookup"><span data-stu-id="7884e-111">To enable branch to branch traffic for route server.</span></span>

### <span data-ttu-id="7884e-112">範例 1</span><span class="sxs-lookup"><span data-stu-id="7884e-112">Example 1</span></span>
```powershell
PS C:\>  Update-AzRouteServer -ResourceGroupName $rgname -RouteServerName $routeServerName
```
<span data-ttu-id="7884e-113">若要停用路由伺服器的分支到分支流量。</span><span class="sxs-lookup"><span data-stu-id="7884e-113">To disable branch to branch traffic for route server.</span></span>

## <span data-ttu-id="7884e-114">參數</span><span class="sxs-lookup"><span data-stu-id="7884e-114">PARAMETERS</span></span>

### <span data-ttu-id="7884e-115">-AllowBranchToBranchTraffic</span><span class="sxs-lookup"><span data-stu-id="7884e-115">-AllowBranchToBranchTraffic</span></span>
<span data-ttu-id="7884e-116">旗標以允許路由伺服器的分支至分支流量。</span><span class="sxs-lookup"><span data-stu-id="7884e-116">Flag to allow branch to branch traffic for route server.</span></span>

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

### <span data-ttu-id="7884e-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7884e-117">-DefaultProfile</span></span>
<span data-ttu-id="7884e-118">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="7884e-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7884e-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7884e-119">-ResourceGroupName</span></span>
<span data-ttu-id="7884e-120">路由伺服器的資源組名。</span><span class="sxs-lookup"><span data-stu-id="7884e-120">The resource group name of the route server.</span></span>

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

### <span data-ttu-id="7884e-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7884e-121">-ResourceId</span></span>
<span data-ttu-id="7884e-122">路由伺服器的 ResourceId。</span><span class="sxs-lookup"><span data-stu-id="7884e-122">ResourceId of the route server.</span></span>

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

### <span data-ttu-id="7884e-123">-RouteServerName</span><span class="sxs-lookup"><span data-stu-id="7884e-123">-RouteServerName</span></span>
<span data-ttu-id="7884e-124">路由伺服器的名稱。</span><span class="sxs-lookup"><span data-stu-id="7884e-124">The name of the route server.</span></span>

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

### <span data-ttu-id="7884e-125">-確認</span><span class="sxs-lookup"><span data-stu-id="7884e-125">-Confirm</span></span>
<span data-ttu-id="7884e-126">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="7884e-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7884e-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7884e-127">-WhatIf</span></span>
<span data-ttu-id="7884e-128">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="7884e-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7884e-129">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="7884e-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7884e-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7884e-130">CommonParameters</span></span>
<span data-ttu-id="7884e-131">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="7884e-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7884e-132">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7884e-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7884e-133">輸入</span><span class="sxs-lookup"><span data-stu-id="7884e-133">INPUTS</span></span>

### <span data-ttu-id="7884e-134">System.String</span><span class="sxs-lookup"><span data-stu-id="7884e-134">System.String</span></span>

## <span data-ttu-id="7884e-135">輸出</span><span class="sxs-lookup"><span data-stu-id="7884e-135">OUTPUTS</span></span>

### <span data-ttu-id="7884e-136">Microsoft.Azure.Commands.Network.models.PSRouteServer</span><span class="sxs-lookup"><span data-stu-id="7884e-136">Microsoft.Azure.Commands.Network.Models.PSRouteServer</span></span>

## <span data-ttu-id="7884e-137">筆記</span><span class="sxs-lookup"><span data-stu-id="7884e-137">NOTES</span></span>

## <span data-ttu-id="7884e-138">相關連結</span><span class="sxs-lookup"><span data-stu-id="7884e-138">RELATED LINKS</span></span>
