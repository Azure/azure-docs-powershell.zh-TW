---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 1FDA90C0-D01F-45E1-9149-16AD04046271
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmLoadBalancerInboundNatRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmLoadBalancerInboundNatRuleConfig.md
ms.openlocfilehash: 71c093573f4384884702c72e586c36bbdb9b4066
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93451636"
---
# <span data-ttu-id="4e247-101">Get-AzureRmLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="4e247-101">Get-AzureRmLoadBalancerInboundNatRuleConfig</span></span>

## <span data-ttu-id="4e247-102">摘要</span><span class="sxs-lookup"><span data-stu-id="4e247-102">SYNOPSIS</span></span>
<span data-ttu-id="4e247-103">取得負載平衡器的入站 NAT 規則配置。</span><span class="sxs-lookup"><span data-stu-id="4e247-103">Gets an inbound NAT rule configuration for a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4e247-104">句法</span><span class="sxs-lookup"><span data-stu-id="4e247-104">SYNTAX</span></span>

```
Get-AzureRmLoadBalancerInboundNatRuleConfig [-Name <String>] -LoadBalancer <PSLoadBalancer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4e247-105">說明</span><span class="sxs-lookup"><span data-stu-id="4e247-105">DESCRIPTION</span></span>
<span data-ttu-id="4e247-106">**AzureRmLoadBalancerInboundNatRuleConfig** Cmdlet 會在 Azure 負載平衡器中取得一或多個入站網路位址轉譯 (NAT) 規則。</span><span class="sxs-lookup"><span data-stu-id="4e247-106">The **Get-AzureRmLoadBalancerInboundNatRuleConfig** cmdlet gets one or more inbound network address translation (NAT) rules in an Azure load balancer.</span></span>

## <span data-ttu-id="4e247-107">示例</span><span class="sxs-lookup"><span data-stu-id="4e247-107">EXAMPLES</span></span>

### <span data-ttu-id="4e247-108">範例1：取得入站 NAT 規則設定</span><span class="sxs-lookup"><span data-stu-id="4e247-108">Example 1: Get an inbound NAT rule configuration</span></span>
```
PS C:\>$slb = Get-AzureRmLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> Get-AzureRmLoadBalancerInboundNatRuleConfig -Name "MyInboundNatRule1" -LoadBalancer $slb
```

<span data-ttu-id="4e247-109">第一個命令會取得名為 MyLoadBalancer 的負載平衡器，並將它儲存在 $slb 的變數中。</span><span class="sxs-lookup"><span data-stu-id="4e247-109">The first command gets the load balancer named MyLoadBalancer, and stores it in the variable $slb.</span></span>

<span data-ttu-id="4e247-110">第二個命令會從 $slb 中的負載平衡器取得關聯的 NAT 規則（名為 MyInboundNatRule1）。</span><span class="sxs-lookup"><span data-stu-id="4e247-110">The second command gets the associated NAT rule named MyInboundNatRule1 from the load balancer in $slb.</span></span>

## <span data-ttu-id="4e247-111">參數</span><span class="sxs-lookup"><span data-stu-id="4e247-111">PARAMETERS</span></span>

### <span data-ttu-id="4e247-112">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="4e247-112">-LoadBalancer</span></span>
<span data-ttu-id="4e247-113">指定與要取得的輸入 NAT 規則配置相關聯的負載平衡器。</span><span class="sxs-lookup"><span data-stu-id="4e247-113">Specifies the load balancer that is associated with the inbound NAT rule configuration to get.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSLoadBalancer
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4e247-114">-名稱</span><span class="sxs-lookup"><span data-stu-id="4e247-114">-Name</span></span>
<span data-ttu-id="4e247-115">指定要取得的輸入 NAT 規則配置名稱。</span><span class="sxs-lookup"><span data-stu-id="4e247-115">Specifies the name of the inbound NAT rule configuration to get.</span></span>

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

### <span data-ttu-id="4e247-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4e247-116">-DefaultProfile</span></span>
<span data-ttu-id="4e247-117">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="4e247-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4e247-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4e247-118">CommonParameters</span></span>
<span data-ttu-id="4e247-119">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="4e247-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4e247-120">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="4e247-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4e247-121">輸入</span><span class="sxs-lookup"><span data-stu-id="4e247-121">INPUTS</span></span>

### <span data-ttu-id="4e247-122">PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="4e247-122">PSLoadBalancer</span></span>
<span data-ttu-id="4e247-123">形參 "LoadBalancer" 接受管線中 "PSLoadBalancer" 類型的值</span><span class="sxs-lookup"><span data-stu-id="4e247-123">Parameter 'LoadBalancer' accepts value of type 'PSLoadBalancer' from the pipeline</span></span>

## <span data-ttu-id="4e247-124">輸出</span><span class="sxs-lookup"><span data-stu-id="4e247-124">OUTPUTS</span></span>

### <span data-ttu-id="4e247-125">PSInboundNatRule 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="4e247-125">Microsoft.Azure.Commands.Network.Models.PSInboundNatRule</span></span>

## <span data-ttu-id="4e247-126">筆記</span><span class="sxs-lookup"><span data-stu-id="4e247-126">NOTES</span></span>

## <span data-ttu-id="4e247-127">相關連結</span><span class="sxs-lookup"><span data-stu-id="4e247-127">RELATED LINKS</span></span>

[<span data-ttu-id="4e247-128">AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="4e247-128">Get-AzureRmLoadBalancer</span></span>](./Get-AzureRmLoadBalancer.md)

[<span data-ttu-id="4e247-129">新-AzureRmLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="4e247-129">New-AzureRmLoadBalancerInboundNatRuleConfig</span></span>](./New-AzureRmLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="4e247-130">移除-AzureRmLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="4e247-130">Remove-AzureRmLoadBalancerInboundNatRuleConfig</span></span>](./Remove-AzureRmLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="4e247-131">Set-AzureRmLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="4e247-131">Set-AzureRmLoadBalancerInboundNatRuleConfig</span></span>](./Set-AzureRmLoadBalancerInboundNatRuleConfig.md)


