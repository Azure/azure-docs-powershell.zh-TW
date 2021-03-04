---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: B2CF11FC-520C-4C14-9A1B-13F06B250B5D
online version: https://docs.microsoft.com/powershell/module/az.network/get-azloadbalancerruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzLoadBalancerRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzLoadBalancerRuleConfig.md
ms.openlocfilehash: d5782ea85a97df723967d73cf2716d837477f01d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101916061"
---
# <span data-ttu-id="dafaa-101">Get-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="dafaa-101">Get-AzLoadBalancerRuleConfig</span></span>

## <span data-ttu-id="dafaa-102">簡介</span><span class="sxs-lookup"><span data-stu-id="dafaa-102">SYNOPSIS</span></span>
<span data-ttu-id="dafaa-103">取得負載平衡器的規則組。</span><span class="sxs-lookup"><span data-stu-id="dafaa-103">Gets the rule configuration for a load balancer.</span></span>

## <span data-ttu-id="dafaa-104">語法</span><span class="sxs-lookup"><span data-stu-id="dafaa-104">SYNTAX</span></span>

```
Get-AzLoadBalancerRuleConfig -LoadBalancer <PSLoadBalancer> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="dafaa-105">描述</span><span class="sxs-lookup"><span data-stu-id="dafaa-105">DESCRIPTION</span></span>
<span data-ttu-id="dafaa-106">**Get-AzLoadBalancerRuleConfig** Cmdlet 會針對負載平衡器取得一或多個規則組式。</span><span class="sxs-lookup"><span data-stu-id="dafaa-106">The **Get-AzLoadBalancerRuleConfig** cmdlet gets one or more rule configurations for a load balancer.</span></span>

## <span data-ttu-id="dafaa-107">例子</span><span class="sxs-lookup"><span data-stu-id="dafaa-107">EXAMPLES</span></span>

### <span data-ttu-id="dafaa-108">範例 1：取得負載平衡器的規則組</span><span class="sxs-lookup"><span data-stu-id="dafaa-108">Example 1: Get the rule configuration of a load balancer</span></span>
```
PS C:\>$slb = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> Get-AzLoadBalancerRuleConfig -Name "MyLBrulename" -LoadBalancer $slb
```

<span data-ttu-id="dafaa-109">第一個命令會取得名為 MyLoadBalancer 的負載平衡器，然後將它儲存在變數 $slb。</span><span class="sxs-lookup"><span data-stu-id="dafaa-109">The first command gets the load balancer named MyLoadBalancer, and then stores it in the variable $slb.</span></span>
<span data-ttu-id="dafaa-110">第二個命令會從 $slb 中的負載平衡器取得名為 MyLBrulename 的關聯規則$slb。</span><span class="sxs-lookup"><span data-stu-id="dafaa-110">The second command gets the associated rule configuration named MyLBrulename from the load balancer in $slb.</span></span>

## <span data-ttu-id="dafaa-111">參數</span><span class="sxs-lookup"><span data-stu-id="dafaa-111">PARAMETERS</span></span>

### <span data-ttu-id="dafaa-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dafaa-112">-DefaultProfile</span></span>
<span data-ttu-id="dafaa-113">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="dafaa-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dafaa-114">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="dafaa-114">-LoadBalancer</span></span>
<span data-ttu-id="dafaa-115">指定與要取得規則組配置的負載平衡器。</span><span class="sxs-lookup"><span data-stu-id="dafaa-115">Specifies the load balancer that is associated with the rule configuration to get.</span></span>

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

### <span data-ttu-id="dafaa-116">-名稱</span><span class="sxs-lookup"><span data-stu-id="dafaa-116">-Name</span></span>
<span data-ttu-id="dafaa-117">指定要取得的規則組名。</span><span class="sxs-lookup"><span data-stu-id="dafaa-117">Specifies the name of the rule configuration to get.</span></span>

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

### <span data-ttu-id="dafaa-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dafaa-118">CommonParameters</span></span>
<span data-ttu-id="dafaa-119">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="dafaa-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dafaa-120">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="dafaa-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dafaa-121">輸入</span><span class="sxs-lookup"><span data-stu-id="dafaa-121">INPUTS</span></span>

### <span data-ttu-id="dafaa-122">Microsoft.Azure.Commands.Network.models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="dafaa-122">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="dafaa-123">輸出</span><span class="sxs-lookup"><span data-stu-id="dafaa-123">OUTPUTS</span></span>

### <span data-ttu-id="dafaa-124">Microsoft.Azure.Commands.Network.models.PSLoadBalrule</span><span class="sxs-lookup"><span data-stu-id="dafaa-124">Microsoft.Azure.Commands.Network.Models.PSLoadBalancingRule</span></span>

## <span data-ttu-id="dafaa-125">筆記</span><span class="sxs-lookup"><span data-stu-id="dafaa-125">NOTES</span></span>

## <span data-ttu-id="dafaa-126">相關連結</span><span class="sxs-lookup"><span data-stu-id="dafaa-126">RELATED LINKS</span></span>

[<span data-ttu-id="dafaa-127">Add-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="dafaa-127">Add-AzLoadBalancerRuleConfig</span></span>](./Add-AzLoadBalancerRuleConfig.md)

[<span data-ttu-id="dafaa-128">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="dafaa-128">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="dafaa-129">Remove-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="dafaa-129">Remove-AzLoadBalancerRuleConfig</span></span>](./Remove-AzLoadBalancerRuleConfig.md)

[<span data-ttu-id="dafaa-130">Set-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="dafaa-130">Set-AzLoadBalancerRuleConfig</span></span>](./Set-AzLoadBalancerRuleConfig.md)


