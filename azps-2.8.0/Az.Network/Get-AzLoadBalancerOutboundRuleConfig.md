---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azloadbalanceroutboundruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzLoadBalancerOutboundRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzLoadBalancerOutboundRuleConfig.md
ms.openlocfilehash: 32e22416a6e624af293ffcc0597203d8b24351a9
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93789585"
---
# <span data-ttu-id="b84ac-101">Get-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="b84ac-101">Get-AzLoadBalancerOutboundRuleConfig</span></span>

## <span data-ttu-id="b84ac-102">摘要</span><span class="sxs-lookup"><span data-stu-id="b84ac-102">SYNOPSIS</span></span>
<span data-ttu-id="b84ac-103">在負載平衡器中取得輸出規則配置。</span><span class="sxs-lookup"><span data-stu-id="b84ac-103">Gets an outbound rule configuration in a load balancer.</span></span>

## <span data-ttu-id="b84ac-104">句法</span><span class="sxs-lookup"><span data-stu-id="b84ac-104">SYNTAX</span></span>

```
Get-AzLoadBalancerOutboundRuleConfig -LoadBalancer <PSLoadBalancer> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b84ac-105">說明</span><span class="sxs-lookup"><span data-stu-id="b84ac-105">DESCRIPTION</span></span>
<span data-ttu-id="b84ac-106">**AzLoadBalancerOutboundRuleConfig** Cmdlet 會在負載平衡器中取得輸出規則設定或輸出規則配置清單。</span><span class="sxs-lookup"><span data-stu-id="b84ac-106">The **Get-AzLoadBalancerOutboundRuleConfig** cmdlet gets an outbound rule configuration or a list of outbound rule configurations in a load balancer.</span></span>

## <span data-ttu-id="b84ac-107">示例</span><span class="sxs-lookup"><span data-stu-id="b84ac-107">EXAMPLES</span></span>

### <span data-ttu-id="b84ac-108">範例1：在負載平衡器中取得輸出規則配置</span><span class="sxs-lookup"><span data-stu-id="b84ac-108">Example 1: Get an outbound rule configuration in a load balancer</span></span>
```powershell
PS C:\>$slb = Get-AzLoadBalancer -ResourceGroupName "MyResourceGroup" -Name "MyLoadBalancer"
PS C:\>Get-AzLoadBalancerOutboundRuleConfig -LoadBalancer $slb -Name "MyRule"
```

<span data-ttu-id="b84ac-109">第一個命令會取得名為 MyLoadBalancer 的負載平衡器，然後將它儲存在 $slb 的變數中。</span><span class="sxs-lookup"><span data-stu-id="b84ac-109">The first command gets the load balancer named MyLoadBalancer, and then stores it in the variable $slb.</span></span>
<span data-ttu-id="b84ac-110">第二個命令會取得與該負載平衡器相關聯之名為 MyRule 的輸出規則配置。</span><span class="sxs-lookup"><span data-stu-id="b84ac-110">The second command gets the outbound rule configuration named MyRule associated with that load balancer.</span></span>

## <span data-ttu-id="b84ac-111">參數</span><span class="sxs-lookup"><span data-stu-id="b84ac-111">PARAMETERS</span></span>

### <span data-ttu-id="b84ac-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b84ac-112">-DefaultProfile</span></span>
<span data-ttu-id="b84ac-113">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="b84ac-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b84ac-114">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="b84ac-114">-LoadBalancer</span></span>
<span data-ttu-id="b84ac-115">負載平衡器資源的參照。</span><span class="sxs-lookup"><span data-stu-id="b84ac-115">The reference of the load balancer resource.</span></span>

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

### <span data-ttu-id="b84ac-116">-名稱</span><span class="sxs-lookup"><span data-stu-id="b84ac-116">-Name</span></span>
<span data-ttu-id="b84ac-117">輸出規則的名稱。</span><span class="sxs-lookup"><span data-stu-id="b84ac-117">Name of the outbound rule.</span></span>

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

### <span data-ttu-id="b84ac-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b84ac-118">CommonParameters</span></span>
<span data-ttu-id="b84ac-119">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="b84ac-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b84ac-120">如需詳細資訊，請參閱 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="b84ac-120">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b84ac-121">輸入</span><span class="sxs-lookup"><span data-stu-id="b84ac-121">INPUTS</span></span>

### <span data-ttu-id="b84ac-122">PSLoadBalancer 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="b84ac-122">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="b84ac-123">輸出</span><span class="sxs-lookup"><span data-stu-id="b84ac-123">OUTPUTS</span></span>

### <span data-ttu-id="b84ac-124">PSOutboundRule 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="b84ac-124">Microsoft.Azure.Commands.Network.Models.PSOutboundRule</span></span>

## <span data-ttu-id="b84ac-125">筆記</span><span class="sxs-lookup"><span data-stu-id="b84ac-125">NOTES</span></span>

## <span data-ttu-id="b84ac-126">相關連結</span><span class="sxs-lookup"><span data-stu-id="b84ac-126">RELATED LINKS</span></span>

[<span data-ttu-id="b84ac-127">附加 AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="b84ac-127">Add-AzLoadBalancerOutboundRuleConfig</span></span>](./Add-AzLoadBalancerOutboundRuleConfig.md)

[<span data-ttu-id="b84ac-128">新-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="b84ac-128">New-AzLoadBalancerOutboundRuleConfig</span></span>](./New-AzLoadBalancerOutboundRuleConfig.md)

[<span data-ttu-id="b84ac-129">移除-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="b84ac-129">Remove-AzLoadBalancerOutboundRuleConfig</span></span>](./Remove-AzLoadBalancerOutboundRuleConfig.md)

[<span data-ttu-id="b84ac-130">Set-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="b84ac-130">Set-AzLoadBalancerOutboundRuleConfig</span></span>](./Set-AzLoadBalancerOutboundRuleConfig.md)
