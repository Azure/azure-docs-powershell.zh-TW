---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-azbgpservicecommunity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzBgpServiceCommunity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzBgpServiceCommunity.md
ms.openlocfilehash: 649fb6734caf2df11a65c43c59d123db425e90bd
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101913845"
---
# <span data-ttu-id="2a329-101">Get-AzBgpServiceCommunity</span><span class="sxs-lookup"><span data-stu-id="2a329-101">Get-AzBgpServiceCommunity</span></span>

## <span data-ttu-id="2a329-102">簡介</span><span class="sxs-lookup"><span data-stu-id="2a329-102">SYNOPSIS</span></span>
<span data-ttu-id="2a329-103">提供所有服務/區域、BGP 社群及相關首碼的清單。</span><span class="sxs-lookup"><span data-stu-id="2a329-103">Provides a list of all services / regions, BGP communities, and associated prefixes.</span></span>

## <span data-ttu-id="2a329-104">語法</span><span class="sxs-lookup"><span data-stu-id="2a329-104">SYNTAX</span></span>

```
Get-AzBgpServiceCommunity [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2a329-105">描述</span><span class="sxs-lookup"><span data-stu-id="2a329-105">DESCRIPTION</span></span>
<span data-ttu-id="2a329-106">此 Cmdlet 會提供所有服務/區域、BGP 社群及相關首碼的清單。</span><span class="sxs-lookup"><span data-stu-id="2a329-106">This cmdlet provides a list of all services / regions, BGP communities, and associated prefixes.</span></span>

## <span data-ttu-id="2a329-107">例子</span><span class="sxs-lookup"><span data-stu-id="2a329-107">EXAMPLES</span></span>

### <span data-ttu-id="2a329-108">範例 1</span><span class="sxs-lookup"><span data-stu-id="2a329-108">Example 1</span></span>
```
Get-AzBgpServiceCommunity

...

Name           : AzureCentralIndia
Id             : /subscriptions//resourceGroups//providers/Microsoft.Network/bgpServiceCommunities/AzureCentralIndia
Type           : Microsoft.Network/bgpServiceCommunities
BgpCommunities : [
                   {
                     "ServiceSupportedRegion": "Global",
                     "CommunityName": "Azure Central India",
                     "CommunityValue": "12076:51017",
                     "CommunityPrefixes": [
                       "13.71.0.0/18",
                       "20.190.146.0/25",
                       "40.79.214.0/24",
                       "40.81.224.0/19",
                       "40.87.224.0/22",
                       "40.112.39.0/25",
                       "40.112.39.128/26",
                       "40.126.18.0/25",
                       "52.136.24.0/24",
                       "52.140.64.0/18",
                       "52.159.64.0/19",
                       "52.172.128.0/17",
                       "52.239.135.64/26",
                       "52.239.202.0/24",
                       "52.245.96.0/22",
                       "52.253.168.0/22",
                       "104.47.210.0/23",
                       "104.211.64.0/20",
                       "104.211.81.0/24",
                       "104.211.82.0/23",
                       "104.211.84.0/22",
                       "104.211.88.0/21",
                       "104.211.96.0/19"
                     ],
                     "IsAuthorizedToUse": true,
                     "ServiceGroup": "Azure"
                   }
                 ]
...
```

<span data-ttu-id="2a329-109">此 Cmdlet 會提供所有服務/區域、BGP 社群及相關首碼的清單。</span><span class="sxs-lookup"><span data-stu-id="2a329-109">This cmdlet provides a list of all services / regions, BGP communities, and associated prefixes.</span></span>

## <span data-ttu-id="2a329-110">參數</span><span class="sxs-lookup"><span data-stu-id="2a329-110">PARAMETERS</span></span>

### <span data-ttu-id="2a329-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2a329-111">-DefaultProfile</span></span>
<span data-ttu-id="2a329-112">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="2a329-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2a329-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2a329-113">CommonParameters</span></span>
<span data-ttu-id="2a329-114">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="2a329-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2a329-115">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2a329-115">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2a329-116">輸入</span><span class="sxs-lookup"><span data-stu-id="2a329-116">INPUTS</span></span>

### <span data-ttu-id="2a329-117">沒有</span><span class="sxs-lookup"><span data-stu-id="2a329-117">None</span></span>

## <span data-ttu-id="2a329-118">輸出</span><span class="sxs-lookup"><span data-stu-id="2a329-118">OUTPUTS</span></span>

### <span data-ttu-id="2a329-119">Microsoft.Azure.Commands.Network.models.PSBgpServiceCommunity</span><span class="sxs-lookup"><span data-stu-id="2a329-119">Microsoft.Azure.Commands.Network.Models.PSBgpServiceCommunity</span></span>

## <span data-ttu-id="2a329-120">筆記</span><span class="sxs-lookup"><span data-stu-id="2a329-120">NOTES</span></span>

## <span data-ttu-id="2a329-121">相關連結</span><span class="sxs-lookup"><span data-stu-id="2a329-121">RELATED LINKS</span></span>

[<span data-ttu-id="2a329-122">Move-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="2a329-122">Move-AzExpressRouteCircuit</span></span>](Move-AzExpressRouteCircuit.md)

[<span data-ttu-id="2a329-123">New-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="2a329-123">New-AzExpressRouteCircuit</span></span>](New-AzExpressRouteCircuit.md)

[<span data-ttu-id="2a329-124">Remove-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="2a329-124">Remove-AzExpressRouteCircuit</span></span>](Remove-AzExpressRouteCircuit.md)

[<span data-ttu-id="2a329-125">Set-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="2a329-125">Set-AzExpressRouteCircuit</span></span>](Set-AzExpressRouteCircuit.md)

[<span data-ttu-id="2a329-126">Get-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="2a329-126">Get-AzRouteFilter</span></span>](Get-AzRouteFilter.md)

[<span data-ttu-id="2a329-127">Get-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="2a329-127">Get-AzRouteFilterRuleConfig</span></span>](Get-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="2a329-128">Remove-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="2a329-128">Remove-AzRouteFilter</span></span>](Remove-AzRouteFilter.md)

[<span data-ttu-id="2a329-129">Remove-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="2a329-129">Remove-AzRouteFilterRuleConfig</span></span>](Remove-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="2a329-130">Set-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="2a329-130">Set-AzRouteFilter</span></span>](Set-AzRouteFilter.md)

[<span data-ttu-id="2a329-131">Set-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="2a329-131">Set-AzRouteFilterRuleConfig</span></span>](Set-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="2a329-132">New-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="2a329-132">New-AzRouteFilter</span></span>](New-AzRouteFilter.md)

[<span data-ttu-id="2a329-133">New-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="2a329-133">New-AzRouteFilterRuleConfig</span></span>](New-AzRouteFilterRuleConfig.md)
