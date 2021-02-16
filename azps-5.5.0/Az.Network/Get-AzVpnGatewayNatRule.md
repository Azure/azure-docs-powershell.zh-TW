---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvpngatewaynatrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVpnGatewayNatRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVpnGatewayNatRule.md
ms.openlocfilehash: 61dbb86c7eaa574abfcb3fad4bd37d6dbb242260
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100133870"
---
# <span data-ttu-id="8b689-101">Get-AzVpnGatewayNatRule</span><span class="sxs-lookup"><span data-stu-id="8b689-101">Get-AzVpnGatewayNatRule</span></span>

## <span data-ttu-id="8b689-102">摘要</span><span class="sxs-lookup"><span data-stu-id="8b689-102">SYNOPSIS</span></span>
<span data-ttu-id="8b689-103">取得與 VpnGateway 相關聯的 NAT 規則。</span><span class="sxs-lookup"><span data-stu-id="8b689-103">Gets a NAT rule associated with VpnGateway.</span></span>

## <span data-ttu-id="8b689-104">句法</span><span class="sxs-lookup"><span data-stu-id="8b689-104">SYNTAX</span></span>

### <span data-ttu-id="8b689-105">ByVpnGatewayName (預設) </span><span class="sxs-lookup"><span data-stu-id="8b689-105">ByVpnGatewayName (Default)</span></span>
```
Get-AzVpnGatewayNatRule -ResourceGroupName <String> -ParentResourceName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8b689-106">ByVpnGatewayObject</span><span class="sxs-lookup"><span data-stu-id="8b689-106">ByVpnGatewayObject</span></span>
```
Get-AzVpnGatewayNatRule -ParentObject <PSVpnGateway> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8b689-107">ByVpnGatewayResourceId</span><span class="sxs-lookup"><span data-stu-id="8b689-107">ByVpnGatewayResourceId</span></span>
```
Get-AzVpnGatewayNatRule -ParentResourceId <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="8b689-108">說明</span><span class="sxs-lookup"><span data-stu-id="8b689-108">DESCRIPTION</span></span>
<span data-ttu-id="8b689-109">取得與 VpnGateway 相關聯的 NAT 規則。</span><span class="sxs-lookup"><span data-stu-id="8b689-109">Gets a NAT rule associated with VpnGateway.</span></span>

## <span data-ttu-id="8b689-110">示例</span><span class="sxs-lookup"><span data-stu-id="8b689-110">EXAMPLES</span></span>

### <span data-ttu-id="8b689-111">範例</span><span class="sxs-lookup"><span data-stu-id="8b689-111">Example</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West US"
PS C:\> $virtualHub = New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.0.1/24"
PS C:\> New-AzVpnGateway -ResourceGroupName "testRG" -Name "testvpngw" -VirtualHubId $virtualHub.Id -BGPPeeringWeight 10 -VpnGatewayScaleUnit 2
PS C:\> $vpnGateway = Get-AzVpnGateway -ResourceGroupName "testRG" -Name "testvpngw"
PS C:\> New-AzVpnGatewayNatRule -ResourceGroupName $vpnGateway.ResourceGroupName -ParentResourceName $vpnGateway.Name -Name "testNatRule" -Type Static -Mode EgressSnat -InternalMapping "10.0.0.1/26" -ExternalMapping "192.168.0.0/26"
PS C:\> Get-AzVpnGatewayNatRule -ResourceGroupName $vpnGateway.ResourceGroupName -ParentResourceName $vpnGateway.Name -Name "testNatRule"

Type                      : Static
Mode                      : EgressSnat
VpnConnectionProtocolType : IKEv2
InternalMappings          : 10.0.0.1/26
ExternalMappings          : 192.168.0.0/26
IpConfigurationId         :
IngressVpnSiteLinkConnections : [Microsoft.Azure.Commands.Network.Models.PSResourceId]
EgressVpnSiteLinkConnections  : [Microsoft.Azure.Commands.Network.Models.PSResourceId]
ProvisioningState         : Provisioned
Name                      : ps9709
Etag                      : W/"4580a2e2-2fab-4cff-88eb-92013a76b5a8"
Id                        : /subscriptions/{subscriptionId}/resourceGroups/testRg/providers/Microsoft.Network/vpnGateways/testvpngw/natRules/testNatRule

```

<span data-ttu-id="8b689-112">上述將會建立資源群組、虛擬 WAN、虛擬網路、虛擬中樞及 VpnGateway & 與 Vpngateway 相關聯的 NAT 規則。</span><span class="sxs-lookup"><span data-stu-id="8b689-112">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub and VpnGateway & a NAT rule associated with Vpngateway.</span></span>
<span data-ttu-id="8b689-113">接著，它會使用 NAT 規則名稱取得 NAT 規則。</span><span class="sxs-lookup"><span data-stu-id="8b689-113">Then it gets the NAT rule using the NAT rule name.</span></span>

## <span data-ttu-id="8b689-114">參數</span><span class="sxs-lookup"><span data-stu-id="8b689-114">PARAMETERS</span></span>

### <span data-ttu-id="8b689-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8b689-115">-DefaultProfile</span></span>
<span data-ttu-id="8b689-116">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="8b689-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8b689-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="8b689-117">-Name</span></span>
<span data-ttu-id="8b689-118">資源名稱。</span><span class="sxs-lookup"><span data-stu-id="8b689-118">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName, VpnGatewayNatRuleName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8b689-119">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="8b689-119">-ParentObject</span></span>
<span data-ttu-id="8b689-120">此 VpnGatewayNatRule 的父 VpnGateway。</span><span class="sxs-lookup"><span data-stu-id="8b689-120">The parent VpnGateway for this VpnGatewayNatRule.</span></span>

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

### <span data-ttu-id="8b689-121">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="8b689-121">-ParentResourceId</span></span>
<span data-ttu-id="8b689-122">此 VpnGatewayNatRule 之父 VpnGateway 的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="8b689-122">The resource id of the parent VpnGateway for this VpnGatewayNatRule.</span></span>

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

### <span data-ttu-id="8b689-123">-ParentResourceName</span><span class="sxs-lookup"><span data-stu-id="8b689-123">-ParentResourceName</span></span>
<span data-ttu-id="8b689-124">父資源名稱。</span><span class="sxs-lookup"><span data-stu-id="8b689-124">The parent resource name.</span></span>

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

### <span data-ttu-id="8b689-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8b689-125">-ResourceGroupName</span></span>
<span data-ttu-id="8b689-126">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="8b689-126">The resource group name.</span></span>

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

### <span data-ttu-id="8b689-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8b689-127">CommonParameters</span></span>
<span data-ttu-id="8b689-128">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="8b689-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8b689-129">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="8b689-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8b689-130">輸入</span><span class="sxs-lookup"><span data-stu-id="8b689-130">INPUTS</span></span>

### <span data-ttu-id="8b689-131">PSVpnGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="8b689-131">Microsoft.Azure.Commands.Network.Models.PSVpnGateway</span></span>

### <span data-ttu-id="8b689-132">System.object</span><span class="sxs-lookup"><span data-stu-id="8b689-132">System.String</span></span>

## <span data-ttu-id="8b689-133">輸出</span><span class="sxs-lookup"><span data-stu-id="8b689-133">OUTPUTS</span></span>

### <span data-ttu-id="8b689-134">PSVpnGatewayNatRule 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="8b689-134">Microsoft.Azure.Commands.Network.Models.PSVpnGatewayNatRule</span></span>

## <span data-ttu-id="8b689-135">筆記</span><span class="sxs-lookup"><span data-stu-id="8b689-135">NOTES</span></span>

## <span data-ttu-id="8b689-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="8b689-136">RELATED LINKS</span></span>
