---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: F965A9DE-645C-471B-84E8-58D648B1CA57
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azloadbalancerbackendaddresspoolconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzLoadBalancerBackendAddressPoolConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzLoadBalancerBackendAddressPoolConfig.md
ms.openlocfilehash: ba4251615bd732526ca88f085cf2c7f2d2bf284d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93621613"
---
# <span data-ttu-id="a76ae-101">Remove-AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="a76ae-101">Remove-AzLoadBalancerBackendAddressPoolConfig</span></span>

## <span data-ttu-id="a76ae-102">摘要</span><span class="sxs-lookup"><span data-stu-id="a76ae-102">SYNOPSIS</span></span>
<span data-ttu-id="a76ae-103">從負載平衡器移除後端位址集區配置。</span><span class="sxs-lookup"><span data-stu-id="a76ae-103">Removes a backend address pool configuration from a load balancer.</span></span>

## <span data-ttu-id="a76ae-104">句法</span><span class="sxs-lookup"><span data-stu-id="a76ae-104">SYNTAX</span></span>

```
Remove-AzLoadBalancerBackendAddressPoolConfig -LoadBalancer <PSLoadBalancer> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a76ae-105">說明</span><span class="sxs-lookup"><span data-stu-id="a76ae-105">DESCRIPTION</span></span>
<span data-ttu-id="a76ae-106">**AzLoadBalancerBackendAddressPoolConfig** Cmdlet 會從負載平衡器中移除後端位址集區。</span><span class="sxs-lookup"><span data-stu-id="a76ae-106">The **Remove-AzLoadBalancerBackendAddressPoolConfig** cmdlet removes a backend address pool from a load balancer.</span></span>

## <span data-ttu-id="a76ae-107">示例</span><span class="sxs-lookup"><span data-stu-id="a76ae-107">EXAMPLES</span></span>

### <span data-ttu-id="a76ae-108">範例1：從負載平衡器移除後端位址集區設定</span><span class="sxs-lookup"><span data-stu-id="a76ae-108">Example 1: Remove a backend address pool configuration from a load balancer</span></span>
```
PS C:\>Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup" | Remove-AzLoadBalancerBackendAddressPoolConfig -Name "BackendAddressPool02" | Set-AzLoadBalancer
```

<span data-ttu-id="a76ae-109">這個命令會取得名為 MyLoadBalancer 的負載平衡器，並將它傳遞給 **Remove-AzLoadBalancerBackendAddressPoolConfig** ，這會從 MyLoadBalancer 中移除 BackendAddressPool02 設定。</span><span class="sxs-lookup"><span data-stu-id="a76ae-109">This command gets the load balancer named MyLoadBalancer and passes it to **Remove-AzLoadBalancerBackendAddressPoolConfig** , which removes the BackendAddressPool02 configuration from MyLoadBalancer.</span></span>
<span data-ttu-id="a76ae-110">最後，Set-AzLoadBalancer Cmdlet 更新 MyLoadBalancer。</span><span class="sxs-lookup"><span data-stu-id="a76ae-110">Finally, the Set-AzLoadBalancer cmdlet updates MyLoadBalancer.</span></span>
<span data-ttu-id="a76ae-111">請注意，後端位址集區配置必須存在，才能刪除。</span><span class="sxs-lookup"><span data-stu-id="a76ae-111">Note that a backend address pool configuration must exist before you can delete it.</span></span>

## <span data-ttu-id="a76ae-112">參數</span><span class="sxs-lookup"><span data-stu-id="a76ae-112">PARAMETERS</span></span>

### <span data-ttu-id="a76ae-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a76ae-113">-DefaultProfile</span></span>
<span data-ttu-id="a76ae-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="a76ae-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a76ae-115">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="a76ae-115">-LoadBalancer</span></span>
<span data-ttu-id="a76ae-116">指定包含要移除之後端位址集區的負載平衡器。</span><span class="sxs-lookup"><span data-stu-id="a76ae-116">Specifies the load balancer that contains the backend address pool to remove.</span></span>

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

### <span data-ttu-id="a76ae-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="a76ae-117">-Name</span></span>
<span data-ttu-id="a76ae-118">指定此 Cmdlet 移除之後端位址集區的名稱。</span><span class="sxs-lookup"><span data-stu-id="a76ae-118">Specifies the name of the backend address pool that this cmdlet removes.</span></span>

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

### <span data-ttu-id="a76ae-119">-確認</span><span class="sxs-lookup"><span data-stu-id="a76ae-119">-Confirm</span></span>
<span data-ttu-id="a76ae-120">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="a76ae-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a76ae-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a76ae-121">-WhatIf</span></span>
<span data-ttu-id="a76ae-122">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="a76ae-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a76ae-123">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="a76ae-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a76ae-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a76ae-124">CommonParameters</span></span>
<span data-ttu-id="a76ae-125">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="a76ae-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a76ae-126">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="a76ae-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a76ae-127">輸入</span><span class="sxs-lookup"><span data-stu-id="a76ae-127">INPUTS</span></span>

### <span data-ttu-id="a76ae-128">PSLoadBalancer 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="a76ae-128">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="a76ae-129">輸出</span><span class="sxs-lookup"><span data-stu-id="a76ae-129">OUTPUTS</span></span>

### <span data-ttu-id="a76ae-130">PSLoadBalancer 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="a76ae-130">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="a76ae-131">筆記</span><span class="sxs-lookup"><span data-stu-id="a76ae-131">NOTES</span></span>

## <span data-ttu-id="a76ae-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="a76ae-132">RELATED LINKS</span></span>

[<span data-ttu-id="a76ae-133">附加 AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="a76ae-133">Add-AzLoadBalancerBackendAddressPoolConfig</span></span>](./Add-AzLoadBalancerBackendAddressPoolConfig.md)

[<span data-ttu-id="a76ae-134">AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="a76ae-134">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="a76ae-135">AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="a76ae-135">Get-AzLoadBalancerBackendAddressPoolConfig</span></span>](./Get-AzLoadBalancerBackendAddressPoolConfig.md)

[<span data-ttu-id="a76ae-136">新-AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="a76ae-136">New-AzLoadBalancerBackendAddressPoolConfig</span></span>](./New-AzLoadBalancerBackendAddressPoolConfig.md)


