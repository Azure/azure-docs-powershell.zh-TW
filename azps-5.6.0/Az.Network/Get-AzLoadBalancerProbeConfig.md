---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 278228EB-0126-4F27-A30F-51DC498C65FE
online version: https://docs.microsoft.com/powershell/module/az.network/get-azloadbalancerprobeconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzLoadBalancerProbeConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzLoadBalancerProbeConfig.md
ms.openlocfilehash: 43c3b4d17d024eaae06c7d7f891dfd2ea3e08aa9
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101916069"
---
# <span data-ttu-id="27051-101">Get-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="27051-101">Get-AzLoadBalancerProbeConfig</span></span>

## <span data-ttu-id="27051-102">簡介</span><span class="sxs-lookup"><span data-stu-id="27051-102">SYNOPSIS</span></span>
<span data-ttu-id="27051-103">取得負載平衡器的配置。</span><span class="sxs-lookup"><span data-stu-id="27051-103">Gets a probe configuration for a load balancer.</span></span>

## <span data-ttu-id="27051-104">語法</span><span class="sxs-lookup"><span data-stu-id="27051-104">SYNTAX</span></span>

```
Get-AzLoadBalancerProbeConfig -LoadBalancer <PSLoadBalancer> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="27051-105">描述</span><span class="sxs-lookup"><span data-stu-id="27051-105">DESCRIPTION</span></span>
<span data-ttu-id="27051-106">**Get-AzLoadBalancerProbeConfig** Cmdlet 會針對負載平衡器取得一或多個配置配置。</span><span class="sxs-lookup"><span data-stu-id="27051-106">The **Get-AzLoadBalancerProbeConfig** cmdlet gets one or more probe configurations for a load balancer.</span></span>

## <span data-ttu-id="27051-107">例子</span><span class="sxs-lookup"><span data-stu-id="27051-107">EXAMPLES</span></span>

### <span data-ttu-id="27051-108">範例 1：取得負載平衡器的配置</span><span class="sxs-lookup"><span data-stu-id="27051-108">Example 1: Get the probe configuration of a load balancer</span></span>
```
PS C:\>$slb = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> Get-AzLoadBalancerProbeConfig -Name "MyProbe" -LoadBalancer $slb
```

<span data-ttu-id="27051-109">第一個命令會取得名為 MyLoadBalancer 的負載平衡器，然後將它儲存在變數 $slb。</span><span class="sxs-lookup"><span data-stu-id="27051-109">The first command gets the load balancer named MyLoadBalancer, and then stores it in the variable $slb.</span></span>
<span data-ttu-id="27051-110">第二個命令會從 $slb 中的負載平衡器取得名為 MyProbe 的關聯$slb。</span><span class="sxs-lookup"><span data-stu-id="27051-110">The second command gets the associated probe configuration named MyProbe from the load balancer in $slb.</span></span>

## <span data-ttu-id="27051-111">參數</span><span class="sxs-lookup"><span data-stu-id="27051-111">PARAMETERS</span></span>

### <span data-ttu-id="27051-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="27051-112">-DefaultProfile</span></span>
<span data-ttu-id="27051-113">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="27051-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="27051-114">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="27051-114">-LoadBalancer</span></span>
<span data-ttu-id="27051-115">指定與要取得之安裝配置相關聯的負載平衡器。</span><span class="sxs-lookup"><span data-stu-id="27051-115">Specifies the load balancer that is associated with the probe configuration to get.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSLoadBalancer
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="27051-116">-名稱</span><span class="sxs-lookup"><span data-stu-id="27051-116">-Name</span></span>
<span data-ttu-id="27051-117">指定要取得的群組原則組名。</span><span class="sxs-lookup"><span data-stu-id="27051-117">Specifies the name of the probe configuration to get.</span></span>

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

### <span data-ttu-id="27051-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="27051-118">CommonParameters</span></span>
<span data-ttu-id="27051-119">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="27051-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="27051-120">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="27051-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="27051-121">輸入</span><span class="sxs-lookup"><span data-stu-id="27051-121">INPUTS</span></span>

### <span data-ttu-id="27051-122">Microsoft.Azure.Commands.Network.models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="27051-122">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="27051-123">輸出</span><span class="sxs-lookup"><span data-stu-id="27051-123">OUTPUTS</span></span>

### <span data-ttu-id="27051-124">Microsoft.Azure.Commands.Network.models.PSProbe</span><span class="sxs-lookup"><span data-stu-id="27051-124">Microsoft.Azure.Commands.Network.Models.PSProbe</span></span>

## <span data-ttu-id="27051-125">筆記</span><span class="sxs-lookup"><span data-stu-id="27051-125">NOTES</span></span>

## <span data-ttu-id="27051-126">相關連結</span><span class="sxs-lookup"><span data-stu-id="27051-126">RELATED LINKS</span></span>

[<span data-ttu-id="27051-127">Add-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="27051-127">Add-AzLoadBalancerProbeConfig</span></span>](./Add-AzLoadBalancerProbeConfig.md)

[<span data-ttu-id="27051-128">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="27051-128">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="27051-129">New-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="27051-129">New-AzLoadBalancerProbeConfig</span></span>](./New-AzLoadBalancerProbeConfig.md)

[<span data-ttu-id="27051-130">Remove-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="27051-130">Remove-AzLoadBalancerProbeConfig</span></span>](./Remove-AzLoadBalancerProbeConfig.md)

[<span data-ttu-id="27051-131">Set-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="27051-131">Set-AzLoadBalancerProbeConfig</span></span>](./Set-AzLoadBalancerProbeConfig.md)


