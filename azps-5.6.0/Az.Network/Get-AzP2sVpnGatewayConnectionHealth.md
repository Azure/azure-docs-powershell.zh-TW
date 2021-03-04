---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-azp2svpngatewayconnectionhealth
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzP2sVpnGatewayConnectionHealth.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzP2sVpnGatewayConnectionHealth.md
ms.openlocfilehash: f3df825c7907921885809fa866bcc894a981f7f0
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101902489"
---
# <span data-ttu-id="3aa81-101">Get-AzP2sVpnGatewayConnectionHealth</span><span class="sxs-lookup"><span data-stu-id="3aa81-101">Get-AzP2sVpnGatewayConnectionHealth</span></span>

## <span data-ttu-id="3aa81-102">簡介</span><span class="sxs-lookup"><span data-stu-id="3aa81-102">SYNOPSIS</span></span>
<span data-ttu-id="3aa81-103">從 P2S VpnGateway 獲得網站連結健康情況資訊的目前重點。</span><span class="sxs-lookup"><span data-stu-id="3aa81-103">Gets the current aggregared point to site connections health information from P2SVpnGateway.</span></span>

## <span data-ttu-id="3aa81-104">語法</span><span class="sxs-lookup"><span data-stu-id="3aa81-104">SYNTAX</span></span>

### <span data-ttu-id="3aa81-105">ByP2S VpnGatewayName (預設) </span><span class="sxs-lookup"><span data-stu-id="3aa81-105">ByP2SVpnGatewayName (Default)</span></span>
```
Get-AzP2sVpnGatewayConnectionHealth [-Name <String>] -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3aa81-106">ByP2S VpnGatewayObject</span><span class="sxs-lookup"><span data-stu-id="3aa81-106">ByP2SVpnGatewayObject</span></span>
```
Get-AzP2sVpnGatewayConnectionHealth -InputObject <PSP2SVpnGateway> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="3aa81-107">ByP2S VpnGatewayResourceId</span><span class="sxs-lookup"><span data-stu-id="3aa81-107">ByP2SVpnGatewayResourceId</span></span>
```
Get-AzP2sVpnGatewayConnectionHealth -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="3aa81-108">描述</span><span class="sxs-lookup"><span data-stu-id="3aa81-108">DESCRIPTION</span></span>
<span data-ttu-id="3aa81-109">**Get-AzP2s VpnGatewayConnectionHealth** Cmdlet 可讓您從 P2S VpnGateway 取得指向網站連結的目前匯總健康情況。</span><span class="sxs-lookup"><span data-stu-id="3aa81-109">The **Get-AzP2sVpnGatewayConnectionHealth** cmdlet enables you to get the current aggregated health of point to site connections from P2SVpnGateway.</span></span> <span data-ttu-id="3aa81-110">匯總健康狀態會顯示連接至 P2S VpnGateway 的網站用戶端之點數目、透過 P2S VpnGateway 傳輸的總出口和出口位元組數，以及已配置至網站用戶端之連接點的 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="3aa81-110">Aggregated health shows number of point to site clients connected to P2SVpnGateway, total ingress and egress bytes transferred through P2SVpnGateway and allocated ip addresses for connected point to site clients.</span></span>

## <span data-ttu-id="3aa81-111">例子</span><span class="sxs-lookup"><span data-stu-id="3aa81-111">EXAMPLES</span></span>

### <span data-ttu-id="3aa81-112">範例 1</span><span class="sxs-lookup"><span data-stu-id="3aa81-112">Example 1</span></span>
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

<span data-ttu-id="3aa81-113">**Get-AzP2s VpnGatewayConnectionHealth** Cmdlet 可讓您從 P2S VpnGateway 取得指向網站連結的目前匯總健康情況。</span><span class="sxs-lookup"><span data-stu-id="3aa81-113">The **Get-AzP2sVpnGatewayConnectionHealth** cmdlet enables you to get the current aggregated health of point to site connections from P2SVpnGateway.</span></span> <span data-ttu-id="3aa81-114">上方命令讓輸出健康情況顯示連接至 P2S VpnGateway 的網站用戶端點數目為 2。</span><span class="sxs-lookup"><span data-stu-id="3aa81-114">Above command let output health shows that number of point to site clients connected to P2SVpnGateway are 2.</span></span> <span data-ttu-id="3aa81-115">透過 P2S VpnGateway 傳輸的總出口和出口位元組分別為 100 和 200。</span><span class="sxs-lookup"><span data-stu-id="3aa81-115">Total ingress and egress bytes transferred through P2SVpnGateway are 100 and 200 respectively.</span></span> <span data-ttu-id="3aa81-116">已配置的網站用戶端連接點 IP 位址為"192.168.2.1"、"192.168.2.2"。</span><span class="sxs-lookup"><span data-stu-id="3aa81-116">Allocated ip addresses for connected point to site clients are "192.168.2.1", "192.168.2.2".</span></span>

## <span data-ttu-id="3aa81-117">參數</span><span class="sxs-lookup"><span data-stu-id="3aa81-117">PARAMETERS</span></span>

### <span data-ttu-id="3aa81-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3aa81-118">-DefaultProfile</span></span>
<span data-ttu-id="3aa81-119">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="3aa81-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3aa81-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3aa81-120">-InputObject</span></span>
<span data-ttu-id="3aa81-121">要修改的 p2s vpn 閘道物件</span><span class="sxs-lookup"><span data-stu-id="3aa81-121">The p2s vpn gateway object to be modified</span></span>

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

### <span data-ttu-id="3aa81-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="3aa81-122">-Name</span></span>
<span data-ttu-id="3aa81-123">資源名稱。</span><span class="sxs-lookup"><span data-stu-id="3aa81-123">The resource name.</span></span>

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

### <span data-ttu-id="3aa81-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3aa81-124">-ResourceGroupName</span></span>
<span data-ttu-id="3aa81-125">資源組名。</span><span class="sxs-lookup"><span data-stu-id="3aa81-125">The resource group name.</span></span>

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

### <span data-ttu-id="3aa81-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3aa81-126">-ResourceId</span></span>
<span data-ttu-id="3aa81-127">要修改之 P2S VpnGateway 的 Azure 資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="3aa81-127">The Azure resource ID of the P2SVpnGateway to be modified.</span></span>

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

### <span data-ttu-id="3aa81-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3aa81-128">CommonParameters</span></span>
<span data-ttu-id="3aa81-129">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="3aa81-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3aa81-130">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="3aa81-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3aa81-131">輸入</span><span class="sxs-lookup"><span data-stu-id="3aa81-131">INPUTS</span></span>

### <span data-ttu-id="3aa81-132">System.String</span><span class="sxs-lookup"><span data-stu-id="3aa81-132">System.String</span></span>
<span data-ttu-id="3aa81-133">Microsoft.Azure.Commands.Network.models.PSP2S VpnGateway</span><span class="sxs-lookup"><span data-stu-id="3aa81-133">Microsoft.Azure.Commands.Network.Models.PSP2SVpnGateway</span></span>

## <span data-ttu-id="3aa81-134">輸出</span><span class="sxs-lookup"><span data-stu-id="3aa81-134">OUTPUTS</span></span>

### <span data-ttu-id="3aa81-135">Microsoft.Azure.Commands.Network.models.PSP2S VpnGateway</span><span class="sxs-lookup"><span data-stu-id="3aa81-135">Microsoft.Azure.Commands.Network.Models.PSP2SVpnGateway</span></span>

## <span data-ttu-id="3aa81-136">筆記</span><span class="sxs-lookup"><span data-stu-id="3aa81-136">NOTES</span></span>

## <span data-ttu-id="3aa81-137">相關連結</span><span class="sxs-lookup"><span data-stu-id="3aa81-137">RELATED LINKS</span></span>
