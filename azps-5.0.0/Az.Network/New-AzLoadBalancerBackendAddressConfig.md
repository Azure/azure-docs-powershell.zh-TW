---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azloadbalancerbackendaddressconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLoadBalancerBackendAddressConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLoadBalancerBackendAddressConfig.md
ms.openlocfilehash: 7d373092f850dd25abe5b6d913ddcf2572d4be94
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94287459"
---
# <span data-ttu-id="0af20-101">New-AzLoadBalancerBackendAddressConfig</span><span class="sxs-lookup"><span data-stu-id="0af20-101">New-AzLoadBalancerBackendAddressConfig</span></span>

## <span data-ttu-id="0af20-102">摘要</span><span class="sxs-lookup"><span data-stu-id="0af20-102">SYNOPSIS</span></span>
<span data-ttu-id="0af20-103">傳回負載平衡器後端位址 config。</span><span class="sxs-lookup"><span data-stu-id="0af20-103">Returns a load balancer backend address config.</span></span> 

## <span data-ttu-id="0af20-104">句法</span><span class="sxs-lookup"><span data-stu-id="0af20-104">SYNTAX</span></span>

```
New-AzLoadBalancerBackendAddressConfig -IpAddress <String> -Name <String> -VirtualNetworkId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0af20-105">說明</span><span class="sxs-lookup"><span data-stu-id="0af20-105">DESCRIPTION</span></span>
<span data-ttu-id="0af20-106">傳回負載平衡器後端位址 config。</span><span class="sxs-lookup"><span data-stu-id="0af20-106">Returns a load balancer backend address config.</span></span> 

## <span data-ttu-id="0af20-107">示例</span><span class="sxs-lookup"><span data-stu-id="0af20-107">EXAMPLES</span></span>

### <span data-ttu-id="0af20-108">範例1</span><span class="sxs-lookup"><span data-stu-id="0af20-108">Example 1</span></span>
### <span data-ttu-id="0af20-109">範例2：使用虛擬網路參照的新 loadbalancer 位址配置</span><span class="sxs-lookup"><span data-stu-id="0af20-109">Example 2: New loadbalancer address config with virtual network reference</span></span>
```powershell
PS C:\> $virtualNetwork = Get-AzVirtualNetwork -Name $vnetName -ResourceGroupName $resourceGroup
New-AzLoadBalancerBackendAddressConfig -IpAddress "10.0.0.5" -Name "TestVNetRef" -VirtualNetworkId $virtualNetwork.Id
```

## <span data-ttu-id="0af20-110">參數</span><span class="sxs-lookup"><span data-stu-id="0af20-110">PARAMETERS</span></span>

### <span data-ttu-id="0af20-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0af20-111">-DefaultProfile</span></span>
<span data-ttu-id="0af20-112">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="0af20-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0af20-113">-IpAddress</span><span class="sxs-lookup"><span data-stu-id="0af20-113">-IpAddress</span></span>
<span data-ttu-id="0af20-114">要新增到後端池的 IPAddress</span><span class="sxs-lookup"><span data-stu-id="0af20-114">The IPAddress to add to the backend pool</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0af20-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="0af20-115">-Name</span></span>
<span data-ttu-id="0af20-116">後端位址 config 的名稱</span><span class="sxs-lookup"><span data-stu-id="0af20-116">The name of the Backend Address config</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0af20-117">-VirtualNetworkId</span><span class="sxs-lookup"><span data-stu-id="0af20-117">-VirtualNetworkId</span></span>
<span data-ttu-id="0af20-118">與後端位址 config 相關聯的虛擬網路</span><span class="sxs-lookup"><span data-stu-id="0af20-118">The virtual network associated with Backend Address config</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0af20-119">-確認</span><span class="sxs-lookup"><span data-stu-id="0af20-119">-Confirm</span></span>
<span data-ttu-id="0af20-120">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="0af20-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0af20-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0af20-121">-WhatIf</span></span>
<span data-ttu-id="0af20-122">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="0af20-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="0af20-123">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="0af20-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0af20-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0af20-124">CommonParameters</span></span>
<span data-ttu-id="0af20-125">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="0af20-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0af20-126">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="0af20-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0af20-127">輸入</span><span class="sxs-lookup"><span data-stu-id="0af20-127">INPUTS</span></span>

### <span data-ttu-id="0af20-128">System.object</span><span class="sxs-lookup"><span data-stu-id="0af20-128">System.String</span></span>

### <span data-ttu-id="0af20-129">PSVirtualNetwork 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="0af20-129">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

## <span data-ttu-id="0af20-130">輸出</span><span class="sxs-lookup"><span data-stu-id="0af20-130">OUTPUTS</span></span>

### <span data-ttu-id="0af20-131">PSLoadBalancerBackendAddress 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="0af20-131">Microsoft.Azure.Commands.Network.Models.PSLoadBalancerBackendAddress</span></span>

## <span data-ttu-id="0af20-132">筆記</span><span class="sxs-lookup"><span data-stu-id="0af20-132">NOTES</span></span>

## <span data-ttu-id="0af20-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="0af20-133">RELATED LINKS</span></span>
