---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-azroutefilter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzRouteFilter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzRouteFilter.md
ms.openlocfilehash: 5ae145c79012a62ae5e46c14bd649b17460f8d3c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101902445"
---
# <span data-ttu-id="274f7-101">Get-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="274f7-101">Get-AzRouteFilter</span></span>

## <span data-ttu-id="274f7-102">簡介</span><span class="sxs-lookup"><span data-stu-id="274f7-102">SYNOPSIS</span></span>
<span data-ttu-id="274f7-103">獲得路由篩選。</span><span class="sxs-lookup"><span data-stu-id="274f7-103">Gets a route filter.</span></span>

## <span data-ttu-id="274f7-104">語法</span><span class="sxs-lookup"><span data-stu-id="274f7-104">SYNTAX</span></span>

### <span data-ttu-id="274f7-105">NoExpand</span><span class="sxs-lookup"><span data-stu-id="274f7-105">NoExpand</span></span>
```
Get-AzRouteFilter [-Name <String>] [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="274f7-106">擴大</span><span class="sxs-lookup"><span data-stu-id="274f7-106">Expand</span></span>
```
Get-AzRouteFilter -Name <String> -ResourceGroupName <String> -ExpandResource <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="274f7-107">描述</span><span class="sxs-lookup"><span data-stu-id="274f7-107">DESCRIPTION</span></span>
<span data-ttu-id="274f7-108">**Get-AzRouteFilter** Cmdlet 會取得路由篩選。</span><span class="sxs-lookup"><span data-stu-id="274f7-108">The **Get-AzRouteFilter** cmdlet gets a route filter.</span></span>

## <span data-ttu-id="274f7-109">例子</span><span class="sxs-lookup"><span data-stu-id="274f7-109">EXAMPLES</span></span>

### <span data-ttu-id="274f7-110">範例 1</span><span class="sxs-lookup"><span data-stu-id="274f7-110">Example 1</span></span>
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

<span data-ttu-id="274f7-111">此命令會獲得名為 RouteFilter01 的路由篩選，該路由篩選屬於名為 ResourceGroup01 的資源群組。</span><span class="sxs-lookup"><span data-stu-id="274f7-111">This command gets the route filter named RouteFilter01 that belongs to the resource group named ResourceGroup01.</span></span>

### <span data-ttu-id="274f7-112">範例 2</span><span class="sxs-lookup"><span data-stu-id="274f7-112">Example 2</span></span>
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

<span data-ttu-id="274f7-113">此命令會獲得以「路由篩選」為開始的所有路由篩選。</span><span class="sxs-lookup"><span data-stu-id="274f7-113">This command gets all route filters that start with "RouteFilter".</span></span>

## <span data-ttu-id="274f7-114">參數</span><span class="sxs-lookup"><span data-stu-id="274f7-114">PARAMETERS</span></span>

### <span data-ttu-id="274f7-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="274f7-115">-DefaultProfile</span></span>
<span data-ttu-id="274f7-116">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="274f7-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="274f7-117">-ExpandResource</span><span class="sxs-lookup"><span data-stu-id="274f7-117">-ExpandResource</span></span>
<span data-ttu-id="274f7-118">要展開的資源參照。</span><span class="sxs-lookup"><span data-stu-id="274f7-118">The resource reference to be expanded.</span></span>

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

### <span data-ttu-id="274f7-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="274f7-119">-Name</span></span>
<span data-ttu-id="274f7-120">資源名稱。</span><span class="sxs-lookup"><span data-stu-id="274f7-120">The resource name.</span></span>

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

### <span data-ttu-id="274f7-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="274f7-121">-ResourceGroupName</span></span>
<span data-ttu-id="274f7-122">資源組名。</span><span class="sxs-lookup"><span data-stu-id="274f7-122">The resource group name.</span></span>

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

### <span data-ttu-id="274f7-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="274f7-123">CommonParameters</span></span>
<span data-ttu-id="274f7-124">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="274f7-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="274f7-125">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="274f7-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="274f7-126">輸入</span><span class="sxs-lookup"><span data-stu-id="274f7-126">INPUTS</span></span>

### <span data-ttu-id="274f7-127">System.String</span><span class="sxs-lookup"><span data-stu-id="274f7-127">System.String</span></span>

## <span data-ttu-id="274f7-128">輸出</span><span class="sxs-lookup"><span data-stu-id="274f7-128">OUTPUTS</span></span>

### <span data-ttu-id="274f7-129">Microsoft.Azure.Commands.Network.models.PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="274f7-129">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

## <span data-ttu-id="274f7-130">筆記</span><span class="sxs-lookup"><span data-stu-id="274f7-130">NOTES</span></span>

## <span data-ttu-id="274f7-131">相關連結</span><span class="sxs-lookup"><span data-stu-id="274f7-131">RELATED LINKS</span></span>

[<span data-ttu-id="274f7-132">New-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="274f7-132">New-AzRouteFilter</span></span>](./New-AzRouteFilter.md)

[<span data-ttu-id="274f7-133">Remove-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="274f7-133">Remove-AzRouteFilter</span></span>](./Remove-AzRouteFilter.md)

[<span data-ttu-id="274f7-134">Set-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="274f7-134">Set-AzRouteFilter</span></span>](./Set-AzRouteFilter.md)

[<span data-ttu-id="274f7-135">Add-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="274f7-135">Add-AzRouteFilterRuleConfig</span></span>](./Add-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="274f7-136">Get-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="274f7-136">Get-AzRouteFilterRuleConfig</span></span>](./Get-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="274f7-137">New-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="274f7-137">New-AzRouteFilterRuleConfig</span></span>](./New-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="274f7-138">Remove-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="274f7-138">Remove-AzRouteFilterRuleConfig</span></span>](./Remove-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="274f7-139">Set-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="274f7-139">Set-AzRouteFilterRuleConfig</span></span>](./Set-AzRouteFilterRuleConfig.md)
