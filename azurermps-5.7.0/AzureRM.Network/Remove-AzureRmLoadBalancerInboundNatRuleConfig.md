---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: D818C404-60E4-42DB-AADF-063305D9541B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermloadbalancerinboundnatruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmLoadBalancerInboundNatRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmLoadBalancerInboundNatRuleConfig.md
ms.openlocfilehash: 6dcd7c51a43387139de85a3a9f0c17c0b19cfe12
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93449846"
---
# <span data-ttu-id="c11ce-101">Remove-AzureRmLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="c11ce-101">Remove-AzureRmLoadBalancerInboundNatRuleConfig</span></span>

## <span data-ttu-id="c11ce-102">摘要</span><span class="sxs-lookup"><span data-stu-id="c11ce-102">SYNOPSIS</span></span>
<span data-ttu-id="c11ce-103">從負載平衡器移除入站 NAT 規則配置。</span><span class="sxs-lookup"><span data-stu-id="c11ce-103">Removes an inbound NAT rule configuration from a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c11ce-104">句法</span><span class="sxs-lookup"><span data-stu-id="c11ce-104">SYNTAX</span></span>

```
Remove-AzureRmLoadBalancerInboundNatRuleConfig [-Name <String>] -LoadBalancer <PSLoadBalancer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c11ce-105">說明</span><span class="sxs-lookup"><span data-stu-id="c11ce-105">DESCRIPTION</span></span>
<span data-ttu-id="c11ce-106">**AzureRmLoadBalancerInboundNatRuleConfig** Cmdlet 會從 Azure 負載平衡器移除入站網路位址轉譯 (NAT) 規則配置。</span><span class="sxs-lookup"><span data-stu-id="c11ce-106">The **Remove-AzureRmLoadBalancerInboundNatRuleConfig** cmdlet removes an inbound network address translation (NAT) rule configuration from an Azure load balancer.</span></span>

## <span data-ttu-id="c11ce-107">示例</span><span class="sxs-lookup"><span data-stu-id="c11ce-107">EXAMPLES</span></span>

### <span data-ttu-id="c11ce-108">1：從 Azure 負載平衡器刪除入站 NAT 規則</span><span class="sxs-lookup"><span data-stu-id="c11ce-108">1: Delete an inbound NAT rule from an Azure load balancer</span></span>
```
$loadbalancer = Get-AzureRmLoadBalancer -Name mylb -ResourceGroupName myrg

 Remove-AzureRmLoadBalancerInboundNatRuleConfig -Name "myinboundnatrule" -LoadBalancer $loadbalancer
```

<span data-ttu-id="c11ce-109">第一個命令會載入一個名為 "mylb" 的現有負載等化器，並將它儲存在 $load 平衡器的變數中。</span><span class="sxs-lookup"><span data-stu-id="c11ce-109">The first command loads an already existing load balancer called "mylb" and stores it in the variable $load balancer.</span></span> <span data-ttu-id="c11ce-110">第二個命令會移除與此負載平衡器相關聯的輸入 NAT 規則。</span><span class="sxs-lookup"><span data-stu-id="c11ce-110">The second command removes the inbound NAT rule associated with this load balancer.</span></span>

## <span data-ttu-id="c11ce-111">參數</span><span class="sxs-lookup"><span data-stu-id="c11ce-111">PARAMETERS</span></span>

### <span data-ttu-id="c11ce-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c11ce-112">-DefaultProfile</span></span>
<span data-ttu-id="c11ce-113">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="c11ce-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c11ce-114">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="c11ce-114">-LoadBalancer</span></span>
<span data-ttu-id="c11ce-115">指定包含此 Cmdlet 移除之入站 NAT 規則配置的 **LoadBalancer** 物件。</span><span class="sxs-lookup"><span data-stu-id="c11ce-115">Specifies the **LoadBalancer** object that contains the inbound NAT rule configuration that this cmdlet removes.</span></span>

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

### <span data-ttu-id="c11ce-116">-名稱</span><span class="sxs-lookup"><span data-stu-id="c11ce-116">-Name</span></span>
<span data-ttu-id="c11ce-117">指定此 Cmdlet 移除的輸入 NAT 規則配置名稱。</span><span class="sxs-lookup"><span data-stu-id="c11ce-117">Specifies the name of the inbound NAT rule configuration that this cmdlet removes.</span></span>

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

### <span data-ttu-id="c11ce-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c11ce-118">CommonParameters</span></span>
<span data-ttu-id="c11ce-119">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="c11ce-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c11ce-120">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="c11ce-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c11ce-121">輸入</span><span class="sxs-lookup"><span data-stu-id="c11ce-121">INPUTS</span></span>

### <span data-ttu-id="c11ce-122">PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="c11ce-122">PSLoadBalancer</span></span>
<span data-ttu-id="c11ce-123">形參 "LoadBalancer" 接受管線中 "PSLoadBalancer" 類型的值</span><span class="sxs-lookup"><span data-stu-id="c11ce-123">Parameter 'LoadBalancer' accepts value of type 'PSLoadBalancer' from the pipeline</span></span>

## <span data-ttu-id="c11ce-124">輸出</span><span class="sxs-lookup"><span data-stu-id="c11ce-124">OUTPUTS</span></span>

### <span data-ttu-id="c11ce-125">PSLoadBalancer 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="c11ce-125">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="c11ce-126">筆記</span><span class="sxs-lookup"><span data-stu-id="c11ce-126">NOTES</span></span>

## <span data-ttu-id="c11ce-127">相關連結</span><span class="sxs-lookup"><span data-stu-id="c11ce-127">RELATED LINKS</span></span>

[<span data-ttu-id="c11ce-128">附加 AzureRmLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="c11ce-128">Add-AzureRmLoadBalancerInboundNatRuleConfig</span></span>](./Add-AzureRmLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="c11ce-129">AzureRmLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="c11ce-129">Get-AzureRmLoadBalancerInboundNatRuleConfig</span></span>](./Get-AzureRmLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="c11ce-130">新-AzureRmLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="c11ce-130">New-AzureRmLoadBalancerInboundNatRuleConfig</span></span>](./New-AzureRmLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="c11ce-131">Set-AzureRmLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="c11ce-131">Set-AzureRmLoadBalancerInboundNatRuleConfig</span></span>](./Set-AzureRmLoadBalancerInboundNatRuleConfig.md)


