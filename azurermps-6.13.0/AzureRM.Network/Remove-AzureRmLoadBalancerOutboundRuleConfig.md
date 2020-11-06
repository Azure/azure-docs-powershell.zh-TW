---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermloadbalanceroutboundruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmLoadBalancerOutboundRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmLoadBalancerOutboundRuleConfig.md
ms.openlocfilehash: cc9a79b424d6ad81804aaed0d941ca017463abba
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93450228"
---
# <span data-ttu-id="285ca-101">Remove-AzureRmLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="285ca-101">Remove-AzureRmLoadBalancerOutboundRuleConfig</span></span>

## <span data-ttu-id="285ca-102">摘要</span><span class="sxs-lookup"><span data-stu-id="285ca-102">SYNOPSIS</span></span>
<span data-ttu-id="285ca-103">從負載平衡器移除輸出規則配置。</span><span class="sxs-lookup"><span data-stu-id="285ca-103">Removes an outbound rule configuration from a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="285ca-104">句法</span><span class="sxs-lookup"><span data-stu-id="285ca-104">SYNTAX</span></span>

```
Remove-AzureRmLoadBalancerOutboundRuleConfig -LoadBalancer <PSLoadBalancer> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="285ca-105">說明</span><span class="sxs-lookup"><span data-stu-id="285ca-105">DESCRIPTION</span></span>
<span data-ttu-id="285ca-106">**AzureRmLoadBalancerOutboundRuleConfig** Cmdlet 會從 Azure 負載平衡器移除輸出規則配置。</span><span class="sxs-lookup"><span data-stu-id="285ca-106">The **Remove-AzureRmLoadBalancerOutboundRuleConfig** cmdlet removes an outbound rule configuration from an Azure load balancer.</span></span>

## <span data-ttu-id="285ca-107">示例</span><span class="sxs-lookup"><span data-stu-id="285ca-107">EXAMPLES</span></span>

### <span data-ttu-id="285ca-108">範例1：從 Azure 負載平衡器刪除輸出規則</span><span class="sxs-lookup"><span data-stu-id="285ca-108">Example 1: Delete an outbound rule from an Azure load balancer</span></span>
```powershell
PS C:\>$slb = Get-AzureRmLoadBalancer -ResourceGroupName "MyResourceGroup" -Name "MyLoadBalancer"
PS C:\>Remove-AzureRmLoadBalancerOutboundRuleConfig -Name "RuleName" -LoadBalancer $slb
PS C:\>Set-AzureRmLoadBalancer -LoadBalancer $slb
```

<span data-ttu-id="285ca-109">第一個命令會取得與您想要移除的輸出規則配置相關聯的負載平衡器，然後將它儲存在 $slb 變數中。</span><span class="sxs-lookup"><span data-stu-id="285ca-109">The first command gets the load balancer that is associated with the outbound rule configuration you want to remove, and then stores it in the $slb variable.</span></span>
<span data-ttu-id="285ca-110">第二個命令會從負載平衡器移除關聯的輸出規則配置。</span><span class="sxs-lookup"><span data-stu-id="285ca-110">The second command removes the associated outbound rule configuration from the load balancer.</span></span>
<span data-ttu-id="285ca-111">第三個命令會更新負載平衡器。</span><span class="sxs-lookup"><span data-stu-id="285ca-111">The third command updates the load balancer.</span></span>

## <span data-ttu-id="285ca-112">參數</span><span class="sxs-lookup"><span data-stu-id="285ca-112">PARAMETERS</span></span>

### <span data-ttu-id="285ca-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="285ca-113">-DefaultProfile</span></span>
<span data-ttu-id="285ca-114">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="285ca-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="285ca-115">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="285ca-115">-LoadBalancer</span></span>
<span data-ttu-id="285ca-116">負載平衡器資源的參照。</span><span class="sxs-lookup"><span data-stu-id="285ca-116">The reference of the load balancer resource.</span></span>

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

### <span data-ttu-id="285ca-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="285ca-117">-Name</span></span>
<span data-ttu-id="285ca-118">輸出規則的名稱</span><span class="sxs-lookup"><span data-stu-id="285ca-118">The Name of outbound rule</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="285ca-119">-確認</span><span class="sxs-lookup"><span data-stu-id="285ca-119">-Confirm</span></span>
<span data-ttu-id="285ca-120">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="285ca-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="285ca-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="285ca-121">-WhatIf</span></span>
<span data-ttu-id="285ca-122">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="285ca-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="285ca-123">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="285ca-123">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="285ca-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="285ca-124">CommonParameters</span></span>
<span data-ttu-id="285ca-125">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="285ca-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="285ca-126">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="285ca-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="285ca-127">輸入</span><span class="sxs-lookup"><span data-stu-id="285ca-127">INPUTS</span></span>

### <span data-ttu-id="285ca-128">PSLoadBalancer 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="285ca-128">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="285ca-129">輸出</span><span class="sxs-lookup"><span data-stu-id="285ca-129">OUTPUTS</span></span>

### <span data-ttu-id="285ca-130">PSLoadBalancer 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="285ca-130">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="285ca-131">筆記</span><span class="sxs-lookup"><span data-stu-id="285ca-131">NOTES</span></span>

## <span data-ttu-id="285ca-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="285ca-132">RELATED LINKS</span></span>
