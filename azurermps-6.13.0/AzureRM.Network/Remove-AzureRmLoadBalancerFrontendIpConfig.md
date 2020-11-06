---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 5F8E11DF-D560-44D7-99CA-C425951A56D6
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermloadbalancerfrontendipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmLoadBalancerFrontendIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmLoadBalancerFrontendIpConfig.md
ms.openlocfilehash: 1a71b48387948d65ba0db24fdb2c236a11a9a44d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93456952"
---
# <span data-ttu-id="466d0-101">Remove-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="466d0-101">Remove-AzureRmLoadBalancerFrontendIpConfig</span></span>

## <span data-ttu-id="466d0-102">摘要</span><span class="sxs-lookup"><span data-stu-id="466d0-102">SYNOPSIS</span></span>
<span data-ttu-id="466d0-103">從負載平衡器移除前端 IP 配置。</span><span class="sxs-lookup"><span data-stu-id="466d0-103">Removes a front-end IP configuration from a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="466d0-104">句法</span><span class="sxs-lookup"><span data-stu-id="466d0-104">SYNTAX</span></span>

```
Remove-AzureRmLoadBalancerFrontendIpConfig -LoadBalancer <PSLoadBalancer> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="466d0-105">說明</span><span class="sxs-lookup"><span data-stu-id="466d0-105">DESCRIPTION</span></span>
<span data-ttu-id="466d0-106">**AzureRmLoadBalancerFrontendIpConfig** Cmdlet 會從 Azure 負載平衡器移除前端 IP 配置。</span><span class="sxs-lookup"><span data-stu-id="466d0-106">The **Remove-AzureRmLoadBalancerFrontendIpConfig** cmdlet removes a front-end IP configuration from an Azure load balancer.</span></span>

## <span data-ttu-id="466d0-107">示例</span><span class="sxs-lookup"><span data-stu-id="466d0-107">EXAMPLES</span></span>

### <span data-ttu-id="466d0-108">範例1：從負載平衡器移除前端 IP 配置</span><span class="sxs-lookup"><span data-stu-id="466d0-108">Example 1: Remove a front-end IP configuration from a load balancer</span></span>
```
PS C:\>$loadbalancer = Get-AzureRmLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:> Remove-AzureRmLoadBalancerFrontendIpConfig -Name "frontendName" -LoadBalancer $loadbalancer
```

<span data-ttu-id="466d0-109">第一個命令會取得與您想要移除的前端 IP 設定相關聯的負載平衡器，然後將它儲存在 $loadbalancer 變數中。</span><span class="sxs-lookup"><span data-stu-id="466d0-109">The first command gets the load balancer that is associated with the front-end IP configuration you want to remove, and then stores it in the $loadbalancer variable.</span></span>
<span data-ttu-id="466d0-110">第二個命令會從 $loadbalancer 中的負載平衡器移除關聯的前端 IP 設定。</span><span class="sxs-lookup"><span data-stu-id="466d0-110">The second command removes the associated frontend IP configuration from the load balancer in $loadbalancer.</span></span>

## <span data-ttu-id="466d0-111">參數</span><span class="sxs-lookup"><span data-stu-id="466d0-111">PARAMETERS</span></span>

### <span data-ttu-id="466d0-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="466d0-112">-DefaultProfile</span></span>
<span data-ttu-id="466d0-113">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="466d0-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="466d0-114">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="466d0-114">-LoadBalancer</span></span>
<span data-ttu-id="466d0-115">指定包含要移除之前端 IP 配置的負載平衡器。</span><span class="sxs-lookup"><span data-stu-id="466d0-115">Specifies the load balancer that contains the front-end IP configuration to remove.</span></span>

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

### <span data-ttu-id="466d0-116">-名稱</span><span class="sxs-lookup"><span data-stu-id="466d0-116">-Name</span></span>
<span data-ttu-id="466d0-117">指定要移除的前端 IP 位址配置名稱。</span><span class="sxs-lookup"><span data-stu-id="466d0-117">Specifies the name of the front-end IP address configuration to remove.</span></span>

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

### <span data-ttu-id="466d0-118">-確認</span><span class="sxs-lookup"><span data-stu-id="466d0-118">-Confirm</span></span>
<span data-ttu-id="466d0-119">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="466d0-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="466d0-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="466d0-120">-WhatIf</span></span>
<span data-ttu-id="466d0-121">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="466d0-121">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="466d0-122">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="466d0-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="466d0-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="466d0-123">CommonParameters</span></span>
<span data-ttu-id="466d0-124">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="466d0-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="466d0-125">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="466d0-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="466d0-126">輸入</span><span class="sxs-lookup"><span data-stu-id="466d0-126">INPUTS</span></span>

### <span data-ttu-id="466d0-127">PSLoadBalancer 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="466d0-127">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>
<span data-ttu-id="466d0-128">參數： LoadBalancer (ByValue) </span><span class="sxs-lookup"><span data-stu-id="466d0-128">Parameters: LoadBalancer (ByValue)</span></span>

## <span data-ttu-id="466d0-129">輸出</span><span class="sxs-lookup"><span data-stu-id="466d0-129">OUTPUTS</span></span>

### <span data-ttu-id="466d0-130">PSLoadBalancer 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="466d0-130">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="466d0-131">筆記</span><span class="sxs-lookup"><span data-stu-id="466d0-131">NOTES</span></span>

## <span data-ttu-id="466d0-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="466d0-132">RELATED LINKS</span></span>

[<span data-ttu-id="466d0-133">附加 AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="466d0-133">Add-AzureRmLoadBalancerFrontendIpConfig</span></span>](./Add-AzureRmLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="466d0-134">AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="466d0-134">Get-AzureRmLoadBalancer</span></span>](./Get-AzureRmLoadBalancer.md)

[<span data-ttu-id="466d0-135">AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="466d0-135">Get-AzureRmLoadBalancerFrontendIpConfig</span></span>](./Get-AzureRmLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="466d0-136">新-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="466d0-136">New-AzureRmLoadBalancerFrontendIpConfig</span></span>](./New-AzureRmLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="466d0-137">Set-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="466d0-137">Set-AzureRmLoadBalancerFrontendIpConfig</span></span>](./Set-AzureRmLoadBalancerFrontendIpConfig.md)


