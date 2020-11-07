---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 494E185D-3746-4959-846E-660017A1F392
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmLoadBalancer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmLoadBalancer.md
ms.openlocfilehash: be09bb6592ebf950c2fb3de6b4a512235fd0feab
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93624795"
---
# <span data-ttu-id="515d1-101">Set-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="515d1-101">Set-AzureRmLoadBalancer</span></span>

## <span data-ttu-id="515d1-102">摘要</span><span class="sxs-lookup"><span data-stu-id="515d1-102">SYNOPSIS</span></span>
<span data-ttu-id="515d1-103">設定負載平衡器的目標狀態。</span><span class="sxs-lookup"><span data-stu-id="515d1-103">Sets the goal state for a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="515d1-104">句法</span><span class="sxs-lookup"><span data-stu-id="515d1-104">SYNTAX</span></span>

```
Set-AzureRmLoadBalancer -LoadBalancer <PSLoadBalancer> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="515d1-105">說明</span><span class="sxs-lookup"><span data-stu-id="515d1-105">DESCRIPTION</span></span>
<span data-ttu-id="515d1-106">**AzureRmLoadBalancer** Cmdlet 設定 Azure 負載平衡器的目標狀態。</span><span class="sxs-lookup"><span data-stu-id="515d1-106">The **Set-AzureRmLoadBalancer** cmdlet sets the goal state for an Azure load balancer.</span></span>

## <span data-ttu-id="515d1-107">示例</span><span class="sxs-lookup"><span data-stu-id="515d1-107">EXAMPLES</span></span>

### <span data-ttu-id="515d1-108">範例1：修改負載平衡器</span><span class="sxs-lookup"><span data-stu-id="515d1-108">Example 1: Modify a load balancer</span></span>
```
PS C:\>$slb = Get-AzureRmLoadBalancer -Name "NRPLB" -ResourceGroupName "NRP-RG"
PS C:\> $slb | Add-AzureRmLoadBalancerInboundNatRuleConfig -Name "NewRule" -FrontendIpConfiguration $slb.FrontendIpConfigurations[0] -FrontendPort 81 -BackendPort 8181 -Protocol "TCP"
PS C:\> $slb | Set-AzureRmLoadBalancer
```

<span data-ttu-id="515d1-109">第一個命令會取得名為 NRPLB 的負載平衡器，然後將它儲存在 $slb 變數中。</span><span class="sxs-lookup"><span data-stu-id="515d1-109">The first command gets the load balancer named NRPLB, and then stores it in the $slb variable.</span></span>

<span data-ttu-id="515d1-110">第二個命令使用管線運算子，將負載平衡器 $slb 至 Add-AzureRmLoadBalancerInboundNatRuleConfig，這會新增一個名為 NewRule 的輸入 NAT 規則。</span><span class="sxs-lookup"><span data-stu-id="515d1-110">The second command uses the pipeline operator to pass the load balancer in $slb to Add-AzureRmLoadBalancerInboundNatRuleConfig, which adds an inbound NAT rule named NewRule.</span></span>

<span data-ttu-id="515d1-111">第三個命令會將負載平衡器傳到 AzureRmLoadBalancer，這會更新負載平衡器 **設定** 並儲存。</span><span class="sxs-lookup"><span data-stu-id="515d1-111">The third command passes the load balancer to **Set-AzureRmLoadBalancer** , which updates the load balancer configuration and saves it.</span></span>

## <span data-ttu-id="515d1-112">參數</span><span class="sxs-lookup"><span data-stu-id="515d1-112">PARAMETERS</span></span>

### <span data-ttu-id="515d1-113">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="515d1-113">-LoadBalancer</span></span>
<span data-ttu-id="515d1-114">指定負載平衡器。</span><span class="sxs-lookup"><span data-stu-id="515d1-114">Specifies a load balancer.</span></span>
<span data-ttu-id="515d1-115">這個 Cmdlet 會為此參數指定的負載平衡器設定目標狀態。</span><span class="sxs-lookup"><span data-stu-id="515d1-115">This cmdlet sets the goal state for the load balancer that this parameter specifies.</span></span>

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

### <span data-ttu-id="515d1-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="515d1-116">-DefaultProfile</span></span>
<span data-ttu-id="515d1-117">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="515d1-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="515d1-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="515d1-118">CommonParameters</span></span>
<span data-ttu-id="515d1-119">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="515d1-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="515d1-120">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="515d1-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="515d1-121">輸入</span><span class="sxs-lookup"><span data-stu-id="515d1-121">INPUTS</span></span>

### <span data-ttu-id="515d1-122">PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="515d1-122">PSLoadBalancer</span></span>
<span data-ttu-id="515d1-123">形參 "LoadBalancer" 接受管線中 "PSLoadBalancer" 類型的值</span><span class="sxs-lookup"><span data-stu-id="515d1-123">Parameter 'LoadBalancer' accepts value of type 'PSLoadBalancer' from the pipeline</span></span>

## <span data-ttu-id="515d1-124">輸出</span><span class="sxs-lookup"><span data-stu-id="515d1-124">OUTPUTS</span></span>

### <span data-ttu-id="515d1-125">PSLoadBalancer 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="515d1-125">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="515d1-126">筆記</span><span class="sxs-lookup"><span data-stu-id="515d1-126">NOTES</span></span>

## <span data-ttu-id="515d1-127">相關連結</span><span class="sxs-lookup"><span data-stu-id="515d1-127">RELATED LINKS</span></span>

[<span data-ttu-id="515d1-128">AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="515d1-128">Get-AzureRmLoadBalancer</span></span>](./Get-AzureRmLoadBalancer.md)

[<span data-ttu-id="515d1-129">新-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="515d1-129">New-AzureRmLoadBalancer</span></span>](./New-AzureRmLoadBalancer.md)

[<span data-ttu-id="515d1-130">移除-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="515d1-130">Remove-AzureRmLoadBalancer</span></span>](./Remove-AzureRmLoadBalancer.md)


