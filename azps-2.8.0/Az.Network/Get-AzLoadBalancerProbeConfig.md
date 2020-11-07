---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 278228EB-0126-4F27-A30F-51DC498C65FE
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azloadbalancerprobeconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzLoadBalancerProbeConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzLoadBalancerProbeConfig.md
ms.openlocfilehash: 4b880e98a2b0352591e4a4e8840500ba2d25e431
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93789581"
---
# <span data-ttu-id="f2a90-101">Get-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="f2a90-101">Get-AzLoadBalancerProbeConfig</span></span>

## <span data-ttu-id="f2a90-102">摘要</span><span class="sxs-lookup"><span data-stu-id="f2a90-102">SYNOPSIS</span></span>
<span data-ttu-id="f2a90-103">取得負載平衡器的探測配置。</span><span class="sxs-lookup"><span data-stu-id="f2a90-103">Gets a probe configuration for a load balancer.</span></span>

## <span data-ttu-id="f2a90-104">句法</span><span class="sxs-lookup"><span data-stu-id="f2a90-104">SYNTAX</span></span>

```
Get-AzLoadBalancerProbeConfig -LoadBalancer <PSLoadBalancer> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f2a90-105">說明</span><span class="sxs-lookup"><span data-stu-id="f2a90-105">DESCRIPTION</span></span>
<span data-ttu-id="f2a90-106">**AzLoadBalancerProbeConfig** Cmdlet 會取得一或多個負載平衡器的探測設定。</span><span class="sxs-lookup"><span data-stu-id="f2a90-106">The **Get-AzLoadBalancerProbeConfig** cmdlet gets one or more probe configurations for a load balancer.</span></span>

## <span data-ttu-id="f2a90-107">示例</span><span class="sxs-lookup"><span data-stu-id="f2a90-107">EXAMPLES</span></span>

### <span data-ttu-id="f2a90-108">範例1：取得負載平衡器的探測設定</span><span class="sxs-lookup"><span data-stu-id="f2a90-108">Example 1: Get the probe configuration of a load balancer</span></span>
```
PS C:\>$slb = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> Get-AzLoadBalancerProbeConfig -Name "MyProbe" -LoadBalancer $slb
```

<span data-ttu-id="f2a90-109">第一個命令會取得名為 MyLoadBalancer 的負載平衡器，然後將它儲存在 $slb 的變數中。</span><span class="sxs-lookup"><span data-stu-id="f2a90-109">The first command gets the load balancer named MyLoadBalancer, and then stores it in the variable $slb.</span></span>
<span data-ttu-id="f2a90-110">第二個命令會從 $slb 中的負載平衡器取得名為 MyProbe 的關聯探測配置。</span><span class="sxs-lookup"><span data-stu-id="f2a90-110">The second command gets the associated probe configuration named MyProbe from the load balancer in $slb.</span></span>

## <span data-ttu-id="f2a90-111">參數</span><span class="sxs-lookup"><span data-stu-id="f2a90-111">PARAMETERS</span></span>

### <span data-ttu-id="f2a90-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f2a90-112">-DefaultProfile</span></span>
<span data-ttu-id="f2a90-113">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="f2a90-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f2a90-114">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="f2a90-114">-LoadBalancer</span></span>
<span data-ttu-id="f2a90-115">指定與要取得之探測設定關聯的負載平衡器。</span><span class="sxs-lookup"><span data-stu-id="f2a90-115">Specifies the load balancer that is associated with the probe configuration to get.</span></span>

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

### <span data-ttu-id="f2a90-116">-名稱</span><span class="sxs-lookup"><span data-stu-id="f2a90-116">-Name</span></span>
<span data-ttu-id="f2a90-117">指定要取得的探測配置名稱。</span><span class="sxs-lookup"><span data-stu-id="f2a90-117">Specifies the name of the probe configuration to get.</span></span>

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

### <span data-ttu-id="f2a90-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f2a90-118">CommonParameters</span></span>
<span data-ttu-id="f2a90-119">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="f2a90-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f2a90-120">如需詳細資訊，請參閱 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="f2a90-120">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f2a90-121">輸入</span><span class="sxs-lookup"><span data-stu-id="f2a90-121">INPUTS</span></span>

### <span data-ttu-id="f2a90-122">PSLoadBalancer 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="f2a90-122">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="f2a90-123">輸出</span><span class="sxs-lookup"><span data-stu-id="f2a90-123">OUTPUTS</span></span>

### <span data-ttu-id="f2a90-124">PSProbe 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="f2a90-124">Microsoft.Azure.Commands.Network.Models.PSProbe</span></span>

## <span data-ttu-id="f2a90-125">筆記</span><span class="sxs-lookup"><span data-stu-id="f2a90-125">NOTES</span></span>

## <span data-ttu-id="f2a90-126">相關連結</span><span class="sxs-lookup"><span data-stu-id="f2a90-126">RELATED LINKS</span></span>

[<span data-ttu-id="f2a90-127">附加 AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="f2a90-127">Add-AzLoadBalancerProbeConfig</span></span>](./Add-AzLoadBalancerProbeConfig.md)

[<span data-ttu-id="f2a90-128">AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="f2a90-128">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="f2a90-129">新-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="f2a90-129">New-AzLoadBalancerProbeConfig</span></span>](./New-AzLoadBalancerProbeConfig.md)

[<span data-ttu-id="f2a90-130">移除-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="f2a90-130">Remove-AzLoadBalancerProbeConfig</span></span>](./Remove-AzLoadBalancerProbeConfig.md)

[<span data-ttu-id="f2a90-131">Set-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="f2a90-131">Set-AzLoadBalancerProbeConfig</span></span>](./Set-AzLoadBalancerProbeConfig.md)


