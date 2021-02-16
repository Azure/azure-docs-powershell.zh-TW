---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/update-azrouteserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzRouteServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzRouteServer.md
ms.openlocfilehash: 9f00ccfb01cd6e6b0d80b120364f8ac0c81daae0
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100131079"
---
# <span data-ttu-id="1a010-101">Update-AzRouteServer</span><span class="sxs-lookup"><span data-stu-id="1a010-101">Update-AzRouteServer</span></span>

## <span data-ttu-id="1a010-102">摘要</span><span class="sxs-lookup"><span data-stu-id="1a010-102">SYNOPSIS</span></span>
<span data-ttu-id="1a010-103">更新 Azure RouteServer。</span><span class="sxs-lookup"><span data-stu-id="1a010-103">Update an Azure RouteServer.</span></span>

## <span data-ttu-id="1a010-104">句法</span><span class="sxs-lookup"><span data-stu-id="1a010-104">SYNTAX</span></span>

### <span data-ttu-id="1a010-105">RouteServerNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="1a010-105">RouteServerNameParameterSet (Default)</span></span>
```
Update-AzRouteServer -ResourceGroupName <String> -RouteServerName <String> [-AllowBranchToBranchTraffic]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1a010-106">RouteServerResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="1a010-106">RouteServerResourceIdParameterSet</span></span>
```
Update-AzRouteServer [-AllowBranchToBranchTraffic] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1a010-107">說明</span><span class="sxs-lookup"><span data-stu-id="1a010-107">DESCRIPTION</span></span>
<span data-ttu-id="1a010-108">**AzRouteServer** Cmdlet 會將分支對分支流量切換至 Azure RouteServer。</span><span class="sxs-lookup"><span data-stu-id="1a010-108">The **Update-AzRouteServer** cmdlet switches the branch-to-branch traffic to an Azure RouteServer.</span></span>

## <span data-ttu-id="1a010-109">示例</span><span class="sxs-lookup"><span data-stu-id="1a010-109">EXAMPLES</span></span>

### <span data-ttu-id="1a010-110">範例1</span><span class="sxs-lookup"><span data-stu-id="1a010-110">Example 1</span></span>
```powershell
PS C:\>  Update-AzRouteServer -ResourceGroupName $rgname -RouteServerName $routeServerName -AllowBranchToBranchTraffic
```
<span data-ttu-id="1a010-111">啟用分支以分支路由伺服器的流量。</span><span class="sxs-lookup"><span data-stu-id="1a010-111">To enable branch to branch traffic for route server.</span></span>

### <span data-ttu-id="1a010-112">範例1</span><span class="sxs-lookup"><span data-stu-id="1a010-112">Example 1</span></span>
```powershell
PS C:\>  Update-AzRouteServer -ResourceGroupName $rgname -RouteServerName $routeServerName
```
<span data-ttu-id="1a010-113">若要停用分支來分支路由伺服器的通信量。</span><span class="sxs-lookup"><span data-stu-id="1a010-113">To disable branch to branch traffic for route server.</span></span>

## <span data-ttu-id="1a010-114">參數</span><span class="sxs-lookup"><span data-stu-id="1a010-114">PARAMETERS</span></span>

### <span data-ttu-id="1a010-115">-AllowBranchToBranchTraffic</span><span class="sxs-lookup"><span data-stu-id="1a010-115">-AllowBranchToBranchTraffic</span></span>
<span data-ttu-id="1a010-116">[旗標] 可讓分支對路由伺服器的流量進行分支。</span><span class="sxs-lookup"><span data-stu-id="1a010-116">Flag to allow branch to branch traffic for route server.</span></span>

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

### <span data-ttu-id="1a010-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1a010-117">-DefaultProfile</span></span>
<span data-ttu-id="1a010-118">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="1a010-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1a010-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1a010-119">-ResourceGroupName</span></span>
<span data-ttu-id="1a010-120">路由伺服器的資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="1a010-120">The resource group name of the route server.</span></span>

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

### <span data-ttu-id="1a010-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1a010-121">-ResourceId</span></span>
<span data-ttu-id="1a010-122">路由伺服器的 ResourceId。</span><span class="sxs-lookup"><span data-stu-id="1a010-122">ResourceId of the route server.</span></span>

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

### <span data-ttu-id="1a010-123">-RouteServerName</span><span class="sxs-lookup"><span data-stu-id="1a010-123">-RouteServerName</span></span>
<span data-ttu-id="1a010-124">路由伺服器的名稱。</span><span class="sxs-lookup"><span data-stu-id="1a010-124">The name of the route server.</span></span>

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

### <span data-ttu-id="1a010-125">-確認</span><span class="sxs-lookup"><span data-stu-id="1a010-125">-Confirm</span></span>
<span data-ttu-id="1a010-126">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="1a010-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1a010-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1a010-127">-WhatIf</span></span>
<span data-ttu-id="1a010-128">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="1a010-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1a010-129">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="1a010-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1a010-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1a010-130">CommonParameters</span></span>
<span data-ttu-id="1a010-131">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="1a010-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1a010-132">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="1a010-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1a010-133">輸入</span><span class="sxs-lookup"><span data-stu-id="1a010-133">INPUTS</span></span>

### <span data-ttu-id="1a010-134">System.object</span><span class="sxs-lookup"><span data-stu-id="1a010-134">System.String</span></span>

## <span data-ttu-id="1a010-135">輸出</span><span class="sxs-lookup"><span data-stu-id="1a010-135">OUTPUTS</span></span>

### <span data-ttu-id="1a010-136">PSRouteServer 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="1a010-136">Microsoft.Azure.Commands.Network.Models.PSRouteServer</span></span>

## <span data-ttu-id="1a010-137">筆記</span><span class="sxs-lookup"><span data-stu-id="1a010-137">NOTES</span></span>

## <span data-ttu-id="1a010-138">相關連結</span><span class="sxs-lookup"><span data-stu-id="1a010-138">RELATED LINKS</span></span>
