---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: DEBD58A3-AFAF-485C-8708-53228625138F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermloadbalancerruleconfig
schema: 2.0.0
ms.openlocfilehash: bb0821265f87f959523009a9277dc884498e0e0c
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/15/2020
ms.locfileid: "93801994"
---
# <span data-ttu-id="2f721-101">Remove-AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="2f721-101">Remove-AzureRmLoadBalancerRuleConfig</span></span>

## <span data-ttu-id="2f721-102">摘要</span><span class="sxs-lookup"><span data-stu-id="2f721-102">SYNOPSIS</span></span>
<span data-ttu-id="2f721-103">移除負載平衡器的規則配置。</span><span class="sxs-lookup"><span data-stu-id="2f721-103">Removes a rule configuration for a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2f721-104">句法</span><span class="sxs-lookup"><span data-stu-id="2f721-104">SYNTAX</span></span>

```
Remove-AzureRmLoadBalancerRuleConfig [-Name <String>] -LoadBalancer <PSLoadBalancer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2f721-105">說明</span><span class="sxs-lookup"><span data-stu-id="2f721-105">DESCRIPTION</span></span>
<span data-ttu-id="2f721-106">**AzureRmLoadBalancerRuleConfig** Cmdlet 會移除 Azure 負載平衡器的規則配置。</span><span class="sxs-lookup"><span data-stu-id="2f721-106">The **Remove-AzureRmLoadBalancerRuleConfig** cmdlet removes a rule configuration for an Azure load balancer.</span></span>

## <span data-ttu-id="2f721-107">示例</span><span class="sxs-lookup"><span data-stu-id="2f721-107">EXAMPLES</span></span>

### <span data-ttu-id="2f721-108">範例1：從負載平衡器移除規則配置</span><span class="sxs-lookup"><span data-stu-id="2f721-108">Example 1: Remove a rule configuration from a load balancer</span></span>
```
PS C:\>$loadbalancer = Get-AzureRmLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:> Remove-AzureRmLoadBalancerRuleConfig -Name "MyLBruleName" -LoadBalancer $loadbalancer
```

<span data-ttu-id="2f721-109">第一個命令會取得名為 MyLoadBalancer 的負載平衡器，然後將它儲存在 $loadbalancer 變數中。</span><span class="sxs-lookup"><span data-stu-id="2f721-109">The first command gets the load balancer named MyLoadBalancer, and then stores it in the $loadbalancer variable.</span></span>

<span data-ttu-id="2f721-110">第二個命令會從 $loadbalancer 中的負載平衡器移除名為 MyLBruleName 的規則配置。</span><span class="sxs-lookup"><span data-stu-id="2f721-110">The second command removes the rule configuration named MyLBruleName from the load balancer in $loadbalancer.</span></span>

## <span data-ttu-id="2f721-111">參數</span><span class="sxs-lookup"><span data-stu-id="2f721-111">PARAMETERS</span></span>

### <span data-ttu-id="2f721-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2f721-112">-DefaultProfile</span></span>
<span data-ttu-id="2f721-113">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="2f721-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2f721-114">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="2f721-114">-LoadBalancer</span></span>
<span data-ttu-id="2f721-115">指定包含此 Cmdlet 移除之規則配置的 **LoadBalancer** 物件。</span><span class="sxs-lookup"><span data-stu-id="2f721-115">Specifies the **LoadBalancer** object that contains the rule configuration that this cmdlet removes.</span></span>

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

### <span data-ttu-id="2f721-116">-名稱</span><span class="sxs-lookup"><span data-stu-id="2f721-116">-Name</span></span>
<span data-ttu-id="2f721-117">指定此 Cmdlet 移除的負載等化器規則配置名稱。</span><span class="sxs-lookup"><span data-stu-id="2f721-117">Specifies the name of the load balancer rule configuration that this cmdlet removes.</span></span>

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

### <span data-ttu-id="2f721-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2f721-118">CommonParameters</span></span>
<span data-ttu-id="2f721-119">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="2f721-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2f721-120">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="2f721-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2f721-121">輸入</span><span class="sxs-lookup"><span data-stu-id="2f721-121">INPUTS</span></span>

### <span data-ttu-id="2f721-122">PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="2f721-122">PSLoadBalancer</span></span>
<span data-ttu-id="2f721-123">形參 "LoadBalancer" 接受管線中 "PSLoadBalancer" 類型的值</span><span class="sxs-lookup"><span data-stu-id="2f721-123">Parameter 'LoadBalancer' accepts value of type 'PSLoadBalancer' from the pipeline</span></span>

## <span data-ttu-id="2f721-124">輸出</span><span class="sxs-lookup"><span data-stu-id="2f721-124">OUTPUTS</span></span>

### <span data-ttu-id="2f721-125">PSLoadBalancer 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="2f721-125">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="2f721-126">筆記</span><span class="sxs-lookup"><span data-stu-id="2f721-126">NOTES</span></span>

## <span data-ttu-id="2f721-127">相關連結</span><span class="sxs-lookup"><span data-stu-id="2f721-127">RELATED LINKS</span></span>

[<span data-ttu-id="2f721-128">附加 AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="2f721-128">Add-AzureRmLoadBalancerRuleConfig</span></span>](./Add-AzureRmLoadBalancerRuleConfig.md)

[<span data-ttu-id="2f721-129">AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="2f721-129">Get-AzureRmLoadBalancer</span></span>](./Get-AzureRmLoadBalancer.md)

[<span data-ttu-id="2f721-130">AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="2f721-130">Get-AzureRmLoadBalancerRuleConfig</span></span>](./Get-AzureRmLoadBalancerRuleConfig.md)

[<span data-ttu-id="2f721-131">新-AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="2f721-131">New-AzureRmLoadBalancerRuleConfig</span></span>](./New-AzureRmLoadBalancerRuleConfig.md)

[<span data-ttu-id="2f721-132">Set-AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="2f721-132">Set-AzureRmLoadBalancerRuleConfig</span></span>](./Set-AzureRmLoadBalancerRuleConfig.md)


