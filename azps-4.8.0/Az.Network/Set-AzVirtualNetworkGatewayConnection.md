---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: D7065B04-1A01-4BB4-A519-1DA9002CDE02
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azvirtualnetworkgatewayconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVirtualNetworkGatewayConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVirtualNetworkGatewayConnection.md
ms.openlocfilehash: c7f7f8603c03300f4f1df1d47a62ed35ca3b93d0
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94135500"
---
# <span data-ttu-id="ba940-101">Set-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="ba940-101">Set-AzVirtualNetworkGatewayConnection</span></span>

## <span data-ttu-id="ba940-102">摘要</span><span class="sxs-lookup"><span data-stu-id="ba940-102">SYNOPSIS</span></span>
<span data-ttu-id="ba940-103">配置虛擬網路閘道連線。</span><span class="sxs-lookup"><span data-stu-id="ba940-103">Configures a virtual network gateway connection.</span></span>

## <span data-ttu-id="ba940-104">句法</span><span class="sxs-lookup"><span data-stu-id="ba940-104">SYNTAX</span></span>

### <span data-ttu-id="ba940-105">預設 (預設) </span><span class="sxs-lookup"><span data-stu-id="ba940-105">Default (Default)</span></span>
```
Set-AzVirtualNetworkGatewayConnection -VirtualNetworkGatewayConnection <PSVirtualNetworkGatewayConnection>
 [-EnableBgp <Boolean>] [-DpdTimeoutInSeconds <Int32>] [-UsePolicyBasedTrafficSelectors <Boolean>] [-UseLocalAzureIpAddress <Boolean>]
 [-IpsecPolicies <PSIpsecPolicy[]>] [-TrafficSelectorPolicy <PSTrafficSelectorPolicy[]>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ba940-106">UpdateResourceWithTags</span><span class="sxs-lookup"><span data-stu-id="ba940-106">UpdateResourceWithTags</span></span>
```
Set-AzVirtualNetworkGatewayConnection -VirtualNetworkGatewayConnection <PSVirtualNetworkGatewayConnection>
 [-EnableBgp <Boolean>] [-DpdTimeoutInSeconds <Int32>] [-UsePolicyBasedTrafficSelectors <Boolean>] [-UseLocalAzureIpAddress <Boolean>]
 [-IpsecPolicies <PSIpsecPolicy[]>] [-TrafficSelectorPolicy <PSTrafficSelectorPolicy[]>] -Tag <Hashtable>
 [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ba940-107">說明</span><span class="sxs-lookup"><span data-stu-id="ba940-107">DESCRIPTION</span></span>
<span data-ttu-id="ba940-108">AzVirtualNetworkGatewayConnection Cmdlet 會 **設定** 虛擬網路閘道連線。</span><span class="sxs-lookup"><span data-stu-id="ba940-108">The **Set-AzVirtualNetworkGatewayConnection** cmdlet configures a virtual network gateway connection.</span></span>

## <span data-ttu-id="ba940-109">示例</span><span class="sxs-lookup"><span data-stu-id="ba940-109">EXAMPLES</span></span>

### <span data-ttu-id="ba940-110">範例1：</span><span class="sxs-lookup"><span data-stu-id="ba940-110">Example 1:</span></span>
```
$conn = Get-AzVirtualNetworkGatewayConnection -Name 1 -ResourceGroupName myRG
Set-AzVirtualNetworkGatewayConnection -VirtualNetworkGatewayConnection $conn

Confirm
Are you sure you want to overwrite resource '1'
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y


Name                    : 1
ResourceGroupName       : myRG
Location                : westus
Id                      : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myRG/providers/Mi
                          crosoft.Network/connections/1
Etag                    : W/"00000000-0000-0000-0000-000000000000"
ResourceGuid            : 00000000-0000-0000-0000-000000000000
ProvisioningState       : Succeeded
Tags                    :
AuthorizationKey        :
VirtualNetworkGateway1  : "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myRG/providers/M
                          icrosoft.Network/virtualNetworkGateways/myGateway"
VirtualNetworkGateway2  : "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/S2SVnetConn/providers/Mic
                          rosoft.Network/virtualNetworkGateways/S2SConnGW"
LocalNetworkGateway2    :
Peer                    :
RoutingWeight           : 0
SharedKey               :
ConnectionStatus        : Connected
EgressBytesTransferred  : 91334484
IngressBytesTransferred : 100386089
TunnelConnectionStatus  : []
```

### <span data-ttu-id="ba940-111">範例2：新增/更新標籤至現有的 VirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="ba940-111">Example 2: Add/Update tags to an existing VirtualNetworkGatewayConnection</span></span>
```
$conn = Get-AzVirtualNetworkGatewayConnection -Name 1 -ResourceGroupName myRG
Set-AzVirtualNetworkGatewayConnection -VirtualNetworkGatewayConnection $conn -Tag @{ testtagKey="SomeTagKey"; testtagValue="SomeKeyValue" }

Confirm
Are you sure you want to overwrite resource '1'
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y


Name                    : 1
ResourceGroupName       : myRG
Location                : westus
Id                      : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myRG/providers/Mi
                          crosoft.Network/connections/1
Etag                    : W/"00000000-0000-0000-0000-000000000000"
ResourceGuid            : 00000000-0000-0000-0000-000000000000
ProvisioningState       : Succeeded
Tags                    :
                          Name          Value
                          ============  ============
                          testtagValue  SomeKeyValue
                          testtagKey    SomeTagKey
AuthorizationKey        :
VirtualNetworkGateway1  : "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myRG/providers/M
                          icrosoft.Network/virtualNetworkGateways/myGateway"
VirtualNetworkGateway2  : "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/S2SVnetConn/providers/Mic
                          rosoft.Network/virtualNetworkGateways/S2SConnGW"
LocalNetworkGateway2    :
Peer                    :
RoutingWeight           : 0
SharedKey               :
ConnectionStatus        : Connected
EgressBytesTransferred  : 91334484
IngressBytesTransferred : 100386089
TunnelConnectionStatus  : []
```

## <span data-ttu-id="ba940-112">參數</span><span class="sxs-lookup"><span data-stu-id="ba940-112">PARAMETERS</span></span>

### <span data-ttu-id="ba940-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ba940-113">-AsJob</span></span>
<span data-ttu-id="ba940-114">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="ba940-114">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ba940-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ba940-115">-DefaultProfile</span></span>
<span data-ttu-id="ba940-116">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="ba940-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ba940-117">-EnableBgp</span><span class="sxs-lookup"><span data-stu-id="ba940-117">-EnableBgp</span></span>
<span data-ttu-id="ba940-118">是否要在 S2S VPN 隧道上使用 BGP 會話</span><span class="sxs-lookup"><span data-stu-id="ba940-118">Whether to use a BGP session over a S2S VPN tunnel</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ba940-119">-DpdTimeoutInSeconds</span><span class="sxs-lookup"><span data-stu-id="ba940-119">-DpdTimeoutInSeconds</span></span>
<span data-ttu-id="ba940-120">連線的死對等檢測超時值（以秒為單位）</span><span class="sxs-lookup"><span data-stu-id="ba940-120">Dead Peer Detection Timeout of the connection in seconds</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ba940-121">-Force</span><span class="sxs-lookup"><span data-stu-id="ba940-121">-Force</span></span>
<span data-ttu-id="ba940-122">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="ba940-122">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ba940-123">-IpsecPolicies</span><span class="sxs-lookup"><span data-stu-id="ba940-123">-IpsecPolicies</span></span>
<span data-ttu-id="ba940-124">IPSec 原則清單。</span><span class="sxs-lookup"><span data-stu-id="ba940-124">A list of IPSec policies.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ba940-125">-Tag</span><span class="sxs-lookup"><span data-stu-id="ba940-125">-Tag</span></span>
<span data-ttu-id="ba940-126">代表資源標記的 hashtable。</span><span class="sxs-lookup"><span data-stu-id="ba940-126">A hashtable which represents resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: UpdateResourceWithTags
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ba940-127">-TrafficSelectorPolicy</span><span class="sxs-lookup"><span data-stu-id="ba940-127">-TrafficSelectorPolicy</span></span>
<span data-ttu-id="ba940-128">流量選取器原則的清單。</span><span class="sxs-lookup"><span data-stu-id="ba940-128">A list of Traffic Selector policies.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSTrafficSelectorPolicy[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ba940-129">-UseLocalAzureIpAddress</span><span class="sxs-lookup"><span data-stu-id="ba940-129">-UseLocalAzureIpAddress</span></span>
<span data-ttu-id="ba940-130">是否針對 S2S 連接使用 PrivateIP</span><span class="sxs-lookup"><span data-stu-id="ba940-130">Whether to use PrivateIP for a S2S connection</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ba940-131">-UsePolicyBasedTrafficSelectors</span><span class="sxs-lookup"><span data-stu-id="ba940-131">-UsePolicyBasedTrafficSelectors</span></span>
<span data-ttu-id="ba940-132">是否要針對 S2S 連線使用原則流量選擇器</span><span class="sxs-lookup"><span data-stu-id="ba940-132">Whether to use policy-based traffic selectors for a S2S connection</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ba940-133">-VirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="ba940-133">-VirtualNetworkGatewayConnection</span></span>
<span data-ttu-id="ba940-134">指定此 Cmdlet 用來修改虛擬網路閘道連線的 PSVirtualNetworkGatewayConnection 物件。</span><span class="sxs-lookup"><span data-stu-id="ba940-134">Specifies the PSVirtualNetworkGatewayConnection object that this cmdlet uses to modify the virtual network gateway connection.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayConnection
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ba940-135">-確認</span><span class="sxs-lookup"><span data-stu-id="ba940-135">-Confirm</span></span>
<span data-ttu-id="ba940-136">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="ba940-136">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ba940-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ba940-137">-WhatIf</span></span>
<span data-ttu-id="ba940-138">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="ba940-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ba940-139">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ba940-139">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ba940-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ba940-140">CommonParameters</span></span>
<span data-ttu-id="ba940-141">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="ba940-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ba940-142">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="ba940-142">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ba940-143">輸入</span><span class="sxs-lookup"><span data-stu-id="ba940-143">INPUTS</span></span>

### <span data-ttu-id="ba940-144">PSVirtualNetworkGatewayConnection 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="ba940-144">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayConnection</span></span>

### <span data-ttu-id="ba940-145">"CoreLib" 1 ["System.object，System.object，版本 = 4.0.0.0，Culture = 中立，PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="ba940-145">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="ba940-146">PSIpsecPolicy [] （[]）</span><span class="sxs-lookup"><span data-stu-id="ba940-146">Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy[]</span></span>

### <span data-ttu-id="ba940-147">PSTrafficSelectorPolicy [] （[]）</span><span class="sxs-lookup"><span data-stu-id="ba940-147">Microsoft.Azure.Commands.Network.Models.PSTrafficSelectorPolicy[]</span></span>

## <span data-ttu-id="ba940-148">輸出</span><span class="sxs-lookup"><span data-stu-id="ba940-148">OUTPUTS</span></span>

### <span data-ttu-id="ba940-149">PSVirtualNetworkGatewayConnection 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="ba940-149">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayConnection</span></span>

## <span data-ttu-id="ba940-150">筆記</span><span class="sxs-lookup"><span data-stu-id="ba940-150">NOTES</span></span>

## <span data-ttu-id="ba940-151">相關連結</span><span class="sxs-lookup"><span data-stu-id="ba940-151">RELATED LINKS</span></span>

[<span data-ttu-id="ba940-152">AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="ba940-152">Get-AzVirtualNetworkGatewayConnection</span></span>](./Get-AzVirtualNetworkGatewayConnection.md)

[<span data-ttu-id="ba940-153">新-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="ba940-153">New-AzVirtualNetworkGatewayConnection</span></span>](./New-AzVirtualNetworkGatewayConnection.md)

[<span data-ttu-id="ba940-154">移除-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="ba940-154">Remove-AzVirtualNetworkGatewayConnection</span></span>](./Remove-AzVirtualNetworkGatewayConnection.md)


