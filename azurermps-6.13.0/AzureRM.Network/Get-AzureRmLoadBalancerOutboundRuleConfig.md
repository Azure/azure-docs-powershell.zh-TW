---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermloadbalanceroutboundruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmLoadBalancerOutboundRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmLoadBalancerOutboundRuleConfig.md
ms.openlocfilehash: 1bcaab526ac2fbb82d696db7197bbc8d69c0078f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93626546"
---
# <span data-ttu-id="82a31-101">Get-AzureRmLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="82a31-101">Get-AzureRmLoadBalancerOutboundRuleConfig</span></span>

## <span data-ttu-id="82a31-102">摘要</span><span class="sxs-lookup"><span data-stu-id="82a31-102">SYNOPSIS</span></span>
<span data-ttu-id="82a31-103">在負載平衡器中取得輸出規則配置。</span><span class="sxs-lookup"><span data-stu-id="82a31-103">Gets an outbound rule configuration in a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="82a31-104">句法</span><span class="sxs-lookup"><span data-stu-id="82a31-104">SYNTAX</span></span>

```
Get-AzureRmLoadBalancerOutboundRuleConfig -LoadBalancer <PSLoadBalancer> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="82a31-105">說明</span><span class="sxs-lookup"><span data-stu-id="82a31-105">DESCRIPTION</span></span>
<span data-ttu-id="82a31-106">**AzureRmLoadBalancerOutboundRuleConfig** Cmdlet 會在負載平衡器中取得輸出規則設定或輸出規則配置清單。</span><span class="sxs-lookup"><span data-stu-id="82a31-106">The **Get-AzureRmLoadBalancerOutboundRuleConfig** cmdlet gets an outbound rule configuration or a list of outbound rule configurations in a load balancer.</span></span>

## <span data-ttu-id="82a31-107">示例</span><span class="sxs-lookup"><span data-stu-id="82a31-107">EXAMPLES</span></span>

### <span data-ttu-id="82a31-108">範例1：在負載平衡器中取得輸出規則配置</span><span class="sxs-lookup"><span data-stu-id="82a31-108">Example 1: Get an outbound rule configuration in a load balancer</span></span>
```powershell
PS C:\>$slb = Get-AzureRmLoadBalancer -ResourceGroupName "MyResourceGroup" -Name "MyLoadBalancer"
PS C:\>Get-AzureRmLoadBalancerOutboundRuleConfig -LoadBalancer $slb -Name "MyRule"
```

<span data-ttu-id="82a31-109">第一個命令會取得名為 MyLoadBalancer 的負載平衡器，然後將它儲存在 $slb 的變數中。</span><span class="sxs-lookup"><span data-stu-id="82a31-109">The first command gets the load balancer named MyLoadBalancer, and then stores it in the variable $slb.</span></span>
<span data-ttu-id="82a31-110">第二個命令會取得與該負載平衡器相關聯之名為 MyRule 的輸出規則配置。</span><span class="sxs-lookup"><span data-stu-id="82a31-110">The second command gets the outbound rule configuration named MyRule associated with that load balancer.</span></span>

## <span data-ttu-id="82a31-111">參數</span><span class="sxs-lookup"><span data-stu-id="82a31-111">PARAMETERS</span></span>

### <span data-ttu-id="82a31-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="82a31-112">-DefaultProfile</span></span>
<span data-ttu-id="82a31-113">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="82a31-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="82a31-114">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="82a31-114">-LoadBalancer</span></span>
<span data-ttu-id="82a31-115">負載平衡器資源的參照。</span><span class="sxs-lookup"><span data-stu-id="82a31-115">The reference of the load balancer resource.</span></span>

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

### <span data-ttu-id="82a31-116">-名稱</span><span class="sxs-lookup"><span data-stu-id="82a31-116">-Name</span></span>
<span data-ttu-id="82a31-117">輸出規則的名稱。</span><span class="sxs-lookup"><span data-stu-id="82a31-117">Name of the outbound rule.</span></span>

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

### <span data-ttu-id="82a31-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="82a31-118">CommonParameters</span></span>
<span data-ttu-id="82a31-119">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="82a31-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="82a31-120">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="82a31-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="82a31-121">輸入</span><span class="sxs-lookup"><span data-stu-id="82a31-121">INPUTS</span></span>

### <span data-ttu-id="82a31-122">PSLoadBalancer 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="82a31-122">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="82a31-123">輸出</span><span class="sxs-lookup"><span data-stu-id="82a31-123">OUTPUTS</span></span>

### <span data-ttu-id="82a31-124">PSOutboundRule 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="82a31-124">Microsoft.Azure.Commands.Network.Models.PSOutboundRule</span></span>

## <span data-ttu-id="82a31-125">筆記</span><span class="sxs-lookup"><span data-stu-id="82a31-125">NOTES</span></span>

## <span data-ttu-id="82a31-126">相關連結</span><span class="sxs-lookup"><span data-stu-id="82a31-126">RELATED LINKS</span></span>
