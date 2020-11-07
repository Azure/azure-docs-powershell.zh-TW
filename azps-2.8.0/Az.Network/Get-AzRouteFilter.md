---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azroutefilter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzRouteFilter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzRouteFilter.md
ms.openlocfilehash: 26fb3e9a7b4b097e79fdb328d79a82fc423ac675
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93790046"
---
# <span data-ttu-id="4795f-101">Get-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="4795f-101">Get-AzRouteFilter</span></span>

## <span data-ttu-id="4795f-102">摘要</span><span class="sxs-lookup"><span data-stu-id="4795f-102">SYNOPSIS</span></span>
<span data-ttu-id="4795f-103">取得路由篩選器。</span><span class="sxs-lookup"><span data-stu-id="4795f-103">Gets a route filter.</span></span>

## <span data-ttu-id="4795f-104">句法</span><span class="sxs-lookup"><span data-stu-id="4795f-104">SYNTAX</span></span>

### <span data-ttu-id="4795f-105">NoExpand</span><span class="sxs-lookup"><span data-stu-id="4795f-105">NoExpand</span></span>
```
Get-AzRouteFilter [-Name <String>] [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="4795f-106">擴充</span><span class="sxs-lookup"><span data-stu-id="4795f-106">Expand</span></span>
```
Get-AzRouteFilter -Name <String> -ResourceGroupName <String> -ExpandResource <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4795f-107">說明</span><span class="sxs-lookup"><span data-stu-id="4795f-107">DESCRIPTION</span></span>
<span data-ttu-id="4795f-108">**AzRouteFilter** Cmdlet 會取得路由篩選器。</span><span class="sxs-lookup"><span data-stu-id="4795f-108">The **Get-AzRouteFilter** cmdlet gets a route filter.</span></span>

## <span data-ttu-id="4795f-109">示例</span><span class="sxs-lookup"><span data-stu-id="4795f-109">EXAMPLES</span></span>

### <span data-ttu-id="4795f-110">範例1</span><span class="sxs-lookup"><span data-stu-id="4795f-110">Example 1</span></span>
```powershell
PS C:\> Get-AzRouteFilter -Name "RouteFilter01" -ResourceGroupName "ResourceGroup01"

Name              : RouteFilter01
ResourceGroupName : ResourceGroup01
Location          : westus
Id                : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsof
                    t.Network/routeFilters/RouteFilter01
Etag              : W/"00000000-0000-0000-0000-000000000000"
ProvisioningState : Succeeded
Tags              :
Rules             : []
Peerings          : []
```

<span data-ttu-id="4795f-111">這個命令會取得屬於名為 ResourceGroup01 之資源群組的名為 RouteFilter01 的路由篩選器。</span><span class="sxs-lookup"><span data-stu-id="4795f-111">This command gets the route filter named RouteFilter01 that belongs to the resource group named ResourceGroup01.</span></span>

### <span data-ttu-id="4795f-112">範例2</span><span class="sxs-lookup"><span data-stu-id="4795f-112">Example 2</span></span>
```powershell
PS C:\> Get-AzRouteFilter -Name "RouteFilter*"

Name              : RouteFilter01
ResourceGroupName : ResourceGroup01
Location          : westus
Id                : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsof
                    t.Network/routeFilters/RouteFilter01
Etag              : W/"00000000-0000-0000-0000-000000000000"
ProvisioningState : Succeeded
Tags              :
Rules             : []
Peerings          : []

Name              : RouteFilter02
ResourceGroupName : ResourceGroup01
Location          : westus
Id                : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsof
                    t.Network/routeFilters/RouteFilter02
Etag              : W/"00000000-0000-0000-0000-000000000000"
ProvisioningState : Succeeded
Tags              :
Rules             : []
Peerings          : []
```

<span data-ttu-id="4795f-113">這個命令會取得以 "RouteFilter" 為開頭的所有路由篩選器。</span><span class="sxs-lookup"><span data-stu-id="4795f-113">This command gets all route filters that start with "RouteFilter".</span></span>

## <span data-ttu-id="4795f-114">參數</span><span class="sxs-lookup"><span data-stu-id="4795f-114">PARAMETERS</span></span>

### <span data-ttu-id="4795f-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4795f-115">-DefaultProfile</span></span>
<span data-ttu-id="4795f-116">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="4795f-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4795f-117">-ExpandResource</span><span class="sxs-lookup"><span data-stu-id="4795f-117">-ExpandResource</span></span>
<span data-ttu-id="4795f-118">要展開的資源參照。</span><span class="sxs-lookup"><span data-stu-id="4795f-118">The resource reference to be expanded.</span></span>

```yaml
Type: System.String
Parameter Sets: Expand
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4795f-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="4795f-119">-Name</span></span>
<span data-ttu-id="4795f-120">資源名稱。</span><span class="sxs-lookup"><span data-stu-id="4795f-120">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: NoExpand
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

```yaml
Type: System.String
Parameter Sets: Expand
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="4795f-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4795f-121">-ResourceGroupName</span></span>
<span data-ttu-id="4795f-122">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="4795f-122">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: NoExpand
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

```yaml
Type: System.String
Parameter Sets: Expand
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="4795f-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4795f-123">CommonParameters</span></span>
<span data-ttu-id="4795f-124">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="4795f-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4795f-125">如需詳細資訊，請參閱 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="4795f-125">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4795f-126">輸入</span><span class="sxs-lookup"><span data-stu-id="4795f-126">INPUTS</span></span>

### <span data-ttu-id="4795f-127">System.object</span><span class="sxs-lookup"><span data-stu-id="4795f-127">System.String</span></span>

## <span data-ttu-id="4795f-128">輸出</span><span class="sxs-lookup"><span data-stu-id="4795f-128">OUTPUTS</span></span>

### <span data-ttu-id="4795f-129">PSRouteFilter 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="4795f-129">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

## <span data-ttu-id="4795f-130">筆記</span><span class="sxs-lookup"><span data-stu-id="4795f-130">NOTES</span></span>

## <span data-ttu-id="4795f-131">相關連結</span><span class="sxs-lookup"><span data-stu-id="4795f-131">RELATED LINKS</span></span>

[<span data-ttu-id="4795f-132">新-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="4795f-132">New-AzRouteFilter</span></span>](./New-AzRouteFilter.md)

[<span data-ttu-id="4795f-133">移除-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="4795f-133">Remove-AzRouteFilter</span></span>](./Remove-AzRouteFilter.md)

[<span data-ttu-id="4795f-134">Set-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="4795f-134">Set-AzRouteFilter</span></span>](./Set-AzRouteFilter.md)

[<span data-ttu-id="4795f-135">附加 AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="4795f-135">Add-AzRouteFilterRuleConfig</span></span>](./Add-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="4795f-136">AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="4795f-136">Get-AzRouteFilterRuleConfig</span></span>](./Get-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="4795f-137">新-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="4795f-137">New-AzRouteFilterRuleConfig</span></span>](./New-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="4795f-138">移除-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="4795f-138">Remove-AzRouteFilterRuleConfig</span></span>](./Remove-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="4795f-139">Set-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="4795f-139">Set-AzRouteFilterRuleConfig</span></span>](./Set-AzRouteFilterRuleConfig.md)
