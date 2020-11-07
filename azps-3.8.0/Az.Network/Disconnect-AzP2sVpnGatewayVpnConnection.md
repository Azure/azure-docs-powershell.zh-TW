---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/disconnect-azp2svpngatewayvpnconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Disconnect-AzP2sVpnGatewayVpnConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Disconnect-AzP2sVpnGatewayVpnConnection.md
ms.openlocfilehash: ee14842a636ff451e100a75db427934f9f0a1043
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93959530"
---
# <span data-ttu-id="0bc8d-101">Disconnect-AzP2sVpnGatewayVpnConnection</span><span class="sxs-lookup"><span data-stu-id="0bc8d-101">Disconnect-AzP2sVpnGatewayVpnConnection</span></span>

## <span data-ttu-id="0bc8d-102">摘要</span><span class="sxs-lookup"><span data-stu-id="0bc8d-102">SYNOPSIS</span></span>
<span data-ttu-id="0bc8d-103">與指定 p2s vpn 閘道的連線 vpn 用戶端連線中斷連接</span><span class="sxs-lookup"><span data-stu-id="0bc8d-103">Disconnect given connected vpn client connections with a given p2s vpn gateway</span></span>

## <span data-ttu-id="0bc8d-104">句法</span><span class="sxs-lookup"><span data-stu-id="0bc8d-104">SYNTAX</span></span>

### <span data-ttu-id="0bc8d-105">ByP2SVpnGatewayName (預設) </span><span class="sxs-lookup"><span data-stu-id="0bc8d-105">ByP2SVpnGatewayName (Default)</span></span>
```
Disconnect-AzP2sVpnGatewayVpnConnection -Name <String> -ResourceGroupName <String>
 -VpnConnectionId <VpnConnectionId> [<CommonParameters>]
```

### <span data-ttu-id="0bc8d-106">ByP2SVpnGatewayObject</span><span class="sxs-lookup"><span data-stu-id="0bc8d-106">ByP2SVpnGatewayObject</span></span>
```
Disconnect-AzP2sVpnGatewayVpnConnection -InputObject <PSP2SVpnGateway> -VpnConnectionId <VpnConnectionId> [<CommonParameters>]
```

### <span data-ttu-id="0bc8d-107">ByP2SVpnGatewayResourceId</span><span class="sxs-lookup"><span data-stu-id="0bc8d-107">ByP2SVpnGatewayResourceId</span></span>
```
Disconnect-AzP2sVpnGatewayVpnConnection -ResourceId <String> -VpnConnectionId <VpnConnectionId> [<CommonParameters>]
```

## <span data-ttu-id="0bc8d-108">說明</span><span class="sxs-lookup"><span data-stu-id="0bc8d-108">DESCRIPTION</span></span>
<span data-ttu-id="0bc8d-109">**AzP2sVpnGatewayVpnConnection** Cmdlet 可讓您中斷從 P2SVpnGateway 的目前點至 [網站連線] 的連接。</span><span class="sxs-lookup"><span data-stu-id="0bc8d-109">The **Disconnect-AzP2sVpnGatewayVpnConnection** cmdlet enables you to disconnect given current point to site connection from P2SVpnGateway.</span></span>

## <span data-ttu-id="0bc8d-110">示例</span><span class="sxs-lookup"><span data-stu-id="0bc8d-110">EXAMPLES</span></span>

### <span data-ttu-id="0bc8d-111">範例1</span><span class="sxs-lookup"><span data-stu-id="0bc8d-111">Example 1</span></span>
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

## <span data-ttu-id="0bc8d-112">參數</span><span class="sxs-lookup"><span data-stu-id="0bc8d-112">PARAMETERS</span></span>

### <span data-ttu-id="0bc8d-113">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0bc8d-113">-InputObject</span></span>
<span data-ttu-id="0bc8d-114">要修改的 p2s vpn 閘道物件</span><span class="sxs-lookup"><span data-stu-id="0bc8d-114">The p2s vpn gateway object to be modified</span></span>

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

### <span data-ttu-id="0bc8d-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="0bc8d-115">-Name</span></span>
<span data-ttu-id="0bc8d-116">資源名稱。</span><span class="sxs-lookup"><span data-stu-id="0bc8d-116">The resource name.</span></span>

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

### <span data-ttu-id="0bc8d-117">-VpnConnectionId</span><span class="sxs-lookup"><span data-stu-id="0bc8d-117">-VpnConnectionId</span></span>
<span data-ttu-id="0bc8d-118">Vpn 連線 Ida</span><span class="sxs-lookup"><span data-stu-id="0bc8d-118">Vpn Connection Ida</span></span>

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

### <span data-ttu-id="0bc8d-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0bc8d-119">-ResourceGroupName</span></span>
<span data-ttu-id="0bc8d-120">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="0bc8d-120">The resource group name.</span></span>

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

### <span data-ttu-id="0bc8d-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0bc8d-121">-ResourceId</span></span>
<span data-ttu-id="0bc8d-122">P2s 虛擬網路閘道資源識別碼</span><span class="sxs-lookup"><span data-stu-id="0bc8d-122">P2s Virtual network gateway resource Id</span></span>

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

### <span data-ttu-id="0bc8d-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0bc8d-123">CommonParameters</span></span>
<span data-ttu-id="0bc8d-124">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="0bc8d-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0bc8d-125">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="0bc8d-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0bc8d-126">輸入</span><span class="sxs-lookup"><span data-stu-id="0bc8d-126">INPUTS</span></span>

### <span data-ttu-id="0bc8d-127">System.object</span><span class="sxs-lookup"><span data-stu-id="0bc8d-127">System.String</span></span>

## <span data-ttu-id="0bc8d-128">輸出</span><span class="sxs-lookup"><span data-stu-id="0bc8d-128">OUTPUTS</span></span>

### <span data-ttu-id="0bc8d-129">PSP2SVpnGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="0bc8d-129">Microsoft.Azure.Commands.Network.Models.PSP2SVpnGateway</span></span>

## <span data-ttu-id="0bc8d-130">筆記</span><span class="sxs-lookup"><span data-stu-id="0bc8d-130">NOTES</span></span>

## <span data-ttu-id="0bc8d-131">相關連結</span><span class="sxs-lookup"><span data-stu-id="0bc8d-131">RELATED LINKS</span></span>
