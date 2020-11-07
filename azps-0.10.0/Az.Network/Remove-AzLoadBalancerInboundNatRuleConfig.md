---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: D818C404-60E4-42DB-AADF-063305D9541B
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azloadbalancerinboundnatruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzLoadBalancerInboundNatRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzLoadBalancerInboundNatRuleConfig.md
ms.openlocfilehash: b135f9a54c084eb7bc5dc4562e16c67e316f8736
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/16/2020
ms.locfileid: "93794174"
---
# <span data-ttu-id="dfe98-101">Remove-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="dfe98-101">Remove-AzLoadBalancerInboundNatRuleConfig</span></span>

## <span data-ttu-id="dfe98-102">摘要</span><span class="sxs-lookup"><span data-stu-id="dfe98-102">SYNOPSIS</span></span>
<span data-ttu-id="dfe98-103">從負載平衡器移除入站 NAT 規則配置。</span><span class="sxs-lookup"><span data-stu-id="dfe98-103">Removes an inbound NAT rule configuration from a load balancer.</span></span>

## <span data-ttu-id="dfe98-104">句法</span><span class="sxs-lookup"><span data-stu-id="dfe98-104">SYNTAX</span></span>

```
Remove-AzLoadBalancerInboundNatRuleConfig [-Name <String>] -LoadBalancer <PSLoadBalancer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="dfe98-105">說明</span><span class="sxs-lookup"><span data-stu-id="dfe98-105">DESCRIPTION</span></span>
<span data-ttu-id="dfe98-106">**AzLoadBalancerInboundNatRuleConfig** Cmdlet 會從 Azure 負載平衡器移除入站網路位址轉譯 (NAT) 規則配置。</span><span class="sxs-lookup"><span data-stu-id="dfe98-106">The **Remove-AzLoadBalancerInboundNatRuleConfig** cmdlet removes an inbound network address translation (NAT) rule configuration from an Azure load balancer.</span></span>

## <span data-ttu-id="dfe98-107">示例</span><span class="sxs-lookup"><span data-stu-id="dfe98-107">EXAMPLES</span></span>

### <span data-ttu-id="dfe98-108">1：從 Azure 負載平衡器刪除入站 NAT 規則</span><span class="sxs-lookup"><span data-stu-id="dfe98-108">1: Delete an inbound NAT rule from an Azure load balancer</span></span>
```
$loadbalancer = Get-AzLoadBalancer -Name mylb -ResourceGroupName myrg

 Remove-AzLoadBalancerInboundNatRuleConfig -Name "myinboundnatrule" -LoadBalancer $loadbalancer
```

<span data-ttu-id="dfe98-109">第一個命令會載入一個名為 "mylb" 的現有負載等化器，並將它儲存在 $load 平衡器的變數中。</span><span class="sxs-lookup"><span data-stu-id="dfe98-109">The first command loads an already existing load balancer called "mylb" and stores it in the variable $load balancer.</span></span> <span data-ttu-id="dfe98-110">第二個命令會移除與此負載平衡器相關聯的輸入 NAT 規則。</span><span class="sxs-lookup"><span data-stu-id="dfe98-110">The second command removes the inbound NAT rule associated with this load balancer.</span></span>

## <span data-ttu-id="dfe98-111">參數</span><span class="sxs-lookup"><span data-stu-id="dfe98-111">PARAMETERS</span></span>

### <span data-ttu-id="dfe98-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dfe98-112">-DefaultProfile</span></span>
<span data-ttu-id="dfe98-113">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="dfe98-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dfe98-114">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="dfe98-114">-LoadBalancer</span></span>
<span data-ttu-id="dfe98-115">指定包含此 Cmdlet 移除之入站 NAT 規則配置的 **LoadBalancer** 物件。</span><span class="sxs-lookup"><span data-stu-id="dfe98-115">Specifies the **LoadBalancer** object that contains the inbound NAT rule configuration that this cmdlet removes.</span></span>

```yaml
Type: PSLoadBalancer
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="dfe98-116">-名稱</span><span class="sxs-lookup"><span data-stu-id="dfe98-116">-Name</span></span>
<span data-ttu-id="dfe98-117">指定此 Cmdlet 移除的輸入 NAT 規則配置名稱。</span><span class="sxs-lookup"><span data-stu-id="dfe98-117">Specifies the name of the inbound NAT rule configuration that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dfe98-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dfe98-118">CommonParameters</span></span>
<span data-ttu-id="dfe98-119">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="dfe98-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dfe98-120">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="dfe98-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dfe98-121">輸入</span><span class="sxs-lookup"><span data-stu-id="dfe98-121">INPUTS</span></span>

### <span data-ttu-id="dfe98-122">PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="dfe98-122">PSLoadBalancer</span></span>
<span data-ttu-id="dfe98-123">形參 "LoadBalancer" 接受管線中 "PSLoadBalancer" 類型的值</span><span class="sxs-lookup"><span data-stu-id="dfe98-123">Parameter 'LoadBalancer' accepts value of type 'PSLoadBalancer' from the pipeline</span></span>

## <span data-ttu-id="dfe98-124">輸出</span><span class="sxs-lookup"><span data-stu-id="dfe98-124">OUTPUTS</span></span>

### <span data-ttu-id="dfe98-125">PSLoadBalancer 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="dfe98-125">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="dfe98-126">筆記</span><span class="sxs-lookup"><span data-stu-id="dfe98-126">NOTES</span></span>

## <span data-ttu-id="dfe98-127">相關連結</span><span class="sxs-lookup"><span data-stu-id="dfe98-127">RELATED LINKS</span></span>

[<span data-ttu-id="dfe98-128">附加 AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="dfe98-128">Add-AzLoadBalancerInboundNatRuleConfig</span></span>](./Add-AzLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="dfe98-129">AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="dfe98-129">Get-AzLoadBalancerInboundNatRuleConfig</span></span>](./Get-AzLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="dfe98-130">新-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="dfe98-130">New-AzLoadBalancerInboundNatRuleConfig</span></span>](./New-AzLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="dfe98-131">Set-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="dfe98-131">Set-AzLoadBalancerInboundNatRuleConfig</span></span>](./Set-AzLoadBalancerInboundNatRuleConfig.md)


