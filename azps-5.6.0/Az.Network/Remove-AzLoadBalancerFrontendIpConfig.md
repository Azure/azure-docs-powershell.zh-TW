---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 5F8E11DF-D560-44D7-99CA-C425951A56D6
online version: https://docs.microsoft.com/powershell/module/az.network/remove-azloadbalancerfrontendipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzLoadBalancerFrontendIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzLoadBalancerFrontendIpConfig.md
ms.openlocfilehash: 30b66350cffeae7fa42da7c9230a9f3976ab6cc2
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101912673"
---
# <span data-ttu-id="90c54-101">Remove-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="90c54-101">Remove-AzLoadBalancerFrontendIpConfig</span></span>

## <span data-ttu-id="90c54-102">簡介</span><span class="sxs-lookup"><span data-stu-id="90c54-102">SYNOPSIS</span></span>
<span data-ttu-id="90c54-103">從負載平衡器移除前端 IP 組式。</span><span class="sxs-lookup"><span data-stu-id="90c54-103">Removes a front-end IP configuration from a load balancer.</span></span>

## <span data-ttu-id="90c54-104">語法</span><span class="sxs-lookup"><span data-stu-id="90c54-104">SYNTAX</span></span>

```
Remove-AzLoadBalancerFrontendIpConfig -LoadBalancer <PSLoadBalancer> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="90c54-105">描述</span><span class="sxs-lookup"><span data-stu-id="90c54-105">DESCRIPTION</span></span>
<span data-ttu-id="90c54-106">**Remove-AzLoadBalancerFrontendIpConfig** Cmdlet 會從 Azure 負載平衡器移除前端 IP 組式。</span><span class="sxs-lookup"><span data-stu-id="90c54-106">The **Remove-AzLoadBalancerFrontendIpConfig** cmdlet removes a front-end IP configuration from an Azure load balancer.</span></span>

## <span data-ttu-id="90c54-107">例子</span><span class="sxs-lookup"><span data-stu-id="90c54-107">EXAMPLES</span></span>

### <span data-ttu-id="90c54-108">範例 1：從負載平衡器移除前端 IP 組</span><span class="sxs-lookup"><span data-stu-id="90c54-108">Example 1: Remove a front-end IP configuration from a load balancer</span></span>
```
PS C:\>$loadbalancer = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:> Remove-AzLoadBalancerFrontendIpConfig -Name "frontendName" -LoadBalancer $loadbalancer
```

<span data-ttu-id="90c54-109">第一個命令會取得與您想要移除的前端 IP 組配置相關聯的負載平衡器，然後將它儲存在$loadbalancer變數。</span><span class="sxs-lookup"><span data-stu-id="90c54-109">The first command gets the load balancer that is associated with the front-end IP configuration you want to remove, and then stores it in the $loadbalancer variable.</span></span>
<span data-ttu-id="90c54-110">第二個命令會從 $loadbalancer 中的負載平衡器移除相關聯的前端 IP $loadbalancer。</span><span class="sxs-lookup"><span data-stu-id="90c54-110">The second command removes the associated frontend IP configuration from the load balancer in $loadbalancer.</span></span>

## <span data-ttu-id="90c54-111">參數</span><span class="sxs-lookup"><span data-stu-id="90c54-111">PARAMETERS</span></span>

### <span data-ttu-id="90c54-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="90c54-112">-DefaultProfile</span></span>
<span data-ttu-id="90c54-113">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="90c54-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="90c54-114">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="90c54-114">-LoadBalancer</span></span>
<span data-ttu-id="90c54-115">指定包含要移除前端 IP 配置的負載平衡器。</span><span class="sxs-lookup"><span data-stu-id="90c54-115">Specifies the load balancer that contains the front-end IP configuration to remove.</span></span>

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

### <span data-ttu-id="90c54-116">-名稱</span><span class="sxs-lookup"><span data-stu-id="90c54-116">-Name</span></span>
<span data-ttu-id="90c54-117">指定要移除的前端 IP 位址組名。</span><span class="sxs-lookup"><span data-stu-id="90c54-117">Specifies the name of the front-end IP address configuration to remove.</span></span>

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

### <span data-ttu-id="90c54-118">-確認</span><span class="sxs-lookup"><span data-stu-id="90c54-118">-Confirm</span></span>
<span data-ttu-id="90c54-119">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="90c54-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="90c54-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="90c54-120">-WhatIf</span></span>
<span data-ttu-id="90c54-121">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="90c54-121">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="90c54-122">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="90c54-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="90c54-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="90c54-123">CommonParameters</span></span>
<span data-ttu-id="90c54-124">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="90c54-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="90c54-125">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="90c54-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="90c54-126">輸入</span><span class="sxs-lookup"><span data-stu-id="90c54-126">INPUTS</span></span>

### <span data-ttu-id="90c54-127">Microsoft.Azure.Commands.Network.models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="90c54-127">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="90c54-128">輸出</span><span class="sxs-lookup"><span data-stu-id="90c54-128">OUTPUTS</span></span>

### <span data-ttu-id="90c54-129">Microsoft.Azure.Commands.Network.models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="90c54-129">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="90c54-130">筆記</span><span class="sxs-lookup"><span data-stu-id="90c54-130">NOTES</span></span>

## <span data-ttu-id="90c54-131">相關連結</span><span class="sxs-lookup"><span data-stu-id="90c54-131">RELATED LINKS</span></span>

[<span data-ttu-id="90c54-132">Add-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="90c54-132">Add-AzLoadBalancerFrontendIpConfig</span></span>](./Add-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="90c54-133">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="90c54-133">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="90c54-134">Get-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="90c54-134">Get-AzLoadBalancerFrontendIpConfig</span></span>](./Get-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="90c54-135">New-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="90c54-135">New-AzLoadBalancerFrontendIpConfig</span></span>](./New-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="90c54-136">Set-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="90c54-136">Set-AzLoadBalancerFrontendIpConfig</span></span>](./Set-AzLoadBalancerFrontendIpConfig.md)


