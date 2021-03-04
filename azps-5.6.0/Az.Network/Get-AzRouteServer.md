---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-azrouteserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzRouteServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzRouteServer.md
ms.openlocfilehash: ef5609a34104ca8502b8e4ce96fe294a4714366d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101902438"
---
# <span data-ttu-id="e8e30-101">Get-AzRouteServer</span><span class="sxs-lookup"><span data-stu-id="e8e30-101">Get-AzRouteServer</span></span>

## <span data-ttu-id="e8e30-102">簡介</span><span class="sxs-lookup"><span data-stu-id="e8e30-102">SYNOPSIS</span></span>
<span data-ttu-id="e8e30-103">取得 Azure RouteServer</span><span class="sxs-lookup"><span data-stu-id="e8e30-103">Get an Azure RouteServer</span></span>

## <span data-ttu-id="e8e30-104">語法</span><span class="sxs-lookup"><span data-stu-id="e8e30-104">SYNTAX</span></span>

### <span data-ttu-id="e8e30-105">RouteServerSubscriptionIdParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="e8e30-105">RouteServerSubscriptionIdParameterSet (Default)</span></span>
```
Get-AzRouteServer [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e8e30-106">RouteServerNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="e8e30-106">RouteServerNameParameterSet</span></span>
```
Get-AzRouteServer -ResourceGroupName <String> [-RouteServerName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e8e30-107">RouteServerResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e8e30-107">RouteServerResourceIdParameterSet</span></span>
```
Get-AzRouteServer -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e8e30-108">描述</span><span class="sxs-lookup"><span data-stu-id="e8e30-108">DESCRIPTION</span></span>
<span data-ttu-id="e8e30-109">**Get-AzRouteServer** Cmdlet 取得 Azure RouteServer</span><span class="sxs-lookup"><span data-stu-id="e8e30-109">The **Get-AzRouteServer** cmdlet gets an Azure RouteServer</span></span>

## <span data-ttu-id="e8e30-110">例子</span><span class="sxs-lookup"><span data-stu-id="e8e30-110">EXAMPLES</span></span>

### <span data-ttu-id="e8e30-111">範例 1</span><span class="sxs-lookup"><span data-stu-id="e8e30-111">Example 1</span></span>
```powershell
Get-AzRouteServer -ResourceGroupName routeServerRG -RouteServerName routeServer
```

### <span data-ttu-id="e8e30-112">範例 2</span><span class="sxs-lookup"><span data-stu-id="e8e30-112">Example 2</span></span>
```powershell
$routeServerId = '/subscriptions/8c992d64-fce9-426d-b278-85642dfeab03/resourceGroups/routeServerRG/providers/Microsoft.Network/virtualHubs/routeServer'
Get-AzRouteServer -ResourceId $routeServerId
```
## <span data-ttu-id="e8e30-113">參數</span><span class="sxs-lookup"><span data-stu-id="e8e30-113">PARAMETERS</span></span>

### <span data-ttu-id="e8e30-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e8e30-114">-DefaultProfile</span></span>
<span data-ttu-id="e8e30-115">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="e8e30-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e8e30-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e8e30-116">-ResourceGroupName</span></span>
<span data-ttu-id="e8e30-117">路由伺服器的資源組名。</span><span class="sxs-lookup"><span data-stu-id="e8e30-117">The resource group name of the route server.</span></span>

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

### <span data-ttu-id="e8e30-118">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e8e30-118">-ResourceId</span></span>
<span data-ttu-id="e8e30-119">路由伺服器的 ResourceId。</span><span class="sxs-lookup"><span data-stu-id="e8e30-119">ResourceId of the route server.</span></span>

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

### <span data-ttu-id="e8e30-120">-RouteServerName</span><span class="sxs-lookup"><span data-stu-id="e8e30-120">-RouteServerName</span></span>
<span data-ttu-id="e8e30-121">路由伺服器的名稱。</span><span class="sxs-lookup"><span data-stu-id="e8e30-121">The name of the route server.</span></span>

```yaml
Type: System.String
Parameter Sets: RouteServerNameParameterSet
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e8e30-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e8e30-122">CommonParameters</span></span>
<span data-ttu-id="e8e30-123">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="e8e30-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e8e30-124">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e8e30-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e8e30-125">輸入</span><span class="sxs-lookup"><span data-stu-id="e8e30-125">INPUTS</span></span>

### <span data-ttu-id="e8e30-126">System.String</span><span class="sxs-lookup"><span data-stu-id="e8e30-126">System.String</span></span>

## <span data-ttu-id="e8e30-127">輸出</span><span class="sxs-lookup"><span data-stu-id="e8e30-127">OUTPUTS</span></span>

### <span data-ttu-id="e8e30-128">Microsoft.Azure.Commands.Network.models.PSRouteServer</span><span class="sxs-lookup"><span data-stu-id="e8e30-128">Microsoft.Azure.Commands.Network.Models.PSRouteServer</span></span>

## <span data-ttu-id="e8e30-129">筆記</span><span class="sxs-lookup"><span data-stu-id="e8e30-129">NOTES</span></span>

## <span data-ttu-id="e8e30-130">相關連結</span><span class="sxs-lookup"><span data-stu-id="e8e30-130">RELATED LINKS</span></span>
