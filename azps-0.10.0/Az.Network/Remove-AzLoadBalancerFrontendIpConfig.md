---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 5F8E11DF-D560-44D7-99CA-C425951A56D6
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azloadbalancerfrontendipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzLoadBalancerFrontendIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzLoadBalancerFrontendIpConfig.md
ms.openlocfilehash: b9782d56fb18f0f00c52e9ff37ef0d62a609f980
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/16/2020
ms.locfileid: "93794179"
---
# <span data-ttu-id="e95fe-101">Remove-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="e95fe-101">Remove-AzLoadBalancerFrontendIpConfig</span></span>

## <span data-ttu-id="e95fe-102">摘要</span><span class="sxs-lookup"><span data-stu-id="e95fe-102">SYNOPSIS</span></span>
<span data-ttu-id="e95fe-103">從負載平衡器移除前端 IP 配置。</span><span class="sxs-lookup"><span data-stu-id="e95fe-103">Removes a front-end IP configuration from a load balancer.</span></span>

## <span data-ttu-id="e95fe-104">句法</span><span class="sxs-lookup"><span data-stu-id="e95fe-104">SYNTAX</span></span>

```
Remove-AzLoadBalancerFrontendIpConfig [-Name <String>] -LoadBalancer <PSLoadBalancer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e95fe-105">說明</span><span class="sxs-lookup"><span data-stu-id="e95fe-105">DESCRIPTION</span></span>
<span data-ttu-id="e95fe-106">**AzLoadBalancerFrontendIpConfig** Cmdlet 會從 Azure 負載平衡器移除前端 IP 配置。</span><span class="sxs-lookup"><span data-stu-id="e95fe-106">The **Remove-AzLoadBalancerFrontendIpConfig** cmdlet removes a front-end IP configuration from an Azure load balancer.</span></span>

## <span data-ttu-id="e95fe-107">示例</span><span class="sxs-lookup"><span data-stu-id="e95fe-107">EXAMPLES</span></span>

### <span data-ttu-id="e95fe-108">範例1：從負載平衡器移除前端 IP 配置</span><span class="sxs-lookup"><span data-stu-id="e95fe-108">Example 1: Remove a front-end IP configuration from a load balancer</span></span>
```
PS C:\>$loadbalancer = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:> Remove-AzLoadBalancerFrontendIpConfig -Name "frontendName" -LoadBalancer $loadbalancer
```

<span data-ttu-id="e95fe-109">第一個命令會取得與您想要移除的前端 IP 設定相關聯的負載平衡器，然後將它儲存在 $loadbalancer 變數中。</span><span class="sxs-lookup"><span data-stu-id="e95fe-109">The first command gets the load balancer that is associated with the front-end IP configuration you want to remove, and then stores it in the $loadbalancer variable.</span></span>

<span data-ttu-id="e95fe-110">第二個命令會從 $loadbalancer 中的負載平衡器移除關聯的前端 IP 設定。</span><span class="sxs-lookup"><span data-stu-id="e95fe-110">The second command removes the associated frontend IP configuration from the load balancer in $loadbalancer.</span></span>

## <span data-ttu-id="e95fe-111">參數</span><span class="sxs-lookup"><span data-stu-id="e95fe-111">PARAMETERS</span></span>

### <span data-ttu-id="e95fe-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e95fe-112">-DefaultProfile</span></span>
<span data-ttu-id="e95fe-113">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="e95fe-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e95fe-114">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="e95fe-114">-LoadBalancer</span></span>
<span data-ttu-id="e95fe-115">指定包含要移除之前端 IP 配置的負載平衡器。</span><span class="sxs-lookup"><span data-stu-id="e95fe-115">Specifies the load balancer that contains the front-end IP configuration to remove.</span></span>

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

### <span data-ttu-id="e95fe-116">-名稱</span><span class="sxs-lookup"><span data-stu-id="e95fe-116">-Name</span></span>
<span data-ttu-id="e95fe-117">指定要移除的前端 IP 位址配置名稱。</span><span class="sxs-lookup"><span data-stu-id="e95fe-117">Specifies the name of the front-end IP address configuration to remove.</span></span>

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

### <span data-ttu-id="e95fe-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e95fe-118">CommonParameters</span></span>
<span data-ttu-id="e95fe-119">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="e95fe-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e95fe-120">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="e95fe-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e95fe-121">輸入</span><span class="sxs-lookup"><span data-stu-id="e95fe-121">INPUTS</span></span>

### <span data-ttu-id="e95fe-122">PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="e95fe-122">PSLoadBalancer</span></span>
<span data-ttu-id="e95fe-123">形參 "LoadBalancer" 接受管線中 "PSLoadBalancer" 類型的值</span><span class="sxs-lookup"><span data-stu-id="e95fe-123">Parameter 'LoadBalancer' accepts value of type 'PSLoadBalancer' from the pipeline</span></span>

## <span data-ttu-id="e95fe-124">輸出</span><span class="sxs-lookup"><span data-stu-id="e95fe-124">OUTPUTS</span></span>

### <span data-ttu-id="e95fe-125">PSLoadBalancer 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="e95fe-125">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="e95fe-126">筆記</span><span class="sxs-lookup"><span data-stu-id="e95fe-126">NOTES</span></span>

## <span data-ttu-id="e95fe-127">相關連結</span><span class="sxs-lookup"><span data-stu-id="e95fe-127">RELATED LINKS</span></span>

[<span data-ttu-id="e95fe-128">附加 AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="e95fe-128">Add-AzLoadBalancerFrontendIpConfig</span></span>](./Add-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="e95fe-129">AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="e95fe-129">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="e95fe-130">AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="e95fe-130">Get-AzLoadBalancerFrontendIpConfig</span></span>](./Get-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="e95fe-131">新-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="e95fe-131">New-AzLoadBalancerFrontendIpConfig</span></span>](./New-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="e95fe-132">Set-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="e95fe-132">Set-AzLoadBalancerFrontendIpConfig</span></span>](./Set-AzLoadBalancerFrontendIpConfig.md)


