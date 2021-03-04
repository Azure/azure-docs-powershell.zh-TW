---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-azloadbalanceroutboundruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzLoadBalancerOutboundRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzLoadBalancerOutboundRuleConfig.md
ms.openlocfilehash: fc3b34e2fb9f91684aee2427d4271e6fab08843f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101916066"
---
# <span data-ttu-id="2ee13-101">Get-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="2ee13-101">Get-AzLoadBalancerOutboundRuleConfig</span></span>

## <span data-ttu-id="2ee13-102">簡介</span><span class="sxs-lookup"><span data-stu-id="2ee13-102">SYNOPSIS</span></span>
<span data-ttu-id="2ee13-103">取得負載平衡器中的外發規則組式。</span><span class="sxs-lookup"><span data-stu-id="2ee13-103">Gets an outbound rule configuration in a load balancer.</span></span>

## <span data-ttu-id="2ee13-104">語法</span><span class="sxs-lookup"><span data-stu-id="2ee13-104">SYNTAX</span></span>

```
Get-AzLoadBalancerOutboundRuleConfig -LoadBalancer <PSLoadBalancer> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2ee13-105">描述</span><span class="sxs-lookup"><span data-stu-id="2ee13-105">DESCRIPTION</span></span>
<span data-ttu-id="2ee13-106">**Get-AzLoadBalancerOutboundRuleConfig** Cmdlet 會取得輸出規則組式，或負載平衡器中的輸出規則組式清單。</span><span class="sxs-lookup"><span data-stu-id="2ee13-106">The **Get-AzLoadBalancerOutboundRuleConfig** cmdlet gets an outbound rule configuration or a list of outbound rule configurations in a load balancer.</span></span>

## <span data-ttu-id="2ee13-107">例子</span><span class="sxs-lookup"><span data-stu-id="2ee13-107">EXAMPLES</span></span>

### <span data-ttu-id="2ee13-108">範例 1：在負載平衡器中取得外發規則組式</span><span class="sxs-lookup"><span data-stu-id="2ee13-108">Example 1: Get an outbound rule configuration in a load balancer</span></span>
```powershell
PS C:\>$slb = Get-AzLoadBalancer -ResourceGroupName "MyResourceGroup" -Name "MyLoadBalancer"
PS C:\>Get-AzLoadBalancerOutboundRuleConfig -LoadBalancer $slb -Name "MyRule"
```

<span data-ttu-id="2ee13-109">第一個命令會取得名為 MyLoadBalancer 的負載平衡器，然後將它儲存在變數 $slb。</span><span class="sxs-lookup"><span data-stu-id="2ee13-109">The first command gets the load balancer named MyLoadBalancer, and then stores it in the variable $slb.</span></span>
<span data-ttu-id="2ee13-110">第二個命令會取得名為 MyRule 的外發規則組式，該規則組與負載平衡器相關聯。</span><span class="sxs-lookup"><span data-stu-id="2ee13-110">The second command gets the outbound rule configuration named MyRule associated with that load balancer.</span></span>

## <span data-ttu-id="2ee13-111">參數</span><span class="sxs-lookup"><span data-stu-id="2ee13-111">PARAMETERS</span></span>

### <span data-ttu-id="2ee13-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2ee13-112">-DefaultProfile</span></span>
<span data-ttu-id="2ee13-113">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="2ee13-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2ee13-114">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="2ee13-114">-LoadBalancer</span></span>
<span data-ttu-id="2ee13-115">負載平衡器資源的參照。</span><span class="sxs-lookup"><span data-stu-id="2ee13-115">The reference of the load balancer resource.</span></span>

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

### <span data-ttu-id="2ee13-116">-名稱</span><span class="sxs-lookup"><span data-stu-id="2ee13-116">-Name</span></span>
<span data-ttu-id="2ee13-117">外發規則的名稱。</span><span class="sxs-lookup"><span data-stu-id="2ee13-117">Name of the outbound rule.</span></span>

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

### <span data-ttu-id="2ee13-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2ee13-118">CommonParameters</span></span>
<span data-ttu-id="2ee13-119">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="2ee13-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2ee13-120">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2ee13-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2ee13-121">輸入</span><span class="sxs-lookup"><span data-stu-id="2ee13-121">INPUTS</span></span>

### <span data-ttu-id="2ee13-122">Microsoft.Azure.Commands.Network.models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="2ee13-122">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="2ee13-123">輸出</span><span class="sxs-lookup"><span data-stu-id="2ee13-123">OUTPUTS</span></span>

### <span data-ttu-id="2ee13-124">Microsoft.Azure.Commands.Network.models.PSOutboundRule</span><span class="sxs-lookup"><span data-stu-id="2ee13-124">Microsoft.Azure.Commands.Network.Models.PSOutboundRule</span></span>

## <span data-ttu-id="2ee13-125">筆記</span><span class="sxs-lookup"><span data-stu-id="2ee13-125">NOTES</span></span>

## <span data-ttu-id="2ee13-126">相關連結</span><span class="sxs-lookup"><span data-stu-id="2ee13-126">RELATED LINKS</span></span>

[<span data-ttu-id="2ee13-127">Add-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="2ee13-127">Add-AzLoadBalancerOutboundRuleConfig</span></span>](./Add-AzLoadBalancerOutboundRuleConfig.md)

[<span data-ttu-id="2ee13-128">New-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="2ee13-128">New-AzLoadBalancerOutboundRuleConfig</span></span>](./New-AzLoadBalancerOutboundRuleConfig.md)

[<span data-ttu-id="2ee13-129">Remove-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="2ee13-129">Remove-AzLoadBalancerOutboundRuleConfig</span></span>](./Remove-AzLoadBalancerOutboundRuleConfig.md)

[<span data-ttu-id="2ee13-130">Set-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="2ee13-130">Set-AzLoadBalancerOutboundRuleConfig</span></span>](./Set-AzLoadBalancerOutboundRuleConfig.md)
