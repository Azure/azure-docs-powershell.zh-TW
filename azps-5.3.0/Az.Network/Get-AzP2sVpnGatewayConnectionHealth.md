---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azp2svpngatewayconnectionhealth
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzP2sVpnGatewayConnectionHealth.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzP2sVpnGatewayConnectionHealth.md
ms.openlocfilehash: 4b9778275f58025c82922133cb5d6f6142df4fc8
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98436338"
---
# <span data-ttu-id="3f2bb-101">Get-AzP2sVpnGatewayConnectionHealth</span><span class="sxs-lookup"><span data-stu-id="3f2bb-101">Get-AzP2sVpnGatewayConnectionHealth</span></span>

## <span data-ttu-id="3f2bb-102">摘要</span><span class="sxs-lookup"><span data-stu-id="3f2bb-102">SYNOPSIS</span></span>
<span data-ttu-id="3f2bb-103">從 P2SVpnGateway 取得目前的 aggregared 點至網站連線健康情況資訊。</span><span class="sxs-lookup"><span data-stu-id="3f2bb-103">Gets the current aggregared point to site connections health information from P2SVpnGateway.</span></span>

## <span data-ttu-id="3f2bb-104">句法</span><span class="sxs-lookup"><span data-stu-id="3f2bb-104">SYNTAX</span></span>

### <span data-ttu-id="3f2bb-105">ByP2SVpnGatewayName (預設) </span><span class="sxs-lookup"><span data-stu-id="3f2bb-105">ByP2SVpnGatewayName (Default)</span></span>
```
Get-AzP2sVpnGatewayConnectionHealth [-Name <String>] -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3f2bb-106">ByP2SVpnGatewayObject</span><span class="sxs-lookup"><span data-stu-id="3f2bb-106">ByP2SVpnGatewayObject</span></span>
```
Get-AzP2sVpnGatewayConnectionHealth -InputObject <PSP2SVpnGateway> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="3f2bb-107">ByP2SVpnGatewayResourceId</span><span class="sxs-lookup"><span data-stu-id="3f2bb-107">ByP2SVpnGatewayResourceId</span></span>
```
Get-AzP2sVpnGatewayConnectionHealth -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="3f2bb-108">說明</span><span class="sxs-lookup"><span data-stu-id="3f2bb-108">DESCRIPTION</span></span>
<span data-ttu-id="3f2bb-109">**AzP2sVpnGatewayConnectionHealth** Cmdlet 可讓您從 P2SVpnGateway 取得指向網站連線的目前匯總健康情況。</span><span class="sxs-lookup"><span data-stu-id="3f2bb-109">The **Get-AzP2sVpnGatewayConnectionHealth** cmdlet enables you to get the current aggregated health of point to site connections from P2SVpnGateway.</span></span> <span data-ttu-id="3f2bb-110">匯總健康情況顯示已連線至 P2SVpnGateway 的網站用戶端的點數，以及透過 P2SVpnGateway 與已分派的 ip 位址傳送到網站用戶端的總入口和出口位元組數。</span><span class="sxs-lookup"><span data-stu-id="3f2bb-110">Aggregated health shows number of point to site clients connected to P2SVpnGateway, total ingress and egress bytes transferred through P2SVpnGateway and allocated ip addresses for connected point to site clients.</span></span>

## <span data-ttu-id="3f2bb-111">示例</span><span class="sxs-lookup"><span data-stu-id="3f2bb-111">EXAMPLES</span></span>

### <span data-ttu-id="3f2bb-112">範例1</span><span class="sxs-lookup"><span data-stu-id="3f2bb-112">Example 1</span></span>
```powershell
PS C:\> Get-AzP2sVpnGatewayConnectionHealth -ResourceGroupName P2SCortexGATesting -Name 683482ade8564515aed4b8448c9757ea-westus-gw

ResourceGroupName              : P2SCortexGATesting
Name                           : 683482ade8564515aed4b8448c9757ea-westus-gw
Id                             : /subscriptions/b1f1deed-af60-4bab-9223-65d340462e24/resourceGroups/P2SCortexGATesting/providers/Microsoft.Network/p2sVpnGateways/683482ade8564515a
                                 ed4b8448c9757ea-westus-gw
Location                       : westus
VpnGatewayScaleUnit            : 1
VirtualHub                     : /subscriptions/b1f1deed-af60-4bab-9223-65d340462e24/resourceGroups/P2SCortexGATesting/providers/Microsoft.Network/virtualHubs/WestUsVirtualHub
VpnServerConfiguration         : /subscriptions/b1f1deed-af60-4bab-9223-65d340462e24/resourceGroups/P2SCortexGATesting/providers/Microsoft.Network/vpnServerConfigurations/WestUsConfig
VpnServerConfigurationLocation :
VpnClientConnectionHealth      : { 
                  "VpnClientConnectionsCount": 2,
                      "AllocatedIpAddresses": { "192.168.2.1", "192.168.2.2" },
                      "TotalIngressBytesTransferred": 100,
                      "TotalEgressBytesTransferred": 200
                 }
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

<span data-ttu-id="3f2bb-113">**AzP2sVpnGatewayConnectionHealth** Cmdlet 可讓您從 P2SVpnGateway 取得指向網站連線的目前匯總健康情況。</span><span class="sxs-lookup"><span data-stu-id="3f2bb-113">The **Get-AzP2sVpnGatewayConnectionHealth** cmdlet enables you to get the current aggregated health of point to site connections from P2SVpnGateway.</span></span> <span data-ttu-id="3f2bb-114">上述命令：讓輸出健康顯示已連接至 P2SVpnGateway 的網站用戶端數目為2。</span><span class="sxs-lookup"><span data-stu-id="3f2bb-114">Above command let output health shows that number of point to site clients connected to P2SVpnGateway are 2.</span></span> <span data-ttu-id="3f2bb-115">透過 P2SVpnGateway 傳輸的總入口和出口位元組數分別是100和200。</span><span class="sxs-lookup"><span data-stu-id="3f2bb-115">Total ingress and egress bytes transferred through P2SVpnGateway are 100 and 200 respectively.</span></span> <span data-ttu-id="3f2bb-116">已連接點至網站用戶端的已分派 ip 位址是 "192.168.2.1"，"192.168.2.2"。</span><span class="sxs-lookup"><span data-stu-id="3f2bb-116">Allocated ip addresses for connected point to site clients are "192.168.2.1", "192.168.2.2".</span></span>

## <span data-ttu-id="3f2bb-117">參數</span><span class="sxs-lookup"><span data-stu-id="3f2bb-117">PARAMETERS</span></span>

### <span data-ttu-id="3f2bb-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3f2bb-118">-DefaultProfile</span></span>
<span data-ttu-id="3f2bb-119">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="3f2bb-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3f2bb-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3f2bb-120">-InputObject</span></span>
<span data-ttu-id="3f2bb-121">要修改的 p2s vpn 閘道物件</span><span class="sxs-lookup"><span data-stu-id="3f2bb-121">The p2s vpn gateway object to be modified</span></span>

```yaml
Type: PSP2SVpnGateway
Parameter Sets: ByP2SVpnGatewayObject
Aliases: P2SVpnGateway

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3f2bb-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="3f2bb-122">-Name</span></span>
<span data-ttu-id="3f2bb-123">資源名稱。</span><span class="sxs-lookup"><span data-stu-id="3f2bb-123">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: ByP2SVpnGatewayName
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3f2bb-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3f2bb-124">-ResourceGroupName</span></span>
<span data-ttu-id="3f2bb-125">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="3f2bb-125">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByP2SVpnGatewayName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3f2bb-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3f2bb-126">-ResourceId</span></span>
<span data-ttu-id="3f2bb-127">要修改之 P2SVpnGateway 的 Azure 資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="3f2bb-127">The Azure resource ID of the P2SVpnGateway to be modified.</span></span>

```yaml
Type: String
Parameter Sets: ByP2SVpnGatewayResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3f2bb-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3f2bb-128">CommonParameters</span></span>
<span data-ttu-id="3f2bb-129">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="3f2bb-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3f2bb-130">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="3f2bb-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3f2bb-131">輸入</span><span class="sxs-lookup"><span data-stu-id="3f2bb-131">INPUTS</span></span>

### <span data-ttu-id="3f2bb-132">System.object</span><span class="sxs-lookup"><span data-stu-id="3f2bb-132">System.String</span></span>
<span data-ttu-id="3f2bb-133">PSP2SVpnGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="3f2bb-133">Microsoft.Azure.Commands.Network.Models.PSP2SVpnGateway</span></span>

## <span data-ttu-id="3f2bb-134">輸出</span><span class="sxs-lookup"><span data-stu-id="3f2bb-134">OUTPUTS</span></span>

### <span data-ttu-id="3f2bb-135">PSP2SVpnGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="3f2bb-135">Microsoft.Azure.Commands.Network.Models.PSP2SVpnGateway</span></span>

## <span data-ttu-id="3f2bb-136">筆記</span><span class="sxs-lookup"><span data-stu-id="3f2bb-136">NOTES</span></span>

## <span data-ttu-id="3f2bb-137">相關連結</span><span class="sxs-lookup"><span data-stu-id="3f2bb-137">RELATED LINKS</span></span>
