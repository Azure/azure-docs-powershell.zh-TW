---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: B2CF11FC-520C-4C14-9A1B-13F06B250B5D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermloadbalancerruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmLoadBalancerRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmLoadBalancerRuleConfig.md
ms.openlocfilehash: b09aeb7288f69d0edc678578bbcc91306f5b0c2d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93457420"
---
# <span data-ttu-id="5248e-101">Get-AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="5248e-101">Get-AzureRmLoadBalancerRuleConfig</span></span>

## <span data-ttu-id="5248e-102">摘要</span><span class="sxs-lookup"><span data-stu-id="5248e-102">SYNOPSIS</span></span>
<span data-ttu-id="5248e-103">取得負載平衡器的規則配置。</span><span class="sxs-lookup"><span data-stu-id="5248e-103">Gets the rule configuration for a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5248e-104">句法</span><span class="sxs-lookup"><span data-stu-id="5248e-104">SYNTAX</span></span>

```
Get-AzureRmLoadBalancerRuleConfig -LoadBalancer <PSLoadBalancer> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5248e-105">說明</span><span class="sxs-lookup"><span data-stu-id="5248e-105">DESCRIPTION</span></span>
<span data-ttu-id="5248e-106">**AzureRmLoadBalancerRuleConfig** Cmdlet 會取得一或多個負載平衡器的規則設定。</span><span class="sxs-lookup"><span data-stu-id="5248e-106">The **Get-AzureRmLoadBalancerRuleConfig** cmdlet gets one or more rule configurations for a load balancer.</span></span>

## <span data-ttu-id="5248e-107">示例</span><span class="sxs-lookup"><span data-stu-id="5248e-107">EXAMPLES</span></span>

### <span data-ttu-id="5248e-108">範例1：取得負載平衡器的規則設定</span><span class="sxs-lookup"><span data-stu-id="5248e-108">Example 1: Get the rule configuration of a load balancer</span></span>
```
PS C:\>$slb = Get-AzureRmLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> Get-AzureRmLoadBalancerRuleConfig -Name "MyLBrulename" -LoadBalancer $slb
```

<span data-ttu-id="5248e-109">第一個命令會取得名為 MyLoadBalancer 的負載平衡器，然後將它儲存在 $slb 的變數中。</span><span class="sxs-lookup"><span data-stu-id="5248e-109">The first command gets the load balancer named MyLoadBalancer, and then stores it in the variable $slb.</span></span>
<span data-ttu-id="5248e-110">第二個命令會從 $slb 中的負載平衡器取得名為 MyLBrulename 的相關規則配置。</span><span class="sxs-lookup"><span data-stu-id="5248e-110">The second command gets the associated rule configuration named MyLBrulename from the load balancer in $slb.</span></span>

## <span data-ttu-id="5248e-111">參數</span><span class="sxs-lookup"><span data-stu-id="5248e-111">PARAMETERS</span></span>

### <span data-ttu-id="5248e-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5248e-112">-DefaultProfile</span></span>
<span data-ttu-id="5248e-113">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="5248e-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5248e-114">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="5248e-114">-LoadBalancer</span></span>
<span data-ttu-id="5248e-115">指定與要取得之規則配置相關聯的負載平衡器。</span><span class="sxs-lookup"><span data-stu-id="5248e-115">Specifies the load balancer that is associated with the rule configuration to get.</span></span>

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

### <span data-ttu-id="5248e-116">-名稱</span><span class="sxs-lookup"><span data-stu-id="5248e-116">-Name</span></span>
<span data-ttu-id="5248e-117">指定要取得的規則配置名稱。</span><span class="sxs-lookup"><span data-stu-id="5248e-117">Specifies the name of the rule configuration to get.</span></span>

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

### <span data-ttu-id="5248e-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5248e-118">CommonParameters</span></span>
<span data-ttu-id="5248e-119">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="5248e-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5248e-120">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="5248e-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5248e-121">輸入</span><span class="sxs-lookup"><span data-stu-id="5248e-121">INPUTS</span></span>

### <span data-ttu-id="5248e-122">PSLoadBalancer 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="5248e-122">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>
<span data-ttu-id="5248e-123">參數： LoadBalancer (ByValue) </span><span class="sxs-lookup"><span data-stu-id="5248e-123">Parameters: LoadBalancer (ByValue)</span></span>

## <span data-ttu-id="5248e-124">輸出</span><span class="sxs-lookup"><span data-stu-id="5248e-124">OUTPUTS</span></span>

### <span data-ttu-id="5248e-125">PSLoadBalancingRule 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="5248e-125">Microsoft.Azure.Commands.Network.Models.PSLoadBalancingRule</span></span>

## <span data-ttu-id="5248e-126">筆記</span><span class="sxs-lookup"><span data-stu-id="5248e-126">NOTES</span></span>

## <span data-ttu-id="5248e-127">相關連結</span><span class="sxs-lookup"><span data-stu-id="5248e-127">RELATED LINKS</span></span>

[<span data-ttu-id="5248e-128">附加 AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="5248e-128">Add-AzureRmLoadBalancerRuleConfig</span></span>](./Add-AzureRmLoadBalancerRuleConfig.md)

[<span data-ttu-id="5248e-129">AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="5248e-129">Get-AzureRmLoadBalancer</span></span>](./Get-AzureRmLoadBalancer.md)

[<span data-ttu-id="5248e-130">移除-AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="5248e-130">Remove-AzureRmLoadBalancerRuleConfig</span></span>](./Remove-AzureRmLoadBalancerRuleConfig.md)

[<span data-ttu-id="5248e-131">Set-AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="5248e-131">Set-AzureRmLoadBalancerRuleConfig</span></span>](./Set-AzureRmLoadBalancerRuleConfig.md)


