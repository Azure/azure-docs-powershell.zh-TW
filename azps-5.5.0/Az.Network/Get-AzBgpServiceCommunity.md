---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azbgpservicecommunity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzBgpServiceCommunity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzBgpServiceCommunity.md
ms.openlocfilehash: 334c10d1fdeb8dae4379d495975934572fe7e340
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100135011"
---
# <span data-ttu-id="4fce9-101">Get-AzBgpServiceCommunity</span><span class="sxs-lookup"><span data-stu-id="4fce9-101">Get-AzBgpServiceCommunity</span></span>

## <span data-ttu-id="4fce9-102">摘要</span><span class="sxs-lookup"><span data-stu-id="4fce9-102">SYNOPSIS</span></span>
<span data-ttu-id="4fce9-103">提供所有服務/地區、BGP 社區及相關聯的首碼的清單。</span><span class="sxs-lookup"><span data-stu-id="4fce9-103">Provides a list of all services / regions, BGP communities, and associated prefixes.</span></span>

## <span data-ttu-id="4fce9-104">句法</span><span class="sxs-lookup"><span data-stu-id="4fce9-104">SYNTAX</span></span>

```
Get-AzBgpServiceCommunity [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4fce9-105">說明</span><span class="sxs-lookup"><span data-stu-id="4fce9-105">DESCRIPTION</span></span>
<span data-ttu-id="4fce9-106">這個 Cmdlet 提供所有服務/地區、BGP 社區及相關聯的首碼的清單。</span><span class="sxs-lookup"><span data-stu-id="4fce9-106">This cmdlet provides a list of all services / regions, BGP communities, and associated prefixes.</span></span>

## <span data-ttu-id="4fce9-107">示例</span><span class="sxs-lookup"><span data-stu-id="4fce9-107">EXAMPLES</span></span>

### <span data-ttu-id="4fce9-108">範例1</span><span class="sxs-lookup"><span data-stu-id="4fce9-108">Example 1</span></span>
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

<span data-ttu-id="4fce9-109">這個 Cmdlet 提供所有服務/地區、BGP 社區及相關聯的首碼的清單。</span><span class="sxs-lookup"><span data-stu-id="4fce9-109">This cmdlet provides a list of all services / regions, BGP communities, and associated prefixes.</span></span>

## <span data-ttu-id="4fce9-110">參數</span><span class="sxs-lookup"><span data-stu-id="4fce9-110">PARAMETERS</span></span>

### <span data-ttu-id="4fce9-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4fce9-111">-DefaultProfile</span></span>
<span data-ttu-id="4fce9-112">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="4fce9-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4fce9-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4fce9-113">CommonParameters</span></span>
<span data-ttu-id="4fce9-114">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="4fce9-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4fce9-115">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="4fce9-115">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4fce9-116">輸入</span><span class="sxs-lookup"><span data-stu-id="4fce9-116">INPUTS</span></span>

### <span data-ttu-id="4fce9-117">所有</span><span class="sxs-lookup"><span data-stu-id="4fce9-117">None</span></span>

## <span data-ttu-id="4fce9-118">輸出</span><span class="sxs-lookup"><span data-stu-id="4fce9-118">OUTPUTS</span></span>

### <span data-ttu-id="4fce9-119">PSBgpServiceCommunity 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="4fce9-119">Microsoft.Azure.Commands.Network.Models.PSBgpServiceCommunity</span></span>

## <span data-ttu-id="4fce9-120">筆記</span><span class="sxs-lookup"><span data-stu-id="4fce9-120">NOTES</span></span>

## <span data-ttu-id="4fce9-121">相關連結</span><span class="sxs-lookup"><span data-stu-id="4fce9-121">RELATED LINKS</span></span>

[<span data-ttu-id="4fce9-122">移動流覽 AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="4fce9-122">Move-AzExpressRouteCircuit</span></span>](Move-AzExpressRouteCircuit.md)

[<span data-ttu-id="4fce9-123">新-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="4fce9-123">New-AzExpressRouteCircuit</span></span>](New-AzExpressRouteCircuit.md)

[<span data-ttu-id="4fce9-124">移除-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="4fce9-124">Remove-AzExpressRouteCircuit</span></span>](Remove-AzExpressRouteCircuit.md)

[<span data-ttu-id="4fce9-125">Set-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="4fce9-125">Set-AzExpressRouteCircuit</span></span>](Set-AzExpressRouteCircuit.md)

[<span data-ttu-id="4fce9-126">AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="4fce9-126">Get-AzRouteFilter</span></span>](Get-AzRouteFilter.md)

[<span data-ttu-id="4fce9-127">AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="4fce9-127">Get-AzRouteFilterRuleConfig</span></span>](Get-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="4fce9-128">移除-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="4fce9-128">Remove-AzRouteFilter</span></span>](Remove-AzRouteFilter.md)

[<span data-ttu-id="4fce9-129">移除-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="4fce9-129">Remove-AzRouteFilterRuleConfig</span></span>](Remove-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="4fce9-130">Set-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="4fce9-130">Set-AzRouteFilter</span></span>](Set-AzRouteFilter.md)

[<span data-ttu-id="4fce9-131">Set-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="4fce9-131">Set-AzRouteFilterRuleConfig</span></span>](Set-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="4fce9-132">新-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="4fce9-132">New-AzRouteFilter</span></span>](New-AzRouteFilter.md)

[<span data-ttu-id="4fce9-133">新-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="4fce9-133">New-AzRouteFilterRuleConfig</span></span>](New-AzRouteFilterRuleConfig.md)
