---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-azp2svpngateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzP2sVpnGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzP2sVpnGateway.md
ms.openlocfilehash: d20e2098a797d2e90363f54d79759dc682413803
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101902486"
---
# <span data-ttu-id="6755c-101">Get-AzP2sVpnGateway</span><span class="sxs-lookup"><span data-stu-id="6755c-101">Get-AzP2sVpnGateway</span></span>

## <span data-ttu-id="6755c-102">簡介</span><span class="sxs-lookup"><span data-stu-id="6755c-102">SYNOPSIS</span></span>
<span data-ttu-id="6755c-103">在 VirtualHub 下獲得現有的 P2S VpnGateway。</span><span class="sxs-lookup"><span data-stu-id="6755c-103">Gets an existing P2SVpnGateway under VirtualHub.</span></span>

## <span data-ttu-id="6755c-104">語法</span><span class="sxs-lookup"><span data-stu-id="6755c-104">SYNTAX</span></span>

### <span data-ttu-id="6755c-105">ListBySubscriptionId (預設) </span><span class="sxs-lookup"><span data-stu-id="6755c-105">ListBySubscriptionId (Default)</span></span>
```
Get-AzP2sVpnGateway [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6755c-106">ListByResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6755c-106">ListByResourceGroupName</span></span>
```
Get-AzP2sVpnGateway [-ResourceGroupName <String>] [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="6755c-107">描述</span><span class="sxs-lookup"><span data-stu-id="6755c-107">DESCRIPTION</span></span>
<span data-ttu-id="6755c-108">**Get-AzP2s VpnGateway** Cmdlet 可讓您在 VirtualHub 下取得現有的 P2S VpnGateway。</span><span class="sxs-lookup"><span data-stu-id="6755c-108">The **Get-AzP2sVpnGateway** cmdlet enables you to get an existing P2SVpnGateway under VirtualHub.</span></span>

## <span data-ttu-id="6755c-109">例子</span><span class="sxs-lookup"><span data-stu-id="6755c-109">EXAMPLES</span></span>

### <span data-ttu-id="6755c-110">範例 1</span><span class="sxs-lookup"><span data-stu-id="6755c-110">Example 1</span></span>
```powershell
PS C:\> Get-AzP2sVpnGateway -ResourceGroupName P2SCortexGATesting -Name 683482ade8564515aed4b8448c9757ea-westus-gw

ResourceGroupName              : P2SCortexGATesting
Name                           : 683482ade8564515aed4b8448c9757ea-westus-gw
Id                             : /subscriptions/b1f1deed-af60-4bab-9223-65d340462e24/resourceGroups/P2SCortexGATesting/providers/Microsoft.Network/p2sVpnGateways/683482ade8564515a
                                 ed4b8448c9757ea-westus-gw
Location                       : westus
VpnGatewayScaleUnit            : 1
VirtualHub                     : /subscriptions/b1f1deed-af60-4bab-9223-65d340462e24/resourceGroups/P2SCortexGATesting/providers/Microsoft.Network/virtualHubs/WestUsVirtualHub
VpnServerConfiguration         : /subscriptions/b1f1deed-af60-4bab-9223-65d340462e24/resourceGroups/P2SCortexGATesting/providers/Microsoft.Network/vpnServerConfigurations/WestUsConfig
VpnServerConfigurationLocation :
VpnClientConnectionHealth      : null
Type                           : Microsoft.Network/p2sVpnGateways
ProvisioningState              : Succeeded
P2SConnectionConfigurations    : [
                                   {
                                     "ProvisioningState": "Succeeded",
                                     "VpnClientAddressPool": {
                                       "AddressPrefixes": [
                                         "192.168.2.0/24"
                                       ]
                                     },
                                     "RoutingConfiguration": {
                                       "AssociatedRouteTable": {
                                         "Id": "/subscriptions/b1f1deed-af60-4bab-9223-65d340462e24/resourceGroups/P2SCortexGATesting/providers/Microsoft.Network/virtualHubs/WestUsVirtualHub/hubRouteTables/defaultRouteTable"
                                       }
                                       "PropagatedRouteTables": {
                                         "Labels": [],
                                         "Ids": [
                                           {
                                            "Id": "/subscriptions/b1f1deed-af60-4bab-9223-65d340462e24/resourceGroups/P2SCortexGATesting/providers/Microsoft.Network/virtualHubs/WestUsVirtualHub/hubRouteTables/defaultRouteTable"
                                           }
                                        ]
                                       },
                                       "VnetRoutes": {
                                         "StaticRoutes": []
                                       }
                                     },
                                     "Name": "P2SConnectionConfigDefault",
                                     "Etag": "W/\"4b96e6a2-b4d8-46b3-9210-76d40f359bef\"",
                                     "Id": "/subscriptions/b1f1deed-af60-4bab-9223-65d340462e24/resourceGroups/P2SCortexGATesting/providers/Microsoft.Network/p2sVpnGateways/683482
                                 ade8564515aed4b8448c9757ea-westus-gw/p2sConnectionConfigurations/P2SConnectionConfigDefault"
                                   }
                                 ]
```

<span data-ttu-id="6755c-111">**Get-AzP2s VpnGateway** Cmdlet 可讓您在 VirtualHub 下取得現有的 P2S VpnGateway，用於點到網站連接。</span><span class="sxs-lookup"><span data-stu-id="6755c-111">The **Get-AzP2sVpnGateway** cmdlet enables you to get an existing P2SVpnGateway under VirtualHub that is used for Point to site connectivity.</span></span>

## <span data-ttu-id="6755c-112">參數</span><span class="sxs-lookup"><span data-stu-id="6755c-112">PARAMETERS</span></span>

### <span data-ttu-id="6755c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6755c-113">-DefaultProfile</span></span>
<span data-ttu-id="6755c-114">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="6755c-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6755c-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="6755c-115">-Name</span></span>
<span data-ttu-id="6755c-116">資源名稱。</span><span class="sxs-lookup"><span data-stu-id="6755c-116">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: ListByResourceGroupName
Aliases: ResourceName, P2SVpnGatewayName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6755c-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6755c-117">-ResourceGroupName</span></span>
<span data-ttu-id="6755c-118">資源組名。</span><span class="sxs-lookup"><span data-stu-id="6755c-118">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ListByResourceGroupName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6755c-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6755c-119">CommonParameters</span></span>
<span data-ttu-id="6755c-120">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="6755c-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6755c-121">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="6755c-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6755c-122">輸入</span><span class="sxs-lookup"><span data-stu-id="6755c-122">INPUTS</span></span>

### <span data-ttu-id="6755c-123">沒有</span><span class="sxs-lookup"><span data-stu-id="6755c-123">None</span></span>

## <span data-ttu-id="6755c-124">輸出</span><span class="sxs-lookup"><span data-stu-id="6755c-124">OUTPUTS</span></span>

### <span data-ttu-id="6755c-125">Microsoft.Azure.Commands.Network.models.PSP2S VpnGateway</span><span class="sxs-lookup"><span data-stu-id="6755c-125">Microsoft.Azure.Commands.Network.Models.PSP2SVpnGateway</span></span>

## <span data-ttu-id="6755c-126">筆記</span><span class="sxs-lookup"><span data-stu-id="6755c-126">NOTES</span></span>

## <span data-ttu-id="6755c-127">相關連結</span><span class="sxs-lookup"><span data-stu-id="6755c-127">RELATED LINKS</span></span>
