---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: C9954E3D-8645-473E-A6D4-86278C2F6BC1
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azexpressroutecircuit
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCircuit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCircuit.md
ms.openlocfilehash: 7997949db725d50dd656479852b10d12094b8da7
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98436339"
---
# <span data-ttu-id="b8283-101">Get-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="b8283-101">Get-AzExpressRouteCircuit</span></span>

## <span data-ttu-id="b8283-102">摘要</span><span class="sxs-lookup"><span data-stu-id="b8283-102">SYNOPSIS</span></span>
<span data-ttu-id="b8283-103">從 Azure 取得 Azure ExpressRoute 回路。</span><span class="sxs-lookup"><span data-stu-id="b8283-103">Gets an Azure ExpressRoute circuit from Azure.</span></span>

## <span data-ttu-id="b8283-104">句法</span><span class="sxs-lookup"><span data-stu-id="b8283-104">SYNTAX</span></span>

```
Get-AzExpressRouteCircuit [-Name <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b8283-105">說明</span><span class="sxs-lookup"><span data-stu-id="b8283-105">DESCRIPTION</span></span>
<span data-ttu-id="b8283-106">**AzExpressRouteCircuit** Cmdlet 是用來從您的訂閱中取得 ExpressRoute 回路物件。</span><span class="sxs-lookup"><span data-stu-id="b8283-106">The **Get-AzExpressRouteCircuit** cmdlet is used to retrieve an ExpressRoute circuit object from your subscription.</span></span> <span data-ttu-id="b8283-107">傳回的電路物件可以用來做為其他 Cmdlet 的輸入，以在 ExpressRoute 回路上運作。</span><span class="sxs-lookup"><span data-stu-id="b8283-107">The circuit object returned can be used as input to other cmdlets that operate on ExpressRoute circuits.</span></span>

## <span data-ttu-id="b8283-108">示例</span><span class="sxs-lookup"><span data-stu-id="b8283-108">EXAMPLES</span></span>

### <span data-ttu-id="b8283-109">範例1：取得 ExpressRoute 電路</span><span class="sxs-lookup"><span data-stu-id="b8283-109">Example 1: Get the ExpressRoute circuit</span></span>
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

<span data-ttu-id="b8283-110">取得名稱為 "testrg" 的特定 ExpressRoute 回路，並 ResourceGroupName "test"</span><span class="sxs-lookup"><span data-stu-id="b8283-110">Get a specific ExpressRoute circuit with Name "testrg" and ResourceGroupName "test"</span></span>

### <span data-ttu-id="b8283-111">範例2：使用篩選來列出 ExpressRoute 回路</span><span class="sxs-lookup"><span data-stu-id="b8283-111">Example 2: List the ExpressRoute circuits using filtering</span></span>
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

<span data-ttu-id="b8283-112">取得名稱以「test」開頭的所有 ExpressRoute 回路。</span><span class="sxs-lookup"><span data-stu-id="b8283-112">Get all ExpressRoute circuits whose name starts with "test".</span></span>

## <span data-ttu-id="b8283-113">參數</span><span class="sxs-lookup"><span data-stu-id="b8283-113">PARAMETERS</span></span>

### <span data-ttu-id="b8283-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b8283-114">-DefaultProfile</span></span>
<span data-ttu-id="b8283-115">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="b8283-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b8283-116">-名稱</span><span class="sxs-lookup"><span data-stu-id="b8283-116">-Name</span></span>
<span data-ttu-id="b8283-117">ExpressRoute 回路的名稱。</span><span class="sxs-lookup"><span data-stu-id="b8283-117">The name of the ExpressRoute circuit.</span></span>

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

### <span data-ttu-id="b8283-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b8283-118">-ResourceGroupName</span></span>
<span data-ttu-id="b8283-119">包含 ExpressRoute 回路之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="b8283-119">The name of the resource group that contains the ExpressRoute circuit.</span></span>

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

### <span data-ttu-id="b8283-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b8283-120">CommonParameters</span></span>
<span data-ttu-id="b8283-121">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="b8283-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b8283-122">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="b8283-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b8283-123">輸入</span><span class="sxs-lookup"><span data-stu-id="b8283-123">INPUTS</span></span>

### <span data-ttu-id="b8283-124">System.object</span><span class="sxs-lookup"><span data-stu-id="b8283-124">System.String</span></span>

## <span data-ttu-id="b8283-125">輸出</span><span class="sxs-lookup"><span data-stu-id="b8283-125">OUTPUTS</span></span>

### <span data-ttu-id="b8283-126">PSExpressRouteCircuit 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="b8283-126">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="b8283-127">筆記</span><span class="sxs-lookup"><span data-stu-id="b8283-127">NOTES</span></span>

## <span data-ttu-id="b8283-128">相關連結</span><span class="sxs-lookup"><span data-stu-id="b8283-128">RELATED LINKS</span></span>

[<span data-ttu-id="b8283-129">移動流覽 AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="b8283-129">Move-AzExpressRouteCircuit</span></span>](Move-AzExpressRouteCircuit.md)

[<span data-ttu-id="b8283-130">新-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="b8283-130">New-AzExpressRouteCircuit</span></span>](New-AzExpressRouteCircuit.md)

[<span data-ttu-id="b8283-131">移除-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="b8283-131">Remove-AzExpressRouteCircuit</span></span>](Remove-AzExpressRouteCircuit.md)

[<span data-ttu-id="b8283-132">Set-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="b8283-132">Set-AzExpressRouteCircuit</span></span>](Set-AzExpressRouteCircuit.md)
