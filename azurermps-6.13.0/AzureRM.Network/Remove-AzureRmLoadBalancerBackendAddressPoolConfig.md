---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: F965A9DE-645C-471B-84E8-58D648B1CA57
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermloadbalancerbackendaddresspoolconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmLoadBalancerBackendAddressPoolConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmLoadBalancerBackendAddressPoolConfig.md
ms.openlocfilehash: 065aa3718f1a66949265e7dca39880c1eff21fa0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93623916"
---
# <span data-ttu-id="a2b60-101">Remove-AzureRmLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="a2b60-101">Remove-AzureRmLoadBalancerBackendAddressPoolConfig</span></span>

## <span data-ttu-id="a2b60-102">摘要</span><span class="sxs-lookup"><span data-stu-id="a2b60-102">SYNOPSIS</span></span>
<span data-ttu-id="a2b60-103">從負載平衡器移除後端位址集區配置。</span><span class="sxs-lookup"><span data-stu-id="a2b60-103">Removes a backend address pool configuration from a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a2b60-104">句法</span><span class="sxs-lookup"><span data-stu-id="a2b60-104">SYNTAX</span></span>

```
Remove-AzureRmLoadBalancerBackendAddressPoolConfig -LoadBalancer <PSLoadBalancer> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a2b60-105">說明</span><span class="sxs-lookup"><span data-stu-id="a2b60-105">DESCRIPTION</span></span>
<span data-ttu-id="a2b60-106">**AzureRmLoadBalancerBackendAddressPoolConfig** Cmdlet 會從負載平衡器中移除後端位址集區。</span><span class="sxs-lookup"><span data-stu-id="a2b60-106">The **Remove-AzureRmLoadBalancerBackendAddressPoolConfig** cmdlet removes a backend address pool from a load balancer.</span></span>

## <span data-ttu-id="a2b60-107">示例</span><span class="sxs-lookup"><span data-stu-id="a2b60-107">EXAMPLES</span></span>

### <span data-ttu-id="a2b60-108">範例1：從負載平衡器移除後端位址集區設定</span><span class="sxs-lookup"><span data-stu-id="a2b60-108">Example 1: Remove a backend address pool configuration from a load balancer</span></span>
```
PS C:\>Get-AzureRmLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup" | Remove-AzureRmLoadBalancerBackendAddressPoolConfig -Name "BackendAddressPool02" | Set-AzureRmLoadBalancer
```

<span data-ttu-id="a2b60-109">這個命令會取得名為 MyLoadBalancer 的負載平衡器，並將它傳遞給 **Remove-AzureRmLoadBalancerBackendAddressPoolConfig** ，這會從 MyLoadBalancer 中移除 BackendAddressPool02 設定。</span><span class="sxs-lookup"><span data-stu-id="a2b60-109">This command gets the load balancer named MyLoadBalancer and passes it to **Remove-AzureRmLoadBalancerBackendAddressPoolConfig** , which removes the BackendAddressPool02 configuration from MyLoadBalancer.</span></span>
<span data-ttu-id="a2b60-110">最後，Set-AzureRmLoadBalancer Cmdlet 更新 MyLoadBalancer。</span><span class="sxs-lookup"><span data-stu-id="a2b60-110">Finally, the Set-AzureRmLoadBalancer cmdlet updates MyLoadBalancer.</span></span>
<span data-ttu-id="a2b60-111">請注意，後端位址集區配置必須存在，才能刪除。</span><span class="sxs-lookup"><span data-stu-id="a2b60-111">Note that a backend address pool configuration must exist before you can delete it.</span></span>

## <span data-ttu-id="a2b60-112">參數</span><span class="sxs-lookup"><span data-stu-id="a2b60-112">PARAMETERS</span></span>

### <span data-ttu-id="a2b60-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a2b60-113">-DefaultProfile</span></span>
<span data-ttu-id="a2b60-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="a2b60-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a2b60-115">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="a2b60-115">-LoadBalancer</span></span>
<span data-ttu-id="a2b60-116">指定包含要移除之後端位址集區的負載平衡器。</span><span class="sxs-lookup"><span data-stu-id="a2b60-116">Specifies the load balancer that contains the backend address pool to remove.</span></span>

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

### <span data-ttu-id="a2b60-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="a2b60-117">-Name</span></span>
<span data-ttu-id="a2b60-118">指定此 Cmdlet 移除之後端位址集區的名稱。</span><span class="sxs-lookup"><span data-stu-id="a2b60-118">Specifies the name of the backend address pool that this cmdlet removes.</span></span>

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

### <span data-ttu-id="a2b60-119">-確認</span><span class="sxs-lookup"><span data-stu-id="a2b60-119">-Confirm</span></span>
<span data-ttu-id="a2b60-120">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="a2b60-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a2b60-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a2b60-121">-WhatIf</span></span>
<span data-ttu-id="a2b60-122">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="a2b60-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a2b60-123">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="a2b60-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a2b60-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a2b60-124">CommonParameters</span></span>
<span data-ttu-id="a2b60-125">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="a2b60-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a2b60-126">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="a2b60-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a2b60-127">輸入</span><span class="sxs-lookup"><span data-stu-id="a2b60-127">INPUTS</span></span>

### <span data-ttu-id="a2b60-128">PSLoadBalancer 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="a2b60-128">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>
<span data-ttu-id="a2b60-129">參數： LoadBalancer (ByValue) </span><span class="sxs-lookup"><span data-stu-id="a2b60-129">Parameters: LoadBalancer (ByValue)</span></span>

## <span data-ttu-id="a2b60-130">輸出</span><span class="sxs-lookup"><span data-stu-id="a2b60-130">OUTPUTS</span></span>

### <span data-ttu-id="a2b60-131">PSLoadBalancer 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="a2b60-131">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="a2b60-132">筆記</span><span class="sxs-lookup"><span data-stu-id="a2b60-132">NOTES</span></span>

## <span data-ttu-id="a2b60-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="a2b60-133">RELATED LINKS</span></span>

[<span data-ttu-id="a2b60-134">附加 AzureRmLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="a2b60-134">Add-AzureRmLoadBalancerBackendAddressPoolConfig</span></span>](./Add-AzureRmLoadBalancerBackendAddressPoolConfig.md)

[<span data-ttu-id="a2b60-135">AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="a2b60-135">Get-AzureRmLoadBalancer</span></span>](./Get-AzureRmLoadBalancer.md)

[<span data-ttu-id="a2b60-136">AzureRmLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="a2b60-136">Get-AzureRmLoadBalancerBackendAddressPoolConfig</span></span>](./Get-AzureRmLoadBalancerBackendAddressPoolConfig.md)

[<span data-ttu-id="a2b60-137">新-AzureRmLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="a2b60-137">New-AzureRmLoadBalancerBackendAddressPoolConfig</span></span>](./New-AzureRmLoadBalancerBackendAddressPoolConfig.md)


