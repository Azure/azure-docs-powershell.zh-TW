---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermvpnconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVpnConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVpnConnection.md
ms.openlocfilehash: 7f4ba2cf4a57eedea41eccb8d5846129a80414d1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93448358"
---
# <span data-ttu-id="00161-101">Get-AzureRmVpnConnection</span><span class="sxs-lookup"><span data-stu-id="00161-101">Get-AzureRmVpnConnection</span></span>

## <span data-ttu-id="00161-102">摘要</span><span class="sxs-lookup"><span data-stu-id="00161-102">SYNOPSIS</span></span>
<span data-ttu-id="00161-103">透過名稱取得 vpn 連線，或列出連接至 VpnGateway 的所有 vpn 連線。</span><span class="sxs-lookup"><span data-stu-id="00161-103">Gets a vpn connection by name or lists all vpn connections connected to a VpnGateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="00161-104">句法</span><span class="sxs-lookup"><span data-stu-id="00161-104">SYNTAX</span></span>

### <span data-ttu-id="00161-105">ByVpnGatewayName (預設) </span><span class="sxs-lookup"><span data-stu-id="00161-105">ByVpnGatewayName (Default)</span></span>
```
Get-AzureRmVpnConnection -ResourceGroupName <String> -ParentResourceName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="00161-106">ByVpnGatewayObject</span><span class="sxs-lookup"><span data-stu-id="00161-106">ByVpnGatewayObject</span></span>
```
Get-AzureRmVpnConnection -ParentObject <PSVpnGateway> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="00161-107">ByVpnGatewayResourceId</span><span class="sxs-lookup"><span data-stu-id="00161-107">ByVpnGatewayResourceId</span></span>
```
Get-AzureRmVpnConnection -ParentResourceId <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="00161-108">說明</span><span class="sxs-lookup"><span data-stu-id="00161-108">DESCRIPTION</span></span>
<span data-ttu-id="00161-109">透過名稱取得 vpn 連線，或列出連接至 VpnGateway 的所有 vpn 連線。</span><span class="sxs-lookup"><span data-stu-id="00161-109">Gets a vpn connection by name or lists all vpn connections connected to a VpnGateway.</span></span>

## <span data-ttu-id="00161-110">示例</span><span class="sxs-lookup"><span data-stu-id="00161-110">EXAMPLES</span></span>

### <span data-ttu-id="00161-111">範例1</span><span class="sxs-lookup"><span data-stu-id="00161-111">Example 1</span></span>

```powershell
PS C:\> New-AzureRmResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzureRmVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West US"
PS C:\> $virtualHub = New-AzureRmVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.0.1/24"
PS C:\> New-AzureRmVpnGateway -ResourceGroupName "testRG" -Name "testvpngw" -VirtualHubId $virtualHub.Id -BGPPeeringWeight 10 -VpnGatewayScaleUnit 2
PS C:\> $vpnGateway = Get-AzureRmVpnGateway -ResourceGroupName "testRG" -Name "testvpngw"

PS C:\> $vpnSiteAddressSpaces = New-Object string[] 2
PS C:\> $vpnSiteAddressSpaces[0] = "192.168.2.0/24"
PS C:\> $vpnSiteAddressSpaces[1] = "192.168.3.0/24"

PS C:\> $vpnSite = New-AzureRmVpnSite -ResourceGroupName "testRG" -Name "testVpnSite" -Location "West US" -VirtualWan $virtualWan -IpAddress "1.2.3.4" -AddressSpace $vpnSiteAddressSpaces -DeviceModel "SomeDevice" -DeviceVendor "SomeDeviceVendor" -LinkSpeedInMbps "10"

PS C:\> New-AzureRmVpnConnection -ResourceGroupName $vpnGateway.ResourceGroupName -ParentResourceName $vpnGateway.Name -Name "testConnection" -VpnSite $vpnSite
PS C:\> Get-AzureRmVpnConnection -ResourceGroupName $vpnGateway.ResourceGroupName -ParentResourceName $vpnGateway.Name -Name "testConnection"

RemoteVpnSite             : Microsoft.Azure.Commands.Network.Models.PSResourceId
SharedKey                 :
VpnConnectionProtocolType : IKEv2
ConnectionStatus          :
EgressBytesTransferred    : 0
IngressBytesTransferred   : 0
IpsecPolicies             : {}
ConnectionBandwidth       : 20
EnableBgp                 : False
ProvisioningState         : testConnection
Name                      : ps9709
Etag                      : W/"4580a2e2-2fab-4cff-88eb-92013a76b5a8"
Id                        : /subscriptions/{subscriptionId}/resourceGroups/ps9361/providers/Microsoft.Network/vpnGateways/testvpngw/vpnConnections/testConnection
```

<span data-ttu-id="00161-112">上述將會在 Azure 中的 [testRG] 資源群組中，建立資源群組、虛擬 WAN、虛擬網路、虛擬中樞及 VpnSite。</span><span class="sxs-lookup"><span data-stu-id="00161-112">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub and a VpnSite in West US in "testRG" resource group in Azure.</span></span> <span data-ttu-id="00161-113">此後，就會在具有2個比例單位的虛擬中樞中建立 VPN 閘道。</span><span class="sxs-lookup"><span data-stu-id="00161-113">A VPN gateway will be created thereafter in the Virtual Hub with 2 scale units.</span></span>

<span data-ttu-id="00161-114">建立閘道之後，就會使用 [New-AzureRmVpnConnection] 命令將它連線至 VpnSite。</span><span class="sxs-lookup"><span data-stu-id="00161-114">Once the gateway has been created, it is connected to the VpnSite using the New-AzureRmVpnConnection command.</span></span>

<span data-ttu-id="00161-115">然後它會使用連接名稱取得連線。</span><span class="sxs-lookup"><span data-stu-id="00161-115">Then it gets the connection using the connection name.</span></span>

## <span data-ttu-id="00161-116">參數</span><span class="sxs-lookup"><span data-stu-id="00161-116">PARAMETERS</span></span>

### <span data-ttu-id="00161-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="00161-117">-DefaultProfile</span></span>
<span data-ttu-id="00161-118">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="00161-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="00161-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="00161-119">-Name</span></span>
<span data-ttu-id="00161-120">資源名稱。</span><span class="sxs-lookup"><span data-stu-id="00161-120">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName, VpnConnectionName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="00161-121">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="00161-121">-ParentObject</span></span>
<span data-ttu-id="00161-122">此連接的父 VpnGateway。</span><span class="sxs-lookup"><span data-stu-id="00161-122">The parent VpnGateway for this connection.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVpnGateway
Parameter Sets: ByVpnGatewayObject
Aliases: ParentVpnGateway, VpnGateway

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="00161-123">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="00161-123">-ParentResourceId</span></span>
<span data-ttu-id="00161-124">此連線之父 VpnGateway 的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="00161-124">The resource id of the parent VpnGateway for this connection.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnGatewayResourceId
Aliases: ParentVpnGatewayId, VpnGatewayId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="00161-125">-ParentResourceName</span><span class="sxs-lookup"><span data-stu-id="00161-125">-ParentResourceName</span></span>
<span data-ttu-id="00161-126">父資源名稱。</span><span class="sxs-lookup"><span data-stu-id="00161-126">The parent resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnGatewayName
Aliases: ParentVpnGatewayName, VpnGatewayName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="00161-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="00161-127">-ResourceGroupName</span></span>
<span data-ttu-id="00161-128">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="00161-128">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnGatewayName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="00161-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="00161-129">CommonParameters</span></span>
<span data-ttu-id="00161-130">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="00161-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="00161-131">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="00161-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="00161-132">輸入</span><span class="sxs-lookup"><span data-stu-id="00161-132">INPUTS</span></span>

### <span data-ttu-id="00161-133">System.object</span><span class="sxs-lookup"><span data-stu-id="00161-133">System.String</span></span>

## <span data-ttu-id="00161-134">輸出</span><span class="sxs-lookup"><span data-stu-id="00161-134">OUTPUTS</span></span>

### <span data-ttu-id="00161-135">PSVpnConnection 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="00161-135">Microsoft.Azure.Commands.Network.Models.PSVpnConnection</span></span>

## <span data-ttu-id="00161-136">筆記</span><span class="sxs-lookup"><span data-stu-id="00161-136">NOTES</span></span>

## <span data-ttu-id="00161-137">相關連結</span><span class="sxs-lookup"><span data-stu-id="00161-137">RELATED LINKS</span></span>
