---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 6BEED413-E2E4-4557-BD31-2A655E790C1D
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azloadbalancerfrontendipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzLoadBalancerFrontendIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzLoadBalancerFrontendIpConfig.md
ms.openlocfilehash: 776ff53573fa68d1757ea7c0422579e253661968
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93959279"
---
# <span data-ttu-id="00ac7-101">Get-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="00ac7-101">Get-AzLoadBalancerFrontendIpConfig</span></span>

## <span data-ttu-id="00ac7-102">摘要</span><span class="sxs-lookup"><span data-stu-id="00ac7-102">SYNOPSIS</span></span>
<span data-ttu-id="00ac7-103">在負載平衡器中取得前端 IP 配置。</span><span class="sxs-lookup"><span data-stu-id="00ac7-103">Gets a front-end IP configuration in a load balancer.</span></span>

## <span data-ttu-id="00ac7-104">句法</span><span class="sxs-lookup"><span data-stu-id="00ac7-104">SYNTAX</span></span>

```
Get-AzLoadBalancerFrontendIpConfig -LoadBalancer <PSLoadBalancer> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="00ac7-105">說明</span><span class="sxs-lookup"><span data-stu-id="00ac7-105">DESCRIPTION</span></span>
<span data-ttu-id="00ac7-106">**AzLoadBalancerFrontendIpConfig** Cmdlet 會取得前端 ip 設定或負載平衡器中的前端 ip 配置清單。</span><span class="sxs-lookup"><span data-stu-id="00ac7-106">The **Get-AzLoadBalancerFrontendIpConfig** cmdlet gets a front-end IP configuration or a list of front-end IP configurations in a load balancer.</span></span>

## <span data-ttu-id="00ac7-107">示例</span><span class="sxs-lookup"><span data-stu-id="00ac7-107">EXAMPLES</span></span>

### <span data-ttu-id="00ac7-108">範例1：在負載平衡器中取得前端 IP 配置</span><span class="sxs-lookup"><span data-stu-id="00ac7-108">Example 1: Get a front-end IP configuration in a load balancer</span></span>
```
PS C:\>$slb = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> Get-AzLoadBalancerFrontendIpConfig -Name "MyFrontEnd" -LoadBalancer $slb
```

<span data-ttu-id="00ac7-109">第一個命令會取得名為 MyLoadBalancer 的負載平衡器，然後將它儲存在 $slb 的變數中。</span><span class="sxs-lookup"><span data-stu-id="00ac7-109">The first command gets the load balancer named MyLoadBalancer, and then stores it in the variable $slb.</span></span>
<span data-ttu-id="00ac7-110">第二個命令會取得與該負載平衡器相關聯的前端 IP 設定。</span><span class="sxs-lookup"><span data-stu-id="00ac7-110">The second command gets the front end IP configuration associated with that load balancer.</span></span>

## <span data-ttu-id="00ac7-111">參數</span><span class="sxs-lookup"><span data-stu-id="00ac7-111">PARAMETERS</span></span>

### <span data-ttu-id="00ac7-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="00ac7-112">-DefaultProfile</span></span>
<span data-ttu-id="00ac7-113">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="00ac7-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="00ac7-114">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="00ac7-114">-LoadBalancer</span></span>
<span data-ttu-id="00ac7-115">指定與要取得的前端 IP 配置相關聯的負載平衡器。</span><span class="sxs-lookup"><span data-stu-id="00ac7-115">Specifies the load balancer that is associated with the front-end IP configuration to get.</span></span>

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

### <span data-ttu-id="00ac7-116">-名稱</span><span class="sxs-lookup"><span data-stu-id="00ac7-116">-Name</span></span>
<span data-ttu-id="00ac7-117">指定包含要取得的前端 IP 配置的負載平衡器名稱。</span><span class="sxs-lookup"><span data-stu-id="00ac7-117">Specifies the name of the load balancer that contains the front-end IP configuration to get.</span></span>

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

### <span data-ttu-id="00ac7-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="00ac7-118">CommonParameters</span></span>
<span data-ttu-id="00ac7-119">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="00ac7-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="00ac7-120">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="00ac7-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="00ac7-121">輸入</span><span class="sxs-lookup"><span data-stu-id="00ac7-121">INPUTS</span></span>

### <span data-ttu-id="00ac7-122">PSLoadBalancer 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="00ac7-122">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="00ac7-123">輸出</span><span class="sxs-lookup"><span data-stu-id="00ac7-123">OUTPUTS</span></span>

### <span data-ttu-id="00ac7-124">PSFrontendIPConfiguration 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="00ac7-124">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration</span></span>

## <span data-ttu-id="00ac7-125">筆記</span><span class="sxs-lookup"><span data-stu-id="00ac7-125">NOTES</span></span>

## <span data-ttu-id="00ac7-126">相關連結</span><span class="sxs-lookup"><span data-stu-id="00ac7-126">RELATED LINKS</span></span>

[<span data-ttu-id="00ac7-127">附加 AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="00ac7-127">Add-AzLoadBalancerFrontendIpConfig</span></span>](./Add-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="00ac7-128">AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="00ac7-128">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="00ac7-129">新-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="00ac7-129">New-AzLoadBalancerFrontendIpConfig</span></span>](./New-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="00ac7-130">移除-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="00ac7-130">Remove-AzLoadBalancerFrontendIpConfig</span></span>](./Remove-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="00ac7-131">Set-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="00ac7-131">Set-AzLoadBalancerFrontendIpConfig</span></span>](./Set-AzLoadBalancerFrontendIpConfig.md)


