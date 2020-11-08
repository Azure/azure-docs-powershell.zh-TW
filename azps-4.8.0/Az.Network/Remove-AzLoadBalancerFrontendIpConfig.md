---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 5F8E11DF-D560-44D7-99CA-C425951A56D6
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azloadbalancerfrontendipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzLoadBalancerFrontendIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzLoadBalancerFrontendIpConfig.md
ms.openlocfilehash: bde16a6f3ecd68307574ae5eac7760a177101cc1
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94126425"
---
# <span data-ttu-id="4a3ce-101">Remove-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="4a3ce-101">Remove-AzLoadBalancerFrontendIpConfig</span></span>

## <span data-ttu-id="4a3ce-102">摘要</span><span class="sxs-lookup"><span data-stu-id="4a3ce-102">SYNOPSIS</span></span>
<span data-ttu-id="4a3ce-103">從負載平衡器移除前端 IP 配置。</span><span class="sxs-lookup"><span data-stu-id="4a3ce-103">Removes a front-end IP configuration from a load balancer.</span></span>

## <span data-ttu-id="4a3ce-104">句法</span><span class="sxs-lookup"><span data-stu-id="4a3ce-104">SYNTAX</span></span>

```
Remove-AzLoadBalancerFrontendIpConfig -LoadBalancer <PSLoadBalancer> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4a3ce-105">說明</span><span class="sxs-lookup"><span data-stu-id="4a3ce-105">DESCRIPTION</span></span>
<span data-ttu-id="4a3ce-106">**AzLoadBalancerFrontendIpConfig** Cmdlet 會從 Azure 負載平衡器移除前端 IP 配置。</span><span class="sxs-lookup"><span data-stu-id="4a3ce-106">The **Remove-AzLoadBalancerFrontendIpConfig** cmdlet removes a front-end IP configuration from an Azure load balancer.</span></span>

## <span data-ttu-id="4a3ce-107">示例</span><span class="sxs-lookup"><span data-stu-id="4a3ce-107">EXAMPLES</span></span>

### <span data-ttu-id="4a3ce-108">範例1：從負載平衡器移除前端 IP 配置</span><span class="sxs-lookup"><span data-stu-id="4a3ce-108">Example 1: Remove a front-end IP configuration from a load balancer</span></span>
```
PS C:\>$loadbalancer = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:> Remove-AzLoadBalancerFrontendIpConfig -Name "frontendName" -LoadBalancer $loadbalancer
```

<span data-ttu-id="4a3ce-109">第一個命令會取得與您想要移除的前端 IP 設定相關聯的負載平衡器，然後將它儲存在 $loadbalancer 變數中。</span><span class="sxs-lookup"><span data-stu-id="4a3ce-109">The first command gets the load balancer that is associated with the front-end IP configuration you want to remove, and then stores it in the $loadbalancer variable.</span></span>
<span data-ttu-id="4a3ce-110">第二個命令會從 $loadbalancer 中的負載平衡器移除關聯的前端 IP 設定。</span><span class="sxs-lookup"><span data-stu-id="4a3ce-110">The second command removes the associated frontend IP configuration from the load balancer in $loadbalancer.</span></span>

## <span data-ttu-id="4a3ce-111">參數</span><span class="sxs-lookup"><span data-stu-id="4a3ce-111">PARAMETERS</span></span>

### <span data-ttu-id="4a3ce-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4a3ce-112">-DefaultProfile</span></span>
<span data-ttu-id="4a3ce-113">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="4a3ce-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4a3ce-114">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="4a3ce-114">-LoadBalancer</span></span>
<span data-ttu-id="4a3ce-115">指定包含要移除之前端 IP 配置的負載平衡器。</span><span class="sxs-lookup"><span data-stu-id="4a3ce-115">Specifies the load balancer that contains the front-end IP configuration to remove.</span></span>

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

### <span data-ttu-id="4a3ce-116">-名稱</span><span class="sxs-lookup"><span data-stu-id="4a3ce-116">-Name</span></span>
<span data-ttu-id="4a3ce-117">指定要移除的前端 IP 位址配置名稱。</span><span class="sxs-lookup"><span data-stu-id="4a3ce-117">Specifies the name of the front-end IP address configuration to remove.</span></span>

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

### <span data-ttu-id="4a3ce-118">-確認</span><span class="sxs-lookup"><span data-stu-id="4a3ce-118">-Confirm</span></span>
<span data-ttu-id="4a3ce-119">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="4a3ce-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4a3ce-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4a3ce-120">-WhatIf</span></span>
<span data-ttu-id="4a3ce-121">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="4a3ce-121">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="4a3ce-122">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="4a3ce-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4a3ce-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4a3ce-123">CommonParameters</span></span>
<span data-ttu-id="4a3ce-124">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="4a3ce-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4a3ce-125">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="4a3ce-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4a3ce-126">輸入</span><span class="sxs-lookup"><span data-stu-id="4a3ce-126">INPUTS</span></span>

### <span data-ttu-id="4a3ce-127">PSLoadBalancer 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="4a3ce-127">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="4a3ce-128">輸出</span><span class="sxs-lookup"><span data-stu-id="4a3ce-128">OUTPUTS</span></span>

### <span data-ttu-id="4a3ce-129">PSLoadBalancer 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="4a3ce-129">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="4a3ce-130">筆記</span><span class="sxs-lookup"><span data-stu-id="4a3ce-130">NOTES</span></span>

## <span data-ttu-id="4a3ce-131">相關連結</span><span class="sxs-lookup"><span data-stu-id="4a3ce-131">RELATED LINKS</span></span>

[<span data-ttu-id="4a3ce-132">附加 AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="4a3ce-132">Add-AzLoadBalancerFrontendIpConfig</span></span>](./Add-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="4a3ce-133">AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="4a3ce-133">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="4a3ce-134">AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="4a3ce-134">Get-AzLoadBalancerFrontendIpConfig</span></span>](./Get-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="4a3ce-135">新-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="4a3ce-135">New-AzLoadBalancerFrontendIpConfig</span></span>](./New-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="4a3ce-136">Set-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="4a3ce-136">Set-AzLoadBalancerFrontendIpConfig</span></span>](./Set-AzLoadBalancerFrontendIpConfig.md)


