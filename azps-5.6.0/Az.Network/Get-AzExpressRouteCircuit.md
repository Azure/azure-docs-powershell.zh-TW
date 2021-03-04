---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: C9954E3D-8645-473E-A6D4-86278C2F6BC1
online version: https://docs.microsoft.com/powershell/module/az.network/get-azexpressroutecircuit
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCircuit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCircuit.md
ms.openlocfilehash: 8961948970843873f337fd1625aabfdf878ba15d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101905898"
---
# <span data-ttu-id="f7096-101">Get-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="f7096-101">Get-AzExpressRouteCircuit</span></span>

## <span data-ttu-id="f7096-102">簡介</span><span class="sxs-lookup"><span data-stu-id="f7096-102">SYNOPSIS</span></span>
<span data-ttu-id="f7096-103">從 Azure 獲得 Azure ExpressRoute 回路。</span><span class="sxs-lookup"><span data-stu-id="f7096-103">Gets an Azure ExpressRoute circuit from Azure.</span></span>

## <span data-ttu-id="f7096-104">語法</span><span class="sxs-lookup"><span data-stu-id="f7096-104">SYNTAX</span></span>

```
Get-AzExpressRouteCircuit [-Name <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f7096-105">描述</span><span class="sxs-lookup"><span data-stu-id="f7096-105">DESCRIPTION</span></span>
<span data-ttu-id="f7096-106">**Get-AzExpressRouteCircuit** Cmdlet 可用來從訂閱中取回 ExpressRoute 回路物件。</span><span class="sxs-lookup"><span data-stu-id="f7096-106">The **Get-AzExpressRouteCircuit** cmdlet is used to retrieve an ExpressRoute circuit object from your subscription.</span></span> <span data-ttu-id="f7096-107">所返回的回路物件可以用來做為在 ExpressRoute 回路上運作之其他 Cmdlet 的輸入。</span><span class="sxs-lookup"><span data-stu-id="f7096-107">The circuit object returned can be used as input to other cmdlets that operate on ExpressRoute circuits.</span></span>

## <span data-ttu-id="f7096-108">例子</span><span class="sxs-lookup"><span data-stu-id="f7096-108">EXAMPLES</span></span>

### <span data-ttu-id="f7096-109">範例 1：取得 ExpressRoute 回路</span><span class="sxs-lookup"><span data-stu-id="f7096-109">Example 1: Get the ExpressRoute circuit</span></span>
```
Get-AzExpressRouteCircuit -ResourceGroupName testrg -Name test

Name                             : test
ResourceGroupName                : testrg
Location                         : southcentralus
Id                               : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/testrg/pro
                                   viders/Microsoft.Network/expressRouteCircuits/test
Etag                             : W/"00000000-0000-0000-0000-000000000000"
ProvisioningState                : Succeeded
Sku                              : {
                                     "Name": "Standard_UnlimitedData",
                                     "Tier": "Standard",
                                     "Family": "UnlimitedData"
                                   }
CircuitProvisioningState         : Enabled
ServiceProviderProvisioningState : NotProvisioned
ServiceProviderNotes             :
ServiceProviderProperties        : {
                                     "ServiceProviderName": "AT&T",
                                     "PeeringLocation": "Silicon Valley",
                                     "BandwidthInMbps": 50
                                   }
ExpressRoutePort                 : null
BandwidthInGbps                  :
Stag                             :
ServiceKey                       : 00000000-0000-0000-0000-000000000000
Peerings                         : []
Authorizations                   : []
AllowClassicOperations           : False
GatewayManagerEtag               :
```

<span data-ttu-id="f7096-110">取得具有 Name "testrg" 和 ResourceGroupName "test" 的特定 ExpressRoute 回路</span><span class="sxs-lookup"><span data-stu-id="f7096-110">Get a specific ExpressRoute circuit with Name "testrg" and ResourceGroupName "test"</span></span>

### <span data-ttu-id="f7096-111">範例 2：使用篩選列出 ExpressRoute 回路</span><span class="sxs-lookup"><span data-stu-id="f7096-111">Example 2: List the ExpressRoute circuits using filtering</span></span>
```
Get-AzExpressRouteCircuit -Name test*

Name                             : test1
ResourceGroupName                : testrg
Location                         : southcentralus
Id                               : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/testrg/pro
                                   viders/Microsoft.Network/expressRouteCircuits/test1
Etag                             : W/"00000000-0000-0000-0000-000000000000"
ProvisioningState                : Succeeded
Sku                              : {
                                     "Name": "Standard_UnlimitedData",
                                     "Tier": "Standard",
                                     "Family": "UnlimitedData"
                                   }
CircuitProvisioningState         : Enabled
ServiceProviderProvisioningState : NotProvisioned
ServiceProviderNotes             :
ServiceProviderProperties        : {
                                     "ServiceProviderName": "AT&T",
                                     "PeeringLocation": "Silicon Valley",
                                     "BandwidthInMbps": 50
                                   }
ExpressRoutePort                 : null
BandwidthInGbps                  :
Stag                             :
ServiceKey                       : 00000000-0000-0000-0000-000000000000
Peerings                         : []
Authorizations                   : []
AllowClassicOperations           : False
GatewayManagerEtag               :

Name                             : test2
ResourceGroupName                : testrg
Location                         : southcentralus
Id                               : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/testrg/pro
                                   viders/Microsoft.Network/expressRouteCircuits/test2
Etag                             : W/"00000000-0000-0000-0000-000000000000"
ProvisioningState                : Succeeded
Sku                              : {
                                     "Name": "Standard_UnlimitedData",
                                     "Tier": "Standard",
                                     "Family": "UnlimitedData"
                                   }
CircuitProvisioningState         : Enabled
ServiceProviderProvisioningState : NotProvisioned
ServiceProviderNotes             :
ServiceProviderProperties        : {
                                     "ServiceProviderName": "AT&T",
                                     "PeeringLocation": "Silicon Valley",
                                     "BandwidthInMbps": 50
                                   }
ExpressRoutePort                 : null
BandwidthInGbps                  :
Stag                             :
ServiceKey                       : 00000000-0000-0000-0000-000000000000
Peerings                         : []
Authorizations                   : []
AllowClassicOperations           : False
GatewayManagerEtag               :
```

<span data-ttu-id="f7096-112">取得名稱以「測試」開頭的所有 ExpressRoute 回路。</span><span class="sxs-lookup"><span data-stu-id="f7096-112">Get all ExpressRoute circuits whose name starts with "test".</span></span>

## <span data-ttu-id="f7096-113">參數</span><span class="sxs-lookup"><span data-stu-id="f7096-113">PARAMETERS</span></span>

### <span data-ttu-id="f7096-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f7096-114">-DefaultProfile</span></span>
<span data-ttu-id="f7096-115">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="f7096-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f7096-116">-名稱</span><span class="sxs-lookup"><span data-stu-id="f7096-116">-Name</span></span>
<span data-ttu-id="f7096-117">ExpressRoute 回路的名稱。</span><span class="sxs-lookup"><span data-stu-id="f7096-117">The name of the ExpressRoute circuit.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="f7096-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f7096-118">-ResourceGroupName</span></span>
<span data-ttu-id="f7096-119">包含 ExpressRoute 回路的資源組名。</span><span class="sxs-lookup"><span data-stu-id="f7096-119">The name of the resource group that contains the ExpressRoute circuit.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="f7096-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f7096-120">CommonParameters</span></span>
<span data-ttu-id="f7096-121">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="f7096-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f7096-122">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f7096-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f7096-123">輸入</span><span class="sxs-lookup"><span data-stu-id="f7096-123">INPUTS</span></span>

### <span data-ttu-id="f7096-124">System.String</span><span class="sxs-lookup"><span data-stu-id="f7096-124">System.String</span></span>

## <span data-ttu-id="f7096-125">輸出</span><span class="sxs-lookup"><span data-stu-id="f7096-125">OUTPUTS</span></span>

### <span data-ttu-id="f7096-126">Microsoft.Azure.Commands.Network.models.PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="f7096-126">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="f7096-127">筆記</span><span class="sxs-lookup"><span data-stu-id="f7096-127">NOTES</span></span>

## <span data-ttu-id="f7096-128">相關連結</span><span class="sxs-lookup"><span data-stu-id="f7096-128">RELATED LINKS</span></span>

[<span data-ttu-id="f7096-129">Move-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="f7096-129">Move-AzExpressRouteCircuit</span></span>](Move-AzExpressRouteCircuit.md)

[<span data-ttu-id="f7096-130">New-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="f7096-130">New-AzExpressRouteCircuit</span></span>](New-AzExpressRouteCircuit.md)

[<span data-ttu-id="f7096-131">Remove-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="f7096-131">Remove-AzExpressRouteCircuit</span></span>](Remove-AzExpressRouteCircuit.md)

[<span data-ttu-id="f7096-132">Set-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="f7096-132">Set-AzExpressRouteCircuit</span></span>](Set-AzExpressRouteCircuit.md)
