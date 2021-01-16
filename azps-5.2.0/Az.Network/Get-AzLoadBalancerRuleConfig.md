---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: B2CF11FC-520C-4C14-9A1B-13F06B250B5D
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azloadbalancerruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzLoadBalancerRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzLoadBalancerRuleConfig.md
ms.openlocfilehash: 87329e4864e4fd91d1a8aec09183fe02d8c498ff
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98279042"
---
# <span data-ttu-id="131ad-101">Get-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="131ad-101">Get-AzLoadBalancerRuleConfig</span></span>

## <span data-ttu-id="131ad-102">摘要</span><span class="sxs-lookup"><span data-stu-id="131ad-102">SYNOPSIS</span></span>
<span data-ttu-id="131ad-103">取得負載平衡器的規則配置。</span><span class="sxs-lookup"><span data-stu-id="131ad-103">Gets the rule configuration for a load balancer.</span></span>

## <span data-ttu-id="131ad-104">句法</span><span class="sxs-lookup"><span data-stu-id="131ad-104">SYNTAX</span></span>

```
Get-AzLoadBalancerRuleConfig -LoadBalancer <PSLoadBalancer> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="131ad-105">說明</span><span class="sxs-lookup"><span data-stu-id="131ad-105">DESCRIPTION</span></span>
<span data-ttu-id="131ad-106">**AzLoadBalancerRuleConfig** Cmdlet 會取得一或多個負載平衡器的規則設定。</span><span class="sxs-lookup"><span data-stu-id="131ad-106">The **Get-AzLoadBalancerRuleConfig** cmdlet gets one or more rule configurations for a load balancer.</span></span>

## <span data-ttu-id="131ad-107">示例</span><span class="sxs-lookup"><span data-stu-id="131ad-107">EXAMPLES</span></span>

### <span data-ttu-id="131ad-108">範例1：取得負載平衡器的規則設定</span><span class="sxs-lookup"><span data-stu-id="131ad-108">Example 1: Get the rule configuration of a load balancer</span></span>
```
PS C:\>$slb = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> Get-AzLoadBalancerRuleConfig -Name "MyLBrulename" -LoadBalancer $slb
```

<span data-ttu-id="131ad-109">第一個命令會取得名為 MyLoadBalancer 的負載平衡器，然後將它儲存在 $slb 的變數中。</span><span class="sxs-lookup"><span data-stu-id="131ad-109">The first command gets the load balancer named MyLoadBalancer, and then stores it in the variable $slb.</span></span>
<span data-ttu-id="131ad-110">第二個命令會從 $slb 中的負載平衡器取得名為 MyLBrulename 的相關規則配置。</span><span class="sxs-lookup"><span data-stu-id="131ad-110">The second command gets the associated rule configuration named MyLBrulename from the load balancer in $slb.</span></span>

## <span data-ttu-id="131ad-111">參數</span><span class="sxs-lookup"><span data-stu-id="131ad-111">PARAMETERS</span></span>

### <span data-ttu-id="131ad-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="131ad-112">-DefaultProfile</span></span>
<span data-ttu-id="131ad-113">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="131ad-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="131ad-114">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="131ad-114">-LoadBalancer</span></span>
<span data-ttu-id="131ad-115">指定與要取得之規則配置相關聯的負載平衡器。</span><span class="sxs-lookup"><span data-stu-id="131ad-115">Specifies the load balancer that is associated with the rule configuration to get.</span></span>

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

### <span data-ttu-id="131ad-116">-名稱</span><span class="sxs-lookup"><span data-stu-id="131ad-116">-Name</span></span>
<span data-ttu-id="131ad-117">指定要取得的規則配置名稱。</span><span class="sxs-lookup"><span data-stu-id="131ad-117">Specifies the name of the rule configuration to get.</span></span>

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

### <span data-ttu-id="131ad-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="131ad-118">CommonParameters</span></span>
<span data-ttu-id="131ad-119">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="131ad-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="131ad-120">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="131ad-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="131ad-121">輸入</span><span class="sxs-lookup"><span data-stu-id="131ad-121">INPUTS</span></span>

### <span data-ttu-id="131ad-122">PSLoadBalancer 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="131ad-122">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="131ad-123">輸出</span><span class="sxs-lookup"><span data-stu-id="131ad-123">OUTPUTS</span></span>

### <span data-ttu-id="131ad-124">PSLoadBalancingRule 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="131ad-124">Microsoft.Azure.Commands.Network.Models.PSLoadBalancingRule</span></span>

## <span data-ttu-id="131ad-125">筆記</span><span class="sxs-lookup"><span data-stu-id="131ad-125">NOTES</span></span>

## <span data-ttu-id="131ad-126">相關連結</span><span class="sxs-lookup"><span data-stu-id="131ad-126">RELATED LINKS</span></span>

[<span data-ttu-id="131ad-127">附加 AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="131ad-127">Add-AzLoadBalancerRuleConfig</span></span>](./Add-AzLoadBalancerRuleConfig.md)

[<span data-ttu-id="131ad-128">AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="131ad-128">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="131ad-129">移除-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="131ad-129">Remove-AzLoadBalancerRuleConfig</span></span>](./Remove-AzLoadBalancerRuleConfig.md)

[<span data-ttu-id="131ad-130">Set-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="131ad-130">Set-AzLoadBalancerRuleConfig</span></span>](./Set-AzLoadBalancerRuleConfig.md)


