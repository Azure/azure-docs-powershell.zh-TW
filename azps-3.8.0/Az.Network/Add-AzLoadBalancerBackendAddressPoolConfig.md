---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 9EB11283-0189-4333-8142-DCC3F770F91A
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azloadbalancerbackendaddresspoolconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzLoadBalancerBackendAddressPoolConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzLoadBalancerBackendAddressPoolConfig.md
ms.openlocfilehash: a1e0f8abdc8951155ab56b85f516145c9b6b1d1a
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93958011"
---
# <span data-ttu-id="559c1-101">Add-AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="559c1-101">Add-AzLoadBalancerBackendAddressPoolConfig</span></span>

## <span data-ttu-id="559c1-102">摘要</span><span class="sxs-lookup"><span data-stu-id="559c1-102">SYNOPSIS</span></span>
<span data-ttu-id="559c1-103">將後端位址集區配置新增到負載平衡器。</span><span class="sxs-lookup"><span data-stu-id="559c1-103">Adds a backend address pool configuration to a load balancer.</span></span>

## <span data-ttu-id="559c1-104">句法</span><span class="sxs-lookup"><span data-stu-id="559c1-104">SYNTAX</span></span>

```
Add-AzLoadBalancerBackendAddressPoolConfig -LoadBalancer <PSLoadBalancer> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="559c1-105">說明</span><span class="sxs-lookup"><span data-stu-id="559c1-105">DESCRIPTION</span></span>
<span data-ttu-id="559c1-106">**AzLoadBalancerBackend** Cmdlet 會將後端位址集區新增至 Azure 負載平衡器。</span><span class="sxs-lookup"><span data-stu-id="559c1-106">The **Add-AzLoadBalancerBackend** cmdlet adds a backend address pool to an Azure load balancer.</span></span>

## <span data-ttu-id="559c1-107">示例</span><span class="sxs-lookup"><span data-stu-id="559c1-107">EXAMPLES</span></span>

### <span data-ttu-id="559c1-108">範例1將後端位址集區設定新增到負載平衡器</span><span class="sxs-lookup"><span data-stu-id="559c1-108">Example 1 Add a backend address pool configuration to a load balancer</span></span>
```
PS C:\>Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "myrg" | Add-AzLoadBalancerBackendAddressPoolConfig -Name "BackendAddressPool02" | Set-AzLoadBalancer
```

<span data-ttu-id="559c1-109">這個命令會取得名為 MyLoadBalancer 的負載平衡器，將名為 BackendAddressPool02 的後端位址集區新增至 MyLoadBalancer，然後使用 **Set-AzLoadBalancer** Cmdlet 來更新 MyLoadBalancer。</span><span class="sxs-lookup"><span data-stu-id="559c1-109">This command gets the load balancer named MyLoadBalancer, adds the backend address pool named BackendAddressPool02 to MyLoadBalancer, and then uses the **Set-AzLoadBalancer** cmdlet to update MyLoadBalancer.</span></span>

## <span data-ttu-id="559c1-110">參數</span><span class="sxs-lookup"><span data-stu-id="559c1-110">PARAMETERS</span></span>

### <span data-ttu-id="559c1-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="559c1-111">-DefaultProfile</span></span>
<span data-ttu-id="559c1-112">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="559c1-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="559c1-113">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="559c1-113">-LoadBalancer</span></span>
<span data-ttu-id="559c1-114">指定 **LoadBalancer** 物件。</span><span class="sxs-lookup"><span data-stu-id="559c1-114">Specifies a **LoadBalancer** object.</span></span>

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

### <span data-ttu-id="559c1-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="559c1-115">-Name</span></span>
<span data-ttu-id="559c1-116">指定要新增的後端位址集區配置名稱。</span><span class="sxs-lookup"><span data-stu-id="559c1-116">Specifies the name of the backend address pool configuration to add.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="559c1-117">-確認</span><span class="sxs-lookup"><span data-stu-id="559c1-117">-Confirm</span></span>
<span data-ttu-id="559c1-118">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="559c1-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="559c1-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="559c1-119">-WhatIf</span></span>
<span data-ttu-id="559c1-120">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="559c1-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="559c1-121">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="559c1-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="559c1-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="559c1-122">CommonParameters</span></span>
<span data-ttu-id="559c1-123">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="559c1-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="559c1-124">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="559c1-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="559c1-125">輸入</span><span class="sxs-lookup"><span data-stu-id="559c1-125">INPUTS</span></span>

### <span data-ttu-id="559c1-126">PSLoadBalancer 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="559c1-126">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="559c1-127">輸出</span><span class="sxs-lookup"><span data-stu-id="559c1-127">OUTPUTS</span></span>

### <span data-ttu-id="559c1-128">PSLoadBalancer 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="559c1-128">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="559c1-129">筆記</span><span class="sxs-lookup"><span data-stu-id="559c1-129">NOTES</span></span>

## <span data-ttu-id="559c1-130">相關連結</span><span class="sxs-lookup"><span data-stu-id="559c1-130">RELATED LINKS</span></span>

[<span data-ttu-id="559c1-131">AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="559c1-131">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="559c1-132">AzNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="559c1-132">Get-AzNetworkInterface</span></span>](./Get-AzNetworkInterface.md)

[<span data-ttu-id="559c1-133">AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="559c1-133">Get-AzLoadBalancerBackendAddressPoolConfig</span></span>](./Get-AzLoadBalancerBackendAddressPoolConfig.md)

[<span data-ttu-id="559c1-134">新-AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="559c1-134">New-AzLoadBalancerBackendAddressPoolConfig</span></span>](./New-AzLoadBalancerBackendAddressPoolConfig.md)

[<span data-ttu-id="559c1-135">移除-AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="559c1-135">Remove-AzLoadBalancerBackendAddressPoolConfig</span></span>](./Remove-AzLoadBalancerBackendAddressPoolConfig.md)


