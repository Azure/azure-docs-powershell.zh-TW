---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: F965A9DE-645C-471B-84E8-58D648B1CA57
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azloadbalancerbackendaddresspoolconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzLoadBalancerBackendAddressPoolConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzLoadBalancerBackendAddressPoolConfig.md
ms.openlocfilehash: 30abb6f2d11eeae9749e7285a91ddeb93a1bf743
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/16/2020
ms.locfileid: "93794182"
---
# <span data-ttu-id="b96b6-101">Remove-AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="b96b6-101">Remove-AzLoadBalancerBackendAddressPoolConfig</span></span>

## <span data-ttu-id="b96b6-102">摘要</span><span class="sxs-lookup"><span data-stu-id="b96b6-102">SYNOPSIS</span></span>
<span data-ttu-id="b96b6-103">從負載平衡器移除後端位址集區配置。</span><span class="sxs-lookup"><span data-stu-id="b96b6-103">Removes a backend address pool configuration from a load balancer.</span></span>

## <span data-ttu-id="b96b6-104">句法</span><span class="sxs-lookup"><span data-stu-id="b96b6-104">SYNTAX</span></span>

```
Remove-AzLoadBalancerBackendAddressPoolConfig [-Name <String>] -LoadBalancer <PSLoadBalancer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b96b6-105">說明</span><span class="sxs-lookup"><span data-stu-id="b96b6-105">DESCRIPTION</span></span>
<span data-ttu-id="b96b6-106">**AzLoadBalancerBackendAddressPoolConfig** Cmdlet 會從負載平衡器中移除後端位址集區。</span><span class="sxs-lookup"><span data-stu-id="b96b6-106">The **Remove-AzLoadBalancerBackendAddressPoolConfig** cmdlet removes a backend address pool from a load balancer.</span></span>

## <span data-ttu-id="b96b6-107">示例</span><span class="sxs-lookup"><span data-stu-id="b96b6-107">EXAMPLES</span></span>

### <span data-ttu-id="b96b6-108">範例1：從負載平衡器移除後端位址集區設定</span><span class="sxs-lookup"><span data-stu-id="b96b6-108">Example 1: Remove a backend address pool configuration from a load balancer</span></span>
```
PS C:\>Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup" | Remove-AzLoadBalancerBackendAddressPoolConfig -Name "BackendAddressPool02" | Set-AzLoadBalancer
```

<span data-ttu-id="b96b6-109">這個命令會取得名為 MyLoadBalancer 的負載平衡器，並將它傳遞給 **Remove-AzLoadBalancerBackendAddressPoolConfig** ，這會從 MyLoadBalancer 中移除 BackendAddressPool02 設定。</span><span class="sxs-lookup"><span data-stu-id="b96b6-109">This command gets the load balancer named MyLoadBalancer and passes it to **Remove-AzLoadBalancerBackendAddressPoolConfig** , which removes the BackendAddressPool02 configuration from MyLoadBalancer.</span></span>
<span data-ttu-id="b96b6-110">最後，Set-AzLoadBalancer Cmdlet 更新 MyLoadBalancer。</span><span class="sxs-lookup"><span data-stu-id="b96b6-110">Finally, the Set-AzLoadBalancer cmdlet updates MyLoadBalancer.</span></span>
<span data-ttu-id="b96b6-111">請注意，後端位址集區配置必須存在，才能刪除。</span><span class="sxs-lookup"><span data-stu-id="b96b6-111">Note that a backend address pool configuration must exist before you can delete it.</span></span>

## <span data-ttu-id="b96b6-112">參數</span><span class="sxs-lookup"><span data-stu-id="b96b6-112">PARAMETERS</span></span>

### <span data-ttu-id="b96b6-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b96b6-113">-DefaultProfile</span></span>
<span data-ttu-id="b96b6-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="b96b6-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b96b6-115">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="b96b6-115">-LoadBalancer</span></span>
<span data-ttu-id="b96b6-116">指定包含要移除之後端位址集區的負載平衡器。</span><span class="sxs-lookup"><span data-stu-id="b96b6-116">Specifies the load balancer that contains the backend address pool to remove.</span></span>

```yaml
Type: PSLoadBalancer
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b96b6-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="b96b6-117">-Name</span></span>
<span data-ttu-id="b96b6-118">指定此 Cmdlet 移除之後端位址集區的名稱。</span><span class="sxs-lookup"><span data-stu-id="b96b6-118">Specifies the name of the backend address pool that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b96b6-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b96b6-119">CommonParameters</span></span>
<span data-ttu-id="b96b6-120">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="b96b6-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b96b6-121">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="b96b6-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b96b6-122">輸入</span><span class="sxs-lookup"><span data-stu-id="b96b6-122">INPUTS</span></span>

### <span data-ttu-id="b96b6-123">PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="b96b6-123">PSLoadBalancer</span></span>
<span data-ttu-id="b96b6-124">形參 "LoadBalancer" 接受管線中 "PSLoadBalancer" 類型的值</span><span class="sxs-lookup"><span data-stu-id="b96b6-124">Parameter 'LoadBalancer' accepts value of type 'PSLoadBalancer' from the pipeline</span></span>

## <span data-ttu-id="b96b6-125">輸出</span><span class="sxs-lookup"><span data-stu-id="b96b6-125">OUTPUTS</span></span>

### <span data-ttu-id="b96b6-126">PSLoadBalancer 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="b96b6-126">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="b96b6-127">筆記</span><span class="sxs-lookup"><span data-stu-id="b96b6-127">NOTES</span></span>

## <span data-ttu-id="b96b6-128">相關連結</span><span class="sxs-lookup"><span data-stu-id="b96b6-128">RELATED LINKS</span></span>

[<span data-ttu-id="b96b6-129">附加 AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="b96b6-129">Add-AzLoadBalancerBackendAddressPoolConfig</span></span>](./Add-AzLoadBalancerBackendAddressPoolConfig.md)

[<span data-ttu-id="b96b6-130">AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="b96b6-130">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="b96b6-131">AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="b96b6-131">Get-AzLoadBalancerBackendAddressPoolConfig</span></span>](./Get-AzLoadBalancerBackendAddressPoolConfig.md)

[<span data-ttu-id="b96b6-132">新-AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="b96b6-132">New-AzLoadBalancerBackendAddressPoolConfig</span></span>](./New-AzLoadBalancerBackendAddressPoolConfig.md)


