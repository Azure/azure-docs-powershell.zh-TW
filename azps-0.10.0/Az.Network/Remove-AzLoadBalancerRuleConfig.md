---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: DEBD58A3-AFAF-485C-8708-53228625138F
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azloadbalancerruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzLoadBalancerRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzLoadBalancerRuleConfig.md
ms.openlocfilehash: 9c50452acd832c7ac7ca0c4bc2827b8f320115b4
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/16/2020
ms.locfileid: "93794167"
---
# <span data-ttu-id="5e50a-101">Remove-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="5e50a-101">Remove-AzLoadBalancerRuleConfig</span></span>

## <span data-ttu-id="5e50a-102">摘要</span><span class="sxs-lookup"><span data-stu-id="5e50a-102">SYNOPSIS</span></span>
<span data-ttu-id="5e50a-103">移除負載平衡器的規則配置。</span><span class="sxs-lookup"><span data-stu-id="5e50a-103">Removes a rule configuration for a load balancer.</span></span>

## <span data-ttu-id="5e50a-104">句法</span><span class="sxs-lookup"><span data-stu-id="5e50a-104">SYNTAX</span></span>

```
Remove-AzLoadBalancerRuleConfig [-Name <String>] -LoadBalancer <PSLoadBalancer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5e50a-105">說明</span><span class="sxs-lookup"><span data-stu-id="5e50a-105">DESCRIPTION</span></span>
<span data-ttu-id="5e50a-106">**AzLoadBalancerRuleConfig** Cmdlet 會移除 Azure 負載平衡器的規則配置。</span><span class="sxs-lookup"><span data-stu-id="5e50a-106">The **Remove-AzLoadBalancerRuleConfig** cmdlet removes a rule configuration for an Azure load balancer.</span></span>

## <span data-ttu-id="5e50a-107">示例</span><span class="sxs-lookup"><span data-stu-id="5e50a-107">EXAMPLES</span></span>

### <span data-ttu-id="5e50a-108">範例1：從負載平衡器移除規則配置</span><span class="sxs-lookup"><span data-stu-id="5e50a-108">Example 1: Remove a rule configuration from a load balancer</span></span>
```
PS C:\>$loadbalancer = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:> Remove-AzLoadBalancerRuleConfig -Name "MyLBruleName" -LoadBalancer $loadbalancer
```

<span data-ttu-id="5e50a-109">第一個命令會取得名為 MyLoadBalancer 的負載平衡器，然後將它儲存在 $loadbalancer 變數中。</span><span class="sxs-lookup"><span data-stu-id="5e50a-109">The first command gets the load balancer named MyLoadBalancer, and then stores it in the $loadbalancer variable.</span></span>

<span data-ttu-id="5e50a-110">第二個命令會從 $loadbalancer 中的負載平衡器移除名為 MyLBruleName 的規則配置。</span><span class="sxs-lookup"><span data-stu-id="5e50a-110">The second command removes the rule configuration named MyLBruleName from the load balancer in $loadbalancer.</span></span>

## <span data-ttu-id="5e50a-111">參數</span><span class="sxs-lookup"><span data-stu-id="5e50a-111">PARAMETERS</span></span>

### <span data-ttu-id="5e50a-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5e50a-112">-DefaultProfile</span></span>
<span data-ttu-id="5e50a-113">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="5e50a-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5e50a-114">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="5e50a-114">-LoadBalancer</span></span>
<span data-ttu-id="5e50a-115">指定包含此 Cmdlet 移除之規則配置的 **LoadBalancer** 物件。</span><span class="sxs-lookup"><span data-stu-id="5e50a-115">Specifies the **LoadBalancer** object that contains the rule configuration that this cmdlet removes.</span></span>

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

### <span data-ttu-id="5e50a-116">-名稱</span><span class="sxs-lookup"><span data-stu-id="5e50a-116">-Name</span></span>
<span data-ttu-id="5e50a-117">指定此 Cmdlet 移除的負載等化器規則配置名稱。</span><span class="sxs-lookup"><span data-stu-id="5e50a-117">Specifies the name of the load balancer rule configuration that this cmdlet removes.</span></span>

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

### <span data-ttu-id="5e50a-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5e50a-118">CommonParameters</span></span>
<span data-ttu-id="5e50a-119">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="5e50a-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5e50a-120">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="5e50a-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5e50a-121">輸入</span><span class="sxs-lookup"><span data-stu-id="5e50a-121">INPUTS</span></span>

### <span data-ttu-id="5e50a-122">PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="5e50a-122">PSLoadBalancer</span></span>
<span data-ttu-id="5e50a-123">形參 "LoadBalancer" 接受管線中 "PSLoadBalancer" 類型的值</span><span class="sxs-lookup"><span data-stu-id="5e50a-123">Parameter 'LoadBalancer' accepts value of type 'PSLoadBalancer' from the pipeline</span></span>

## <span data-ttu-id="5e50a-124">輸出</span><span class="sxs-lookup"><span data-stu-id="5e50a-124">OUTPUTS</span></span>

### <span data-ttu-id="5e50a-125">PSLoadBalancer 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="5e50a-125">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="5e50a-126">筆記</span><span class="sxs-lookup"><span data-stu-id="5e50a-126">NOTES</span></span>

## <span data-ttu-id="5e50a-127">相關連結</span><span class="sxs-lookup"><span data-stu-id="5e50a-127">RELATED LINKS</span></span>

[<span data-ttu-id="5e50a-128">附加 AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="5e50a-128">Add-AzLoadBalancerRuleConfig</span></span>](./Add-AzLoadBalancerRuleConfig.md)

[<span data-ttu-id="5e50a-129">AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="5e50a-129">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="5e50a-130">AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="5e50a-130">Get-AzLoadBalancerRuleConfig</span></span>](./Get-AzLoadBalancerRuleConfig.md)

[<span data-ttu-id="5e50a-131">新-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="5e50a-131">New-AzLoadBalancerRuleConfig</span></span>](./New-AzLoadBalancerRuleConfig.md)

[<span data-ttu-id="5e50a-132">Set-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="5e50a-132">Set-AzLoadBalancerRuleConfig</span></span>](./Set-AzLoadBalancerRuleConfig.md)


