---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azrouteserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzRouteServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzRouteServer.md
ms.openlocfilehash: 20021b2d557b4590a9853d3124930db27286313a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100131351"
---
# <span data-ttu-id="00bab-101">Get-AzRouteServer</span><span class="sxs-lookup"><span data-stu-id="00bab-101">Get-AzRouteServer</span></span>

## <span data-ttu-id="00bab-102">摘要</span><span class="sxs-lookup"><span data-stu-id="00bab-102">SYNOPSIS</span></span>
<span data-ttu-id="00bab-103">取得 Azure RouteServer</span><span class="sxs-lookup"><span data-stu-id="00bab-103">Get an Azure RouteServer</span></span>

## <span data-ttu-id="00bab-104">句法</span><span class="sxs-lookup"><span data-stu-id="00bab-104">SYNTAX</span></span>

### <span data-ttu-id="00bab-105">RouteServerSubscriptionIdParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="00bab-105">RouteServerSubscriptionIdParameterSet (Default)</span></span>
```
Get-AzRouteServer [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="00bab-106">RouteServerNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="00bab-106">RouteServerNameParameterSet</span></span>
```
Get-AzRouteServer -ResourceGroupName <String> [-RouteServerName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="00bab-107">RouteServerResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="00bab-107">RouteServerResourceIdParameterSet</span></span>
```
Get-AzRouteServer -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="00bab-108">說明</span><span class="sxs-lookup"><span data-stu-id="00bab-108">DESCRIPTION</span></span>
<span data-ttu-id="00bab-109">**AzRouteServer** Cmdlet 會取得 Azure RouteServer</span><span class="sxs-lookup"><span data-stu-id="00bab-109">The **Get-AzRouteServer** cmdlet gets an Azure RouteServer</span></span>

## <span data-ttu-id="00bab-110">示例</span><span class="sxs-lookup"><span data-stu-id="00bab-110">EXAMPLES</span></span>

### <span data-ttu-id="00bab-111">範例1</span><span class="sxs-lookup"><span data-stu-id="00bab-111">Example 1</span></span>
```powershell
Get-AzRouteServer -ResourceGroupName routeServerRG -RouteServerName routeServer
```

### <span data-ttu-id="00bab-112">範例2</span><span class="sxs-lookup"><span data-stu-id="00bab-112">Example 2</span></span>
```powershell
$routeServerId = '/subscriptions/8c992d64-fce9-426d-b278-85642dfeab03/resourceGroups/routeServerRG/providers/Microsoft.Network/virtualHubs/routeServer'
Get-AzRouteServer -ResourceId $routeServerId
```
## <span data-ttu-id="00bab-113">參數</span><span class="sxs-lookup"><span data-stu-id="00bab-113">PARAMETERS</span></span>

### <span data-ttu-id="00bab-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="00bab-114">-DefaultProfile</span></span>
<span data-ttu-id="00bab-115">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="00bab-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="00bab-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="00bab-116">-ResourceGroupName</span></span>
<span data-ttu-id="00bab-117">路由伺服器的資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="00bab-117">The resource group name of the route server.</span></span>

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

### <span data-ttu-id="00bab-118">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="00bab-118">-ResourceId</span></span>
<span data-ttu-id="00bab-119">路由伺服器的 ResourceId。</span><span class="sxs-lookup"><span data-stu-id="00bab-119">ResourceId of the route server.</span></span>

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

### <span data-ttu-id="00bab-120">-RouteServerName</span><span class="sxs-lookup"><span data-stu-id="00bab-120">-RouteServerName</span></span>
<span data-ttu-id="00bab-121">路由伺服器的名稱。</span><span class="sxs-lookup"><span data-stu-id="00bab-121">The name of the route server.</span></span>

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

### <span data-ttu-id="00bab-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="00bab-122">CommonParameters</span></span>
<span data-ttu-id="00bab-123">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="00bab-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="00bab-124">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="00bab-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="00bab-125">輸入</span><span class="sxs-lookup"><span data-stu-id="00bab-125">INPUTS</span></span>

### <span data-ttu-id="00bab-126">System.object</span><span class="sxs-lookup"><span data-stu-id="00bab-126">System.String</span></span>

## <span data-ttu-id="00bab-127">輸出</span><span class="sxs-lookup"><span data-stu-id="00bab-127">OUTPUTS</span></span>

### <span data-ttu-id="00bab-128">PSRouteServer 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="00bab-128">Microsoft.Azure.Commands.Network.Models.PSRouteServer</span></span>

## <span data-ttu-id="00bab-129">筆記</span><span class="sxs-lookup"><span data-stu-id="00bab-129">NOTES</span></span>

## <span data-ttu-id="00bab-130">相關連結</span><span class="sxs-lookup"><span data-stu-id="00bab-130">RELATED LINKS</span></span>
