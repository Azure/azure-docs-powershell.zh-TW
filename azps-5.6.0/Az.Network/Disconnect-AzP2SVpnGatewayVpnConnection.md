---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/disconnect-azp2svpngatewayvpnconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Disconnect-AzP2SVpnGatewayVpnConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Disconnect-AzP2SVpnGatewayVpnConnection.md
ms.openlocfilehash: 493927a21b4154065777109341b437d75f934ee3
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101908522"
---
# <span data-ttu-id="33bdf-101">Disconnect-AzP2sVpnGatewayVpnConnection</span><span class="sxs-lookup"><span data-stu-id="33bdf-101">Disconnect-AzP2sVpnGatewayVpnConnection</span></span>

## <span data-ttu-id="33bdf-102">簡介</span><span class="sxs-lookup"><span data-stu-id="33bdf-102">SYNOPSIS</span></span>
<span data-ttu-id="33bdf-103">中斷與給定 p2s vpn 閘道的已連接 vpn 用戶端連接</span><span class="sxs-lookup"><span data-stu-id="33bdf-103">Disconnect given connected vpn client connections with a given p2s vpn gateway</span></span>

## <span data-ttu-id="33bdf-104">語法</span><span class="sxs-lookup"><span data-stu-id="33bdf-104">SYNTAX</span></span>

### <span data-ttu-id="33bdf-105">ByP2S VpnGatewayName (預設) </span><span class="sxs-lookup"><span data-stu-id="33bdf-105">ByP2SVpnGatewayName (Default)</span></span>
```
Disconnect-AzP2sVpnGatewayVpnConnection -Name <String> -ResourceGroupName <String>
 -VpnConnectionId <VpnConnectionId> [<CommonParameters>]
```

### <span data-ttu-id="33bdf-106">ByP2S VpnGatewayObject</span><span class="sxs-lookup"><span data-stu-id="33bdf-106">ByP2SVpnGatewayObject</span></span>
```
Disconnect-AzP2sVpnGatewayVpnConnection -InputObject <PSP2SVpnGateway> -VpnConnectionId <VpnConnectionId> [<CommonParameters>]
```

### <span data-ttu-id="33bdf-107">ByP2S VpnGatewayResourceId</span><span class="sxs-lookup"><span data-stu-id="33bdf-107">ByP2SVpnGatewayResourceId</span></span>
```
Disconnect-AzP2sVpnGatewayVpnConnection -ResourceId <String> -VpnConnectionId <VpnConnectionId> [<CommonParameters>]
```

## <span data-ttu-id="33bdf-108">描述</span><span class="sxs-lookup"><span data-stu-id="33bdf-108">DESCRIPTION</span></span>
<span data-ttu-id="33bdf-109">**Disconnect-AzP2s VpnGateway VpnConnection** Cmdlet 可讓您從 P2S VpnGateway 中斷目前點至網站連結。</span><span class="sxs-lookup"><span data-stu-id="33bdf-109">The **Disconnect-AzP2sVpnGatewayVpnConnection** cmdlet enables you to disconnect given current point to site connection from P2SVpnGateway.</span></span>

## <span data-ttu-id="33bdf-110">例子</span><span class="sxs-lookup"><span data-stu-id="33bdf-110">EXAMPLES</span></span>

### <span data-ttu-id="33bdf-111">範例 1</span><span class="sxs-lookup"><span data-stu-id="33bdf-111">Example 1</span></span>
```powershell
PS C:\> Disconnect-AzP2sVpnGatewayVpnConnection -ResourceName 683482ade8564515aed4b8448c9757ea-westus-gw -ResourceGroupName P2SCortexGATesting -VpnConnectionId @("IKEv2_7e1cfe59-5c7c-4315-a876-b11fbfdfeed4")

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
                                     "Name": "P2SConnectionConfigDefault",
                                     "Etag": "W/\"4b96e6a2-b4d8-46b3-9210-76d40f359bef\"",
                                     "Id": "/subscriptions/b1f1deed-af60-4bab-9223-65d340462e24/resourceGroups/P2SCortexGATesting/providers/Microsoft.Network/p2sVpnGateways/683482
                                 ade8564515aed4b8448c9757ea-westus-gw/p2sConnectionConfigurations/P2SConnectionConfigDefault"
                                   }
                                 ]
```

## <span data-ttu-id="33bdf-112">參數</span><span class="sxs-lookup"><span data-stu-id="33bdf-112">PARAMETERS</span></span>

### <span data-ttu-id="33bdf-113">-InputObject</span><span class="sxs-lookup"><span data-stu-id="33bdf-113">-InputObject</span></span>
<span data-ttu-id="33bdf-114">要修改的 p2s vpn 閘道物件</span><span class="sxs-lookup"><span data-stu-id="33bdf-114">The p2s vpn gateway object to be modified</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSP2SVpnGateway
Parameter Sets: ByP2SVpnGatewayObject
Aliases: P2SVpnGateway

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="33bdf-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="33bdf-115">-Name</span></span>
<span data-ttu-id="33bdf-116">資源名稱。</span><span class="sxs-lookup"><span data-stu-id="33bdf-116">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: ByP2SVpnGatewayName
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="33bdf-117">-VpnConnectionId</span><span class="sxs-lookup"><span data-stu-id="33bdf-117">-VpnConnectionId</span></span>
<span data-ttu-id="33bdf-118">Vpn Connection Ida</span><span class="sxs-lookup"><span data-stu-id="33bdf-118">Vpn Connection Ida</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: VpnConnectionId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="33bdf-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="33bdf-119">-ResourceGroupName</span></span>
<span data-ttu-id="33bdf-120">資源組名。</span><span class="sxs-lookup"><span data-stu-id="33bdf-120">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByP2SVpnGatewayName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="33bdf-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="33bdf-121">-ResourceId</span></span>
<span data-ttu-id="33bdf-122">P2s 虛擬網路閘道資源識別碼</span><span class="sxs-lookup"><span data-stu-id="33bdf-122">P2s Virtual network gateway resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ByP2SVpnGatewayResourceId
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="33bdf-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="33bdf-123">CommonParameters</span></span>
<span data-ttu-id="33bdf-124">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="33bdf-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="33bdf-125">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="33bdf-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="33bdf-126">輸入</span><span class="sxs-lookup"><span data-stu-id="33bdf-126">INPUTS</span></span>

### <span data-ttu-id="33bdf-127">System.String</span><span class="sxs-lookup"><span data-stu-id="33bdf-127">System.String</span></span>

## <span data-ttu-id="33bdf-128">輸出</span><span class="sxs-lookup"><span data-stu-id="33bdf-128">OUTPUTS</span></span>

### <span data-ttu-id="33bdf-129">Microsoft.Azure.Commands.Network.models.PSP2S VpnGateway</span><span class="sxs-lookup"><span data-stu-id="33bdf-129">Microsoft.Azure.Commands.Network.Models.PSP2SVpnGateway</span></span>

## <span data-ttu-id="33bdf-130">筆記</span><span class="sxs-lookup"><span data-stu-id="33bdf-130">NOTES</span></span>

## <span data-ttu-id="33bdf-131">相關連結</span><span class="sxs-lookup"><span data-stu-id="33bdf-131">RELATED LINKS</span></span>
