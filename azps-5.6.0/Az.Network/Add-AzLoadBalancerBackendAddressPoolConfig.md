---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 9EB11283-0189-4333-8142-DCC3F770F91A
online version: https://docs.microsoft.com/powershell/module/az.network/add-azloadbalancerbackendaddresspoolconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzLoadBalancerBackendAddressPoolConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzLoadBalancerBackendAddressPoolConfig.md
ms.openlocfilehash: 2cda323e33b0c6a719b9a11bae461d5ced34862e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101917145"
---
# <span data-ttu-id="e1c5c-101">Add-AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="e1c5c-101">Add-AzLoadBalancerBackendAddressPoolConfig</span></span>

## <span data-ttu-id="e1c5c-102">簡介</span><span class="sxs-lookup"><span data-stu-id="e1c5c-102">SYNOPSIS</span></span>
<span data-ttu-id="e1c5c-103">將後端位址資料庫組新增到負載平衡器。</span><span class="sxs-lookup"><span data-stu-id="e1c5c-103">Adds a backend address pool configuration to a load balancer.</span></span>

## <span data-ttu-id="e1c5c-104">語法</span><span class="sxs-lookup"><span data-stu-id="e1c5c-104">SYNTAX</span></span>

```
Add-AzLoadBalancerBackendAddressPoolConfig -LoadBalancer <PSLoadBalancer> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e1c5c-105">描述</span><span class="sxs-lookup"><span data-stu-id="e1c5c-105">DESCRIPTION</span></span>
<span data-ttu-id="e1c5c-106">**Add-AzLoadBalancerBackend** Cmdlet 會新增後端位址資料庫至 Azure 負載平衡器。</span><span class="sxs-lookup"><span data-stu-id="e1c5c-106">The **Add-AzLoadBalancerBackend** cmdlet adds a backend address pool to an Azure load balancer.</span></span>

## <span data-ttu-id="e1c5c-107">例子</span><span class="sxs-lookup"><span data-stu-id="e1c5c-107">EXAMPLES</span></span>

### <span data-ttu-id="e1c5c-108">範例 1：將後端位址資料庫組新增到負載平衡器</span><span class="sxs-lookup"><span data-stu-id="e1c5c-108">Example 1: Add a backend address pool configuration to a load balancer</span></span>
```powershell
PS C:\>Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "myrg" | Add-AzLoadBalancerBackendAddressPoolConfig -Name "BackendAddressPool02" | Set-AzLoadBalancer
```

<span data-ttu-id="e1c5c-109">此命令會取得名為 MyLoadBalancer 的負載平衡器，將後端位址集區命名為後端AddressPool02 新增到 MyLoadBalancer，然後使用 **Set-AzLoadBalancer** Cmdlet 更新 MyLoadBalancer。</span><span class="sxs-lookup"><span data-stu-id="e1c5c-109">This command gets the load balancer named MyLoadBalancer, adds the backend address pool named BackendAddressPool02 to MyLoadBalancer, and then uses the **Set-AzLoadBalancer** cmdlet to update MyLoadBalancer.</span></span>

## <span data-ttu-id="e1c5c-110">參數</span><span class="sxs-lookup"><span data-stu-id="e1c5c-110">PARAMETERS</span></span>

### <span data-ttu-id="e1c5c-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e1c5c-111">-DefaultProfile</span></span>
<span data-ttu-id="e1c5c-112">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="e1c5c-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e1c5c-113">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="e1c5c-113">-LoadBalancer</span></span>
<span data-ttu-id="e1c5c-114">指定 **LoadBalancer** 物件。</span><span class="sxs-lookup"><span data-stu-id="e1c5c-114">Specifies a **LoadBalancer** object.</span></span>

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

### <span data-ttu-id="e1c5c-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="e1c5c-115">-Name</span></span>
<span data-ttu-id="e1c5c-116">指定要新增的後端位址資料庫組組組的名稱。</span><span class="sxs-lookup"><span data-stu-id="e1c5c-116">Specifies the name of the backend address pool configuration to add.</span></span>

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

### <span data-ttu-id="e1c5c-117">-確認</span><span class="sxs-lookup"><span data-stu-id="e1c5c-117">-Confirm</span></span>
<span data-ttu-id="e1c5c-118">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="e1c5c-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e1c5c-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e1c5c-119">-WhatIf</span></span>
<span data-ttu-id="e1c5c-120">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="e1c5c-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e1c5c-121">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="e1c5c-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e1c5c-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e1c5c-122">CommonParameters</span></span>
<span data-ttu-id="e1c5c-123">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="e1c5c-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e1c5c-124">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="e1c5c-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e1c5c-125">輸入</span><span class="sxs-lookup"><span data-stu-id="e1c5c-125">INPUTS</span></span>

### <span data-ttu-id="e1c5c-126">Microsoft.Azure.Commands.Network.models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="e1c5c-126">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="e1c5c-127">輸出</span><span class="sxs-lookup"><span data-stu-id="e1c5c-127">OUTPUTS</span></span>

### <span data-ttu-id="e1c5c-128">Microsoft.Azure.Commands.Network.models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="e1c5c-128">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="e1c5c-129">筆記</span><span class="sxs-lookup"><span data-stu-id="e1c5c-129">NOTES</span></span>

## <span data-ttu-id="e1c5c-130">相關連結</span><span class="sxs-lookup"><span data-stu-id="e1c5c-130">RELATED LINKS</span></span>

[<span data-ttu-id="e1c5c-131">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="e1c5c-131">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="e1c5c-132">Get-AzNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="e1c5c-132">Get-AzNetworkInterface</span></span>](./Get-AzNetworkInterface.md)

[<span data-ttu-id="e1c5c-133">Get-AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="e1c5c-133">Get-AzLoadBalancerBackendAddressPoolConfig</span></span>](./Get-AzLoadBalancerBackendAddressPoolConfig.md)

[<span data-ttu-id="e1c5c-134">New-AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="e1c5c-134">New-AzLoadBalancerBackendAddressPoolConfig</span></span>](./New-AzLoadBalancerBackendAddressPoolConfig.md)

[<span data-ttu-id="e1c5c-135">Remove-AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="e1c5c-135">Remove-AzLoadBalancerBackendAddressPoolConfig</span></span>](./Remove-AzLoadBalancerBackendAddressPoolConfig.md)


