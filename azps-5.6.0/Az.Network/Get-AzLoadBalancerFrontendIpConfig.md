---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 6BEED413-E2E4-4557-BD31-2A655E790C1D
online version: https://docs.microsoft.com/powershell/module/az.network/get-azloadbalancerfrontendipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzLoadBalancerFrontendIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzLoadBalancerFrontendIpConfig.md
ms.openlocfilehash: 2cafba2d579a37db45f12c5e3dd1746f799bfe21
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101903122"
---
# <span data-ttu-id="a081c-101">Get-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="a081c-101">Get-AzLoadBalancerFrontendIpConfig</span></span>

## <span data-ttu-id="a081c-102">簡介</span><span class="sxs-lookup"><span data-stu-id="a081c-102">SYNOPSIS</span></span>
<span data-ttu-id="a081c-103">在負載平衡器中取得前端 IP 組式。</span><span class="sxs-lookup"><span data-stu-id="a081c-103">Gets a front-end IP configuration in a load balancer.</span></span>

## <span data-ttu-id="a081c-104">語法</span><span class="sxs-lookup"><span data-stu-id="a081c-104">SYNTAX</span></span>

```
Get-AzLoadBalancerFrontendIpConfig -LoadBalancer <PSLoadBalancer> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a081c-105">描述</span><span class="sxs-lookup"><span data-stu-id="a081c-105">DESCRIPTION</span></span>
<span data-ttu-id="a081c-106">**Get-AzLoadBalancerFrontendIpConfig** Cmdlet 會取得前端 IP 組式或負載平衡器中的前端 IP 組式清單。</span><span class="sxs-lookup"><span data-stu-id="a081c-106">The **Get-AzLoadBalancerFrontendIpConfig** cmdlet gets a front-end IP configuration or a list of front-end IP configurations in a load balancer.</span></span>

## <span data-ttu-id="a081c-107">例子</span><span class="sxs-lookup"><span data-stu-id="a081c-107">EXAMPLES</span></span>

### <span data-ttu-id="a081c-108">範例 1：在負載平衡器中取得前端 IP 組</span><span class="sxs-lookup"><span data-stu-id="a081c-108">Example 1: Get a front-end IP configuration in a load balancer</span></span>
```
PS C:\>$slb = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> Get-AzLoadBalancerFrontendIpConfig -Name "MyFrontEnd" -LoadBalancer $slb
```

<span data-ttu-id="a081c-109">第一個命令會取得名為 MyLoadBalancer 的負載平衡器，然後將它儲存在變數 $slb。</span><span class="sxs-lookup"><span data-stu-id="a081c-109">The first command gets the load balancer named MyLoadBalancer, and then stores it in the variable $slb.</span></span>
<span data-ttu-id="a081c-110">第二個命令會取得與該負載平衡器相關聯的前端 IP 組。</span><span class="sxs-lookup"><span data-stu-id="a081c-110">The second command gets the front end IP configuration associated with that load balancer.</span></span>

## <span data-ttu-id="a081c-111">參數</span><span class="sxs-lookup"><span data-stu-id="a081c-111">PARAMETERS</span></span>

### <span data-ttu-id="a081c-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a081c-112">-DefaultProfile</span></span>
<span data-ttu-id="a081c-113">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="a081c-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a081c-114">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="a081c-114">-LoadBalancer</span></span>
<span data-ttu-id="a081c-115">指定要取得前端 IP 配置的負載平衡器。</span><span class="sxs-lookup"><span data-stu-id="a081c-115">Specifies the load balancer that is associated with the front-end IP configuration to get.</span></span>

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

### <span data-ttu-id="a081c-116">-名稱</span><span class="sxs-lookup"><span data-stu-id="a081c-116">-Name</span></span>
<span data-ttu-id="a081c-117">指定包含要取得前端 IP 配置的負載平衡器名稱。</span><span class="sxs-lookup"><span data-stu-id="a081c-117">Specifies the name of the load balancer that contains the front-end IP configuration to get.</span></span>

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

### <span data-ttu-id="a081c-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a081c-118">CommonParameters</span></span>
<span data-ttu-id="a081c-119">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="a081c-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a081c-120">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a081c-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a081c-121">輸入</span><span class="sxs-lookup"><span data-stu-id="a081c-121">INPUTS</span></span>

### <span data-ttu-id="a081c-122">Microsoft.Azure.Commands.Network.models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="a081c-122">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="a081c-123">輸出</span><span class="sxs-lookup"><span data-stu-id="a081c-123">OUTPUTS</span></span>

### <span data-ttu-id="a081c-124">Microsoft.Azure.Commands.Network.models.PSFrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="a081c-124">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration</span></span>

## <span data-ttu-id="a081c-125">筆記</span><span class="sxs-lookup"><span data-stu-id="a081c-125">NOTES</span></span>

## <span data-ttu-id="a081c-126">相關連結</span><span class="sxs-lookup"><span data-stu-id="a081c-126">RELATED LINKS</span></span>

[<span data-ttu-id="a081c-127">Add-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="a081c-127">Add-AzLoadBalancerFrontendIpConfig</span></span>](./Add-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="a081c-128">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="a081c-128">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="a081c-129">New-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="a081c-129">New-AzLoadBalancerFrontendIpConfig</span></span>](./New-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="a081c-130">Remove-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="a081c-130">Remove-AzLoadBalancerFrontendIpConfig</span></span>](./Remove-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="a081c-131">Set-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="a081c-131">Set-AzLoadBalancerFrontendIpConfig</span></span>](./Set-AzLoadBalancerFrontendIpConfig.md)


