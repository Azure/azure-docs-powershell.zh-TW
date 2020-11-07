---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 9EB11283-0189-4333-8142-DCC3F770F91A
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azloadbalancerbackendaddresspoolconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Add-AzLoadBalancerBackendAddressPoolConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Add-AzLoadBalancerBackendAddressPoolConfig.md
ms.openlocfilehash: e97e8f3ed5769e4f81175b29f097aa4946d28881
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/16/2020
ms.locfileid: "93794520"
---
# <span data-ttu-id="b127e-101">Add-AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="b127e-101">Add-AzLoadBalancerBackendAddressPoolConfig</span></span>

## <span data-ttu-id="b127e-102">摘要</span><span class="sxs-lookup"><span data-stu-id="b127e-102">SYNOPSIS</span></span>
<span data-ttu-id="b127e-103">將後端位址集區配置新增到負載平衡器。</span><span class="sxs-lookup"><span data-stu-id="b127e-103">Adds a backend address pool configuration to a load balancer.</span></span>

## <span data-ttu-id="b127e-104">句法</span><span class="sxs-lookup"><span data-stu-id="b127e-104">SYNTAX</span></span>

```
Add-AzLoadBalancerBackendAddressPoolConfig -Name <String> -LoadBalancer <PSLoadBalancer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b127e-105">說明</span><span class="sxs-lookup"><span data-stu-id="b127e-105">DESCRIPTION</span></span>
<span data-ttu-id="b127e-106">**AzLoadBalancerBackend** Cmdlet 會將後端位址集區新增至 Azure 負載平衡器。</span><span class="sxs-lookup"><span data-stu-id="b127e-106">The **Add-AzLoadBalancerBackend** cmdlet adds a backend address pool to an Azure load balancer.</span></span>

## <span data-ttu-id="b127e-107">示例</span><span class="sxs-lookup"><span data-stu-id="b127e-107">EXAMPLES</span></span>

### <span data-ttu-id="b127e-108">範例1將後端位址集區設定新增到負載平衡器</span><span class="sxs-lookup"><span data-stu-id="b127e-108">Example 1 Add a backend address pool configuration to a load balancer</span></span>
```
PS C:\>Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "myrg" | Add-AzLoadBalancerBackendAddressPoolConfig -Name "BackendAddressPool02" | Set-AzLoadBalancer
```

<span data-ttu-id="b127e-109">這個命令會取得名為 MyLoadBalancer 的負載平衡器，將名為 BackendAddressPool02 的後端位址集區新增至 MyLoadBalancer，然後使用 **Set-AzLoadBalancer** Cmdlet 來更新 MyLoadBalancer。</span><span class="sxs-lookup"><span data-stu-id="b127e-109">This command gets the load balancer named MyLoadBalancer, adds the backend address pool named BackendAddressPool02 to MyLoadBalancer, and then uses the **Set-AzLoadBalancer** cmdlet to update MyLoadBalancer.</span></span>

## <span data-ttu-id="b127e-110">參數</span><span class="sxs-lookup"><span data-stu-id="b127e-110">PARAMETERS</span></span>

### <span data-ttu-id="b127e-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b127e-111">-DefaultProfile</span></span>
<span data-ttu-id="b127e-112">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="b127e-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b127e-113">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="b127e-113">-LoadBalancer</span></span>
<span data-ttu-id="b127e-114">指定 **LoadBalancer** 物件。</span><span class="sxs-lookup"><span data-stu-id="b127e-114">Specifies a **LoadBalancer** object.</span></span>

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

### <span data-ttu-id="b127e-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="b127e-115">-Name</span></span>
<span data-ttu-id="b127e-116">指定要新增的後端位址集區配置名稱。</span><span class="sxs-lookup"><span data-stu-id="b127e-116">Specifies the name of the backend address pool configuration to add.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b127e-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b127e-117">CommonParameters</span></span>
<span data-ttu-id="b127e-118">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="b127e-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b127e-119">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="b127e-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b127e-120">輸入</span><span class="sxs-lookup"><span data-stu-id="b127e-120">INPUTS</span></span>

### <span data-ttu-id="b127e-121">PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="b127e-121">PSLoadBalancer</span></span>
<span data-ttu-id="b127e-122">形參 "LoadBalancer" 接受管線中 "PSLoadBalancer" 類型的值</span><span class="sxs-lookup"><span data-stu-id="b127e-122">Parameter 'LoadBalancer' accepts value of type 'PSLoadBalancer' from the pipeline</span></span>

## <span data-ttu-id="b127e-123">輸出</span><span class="sxs-lookup"><span data-stu-id="b127e-123">OUTPUTS</span></span>

### <span data-ttu-id="b127e-124">PSLoadBalancer 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="b127e-124">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="b127e-125">筆記</span><span class="sxs-lookup"><span data-stu-id="b127e-125">NOTES</span></span>

## <span data-ttu-id="b127e-126">相關連結</span><span class="sxs-lookup"><span data-stu-id="b127e-126">RELATED LINKS</span></span>

[<span data-ttu-id="b127e-127">AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="b127e-127">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="b127e-128">AzNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="b127e-128">Get-AzNetworkInterface</span></span>](./Get-AzNetworkInterface.md)

[<span data-ttu-id="b127e-129">AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="b127e-129">Get-AzLoadBalancerBackendAddressPoolConfig</span></span>](./Get-AzLoadBalancerBackendAddressPoolConfig.md)

[<span data-ttu-id="b127e-130">新-AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="b127e-130">New-AzLoadBalancerBackendAddressPoolConfig</span></span>](./New-AzLoadBalancerBackendAddressPoolConfig.md)

[<span data-ttu-id="b127e-131">移除-AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="b127e-131">Remove-AzLoadBalancerBackendAddressPoolConfig</span></span>](./Remove-AzLoadBalancerBackendAddressPoolConfig.md)


