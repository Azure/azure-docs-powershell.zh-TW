---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: D7065B04-1A01-4BB4-A519-1DA9002CDE02
online version: https://docs.microsoft.com/powershell/module/az.network/set-azvirtualnetworkgatewayconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVirtualNetworkGatewayConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVirtualNetworkGatewayConnection.md
ms.openlocfilehash: bb937dab16e30eba28b247d5010e3fa8fcc37954
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101908789"
---
# <span data-ttu-id="fb68d-101">Set-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="fb68d-101">Set-AzVirtualNetworkGatewayConnection</span></span>

## <span data-ttu-id="fb68d-102">簡介</span><span class="sxs-lookup"><span data-stu-id="fb68d-102">SYNOPSIS</span></span>
<span data-ttu-id="fb68d-103">設定虛擬網路閘道連接。</span><span class="sxs-lookup"><span data-stu-id="fb68d-103">Configures a virtual network gateway connection.</span></span>

## <span data-ttu-id="fb68d-104">語法</span><span class="sxs-lookup"><span data-stu-id="fb68d-104">SYNTAX</span></span>

### <span data-ttu-id="fb68d-105">預設 (預設) </span><span class="sxs-lookup"><span data-stu-id="fb68d-105">Default (Default)</span></span>
```
Set-AzVirtualNetworkGatewayConnection -VirtualNetworkGatewayConnection <PSVirtualNetworkGatewayConnection>
 [-EnableBgp <Boolean>] [-DpdTimeoutInSeconds <Int32>] [-ConnectionMode <String>] [-UsePolicyBasedTrafficSelectors <Boolean>] [-UseLocalAzureIpAddress <Boolean>]
 [-IpsecPolicies <PSIpsecPolicy[]>] [-TrafficSelectorPolicy <PSTrafficSelectorPolicy[]>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fb68d-106">UpdateResourceWithTags</span><span class="sxs-lookup"><span data-stu-id="fb68d-106">UpdateResourceWithTags</span></span>
```
Set-AzVirtualNetworkGatewayConnection -VirtualNetworkGatewayConnection <PSVirtualNetworkGatewayConnection>
 [-EnableBgp <Boolean>] [-DpdTimeoutInSeconds <Int32>] [-ConnectionMode <String>] [-UsePolicyBasedTrafficSelectors <Boolean>] [-UseLocalAzureIpAddress <Boolean>]
 [-IpsecPolicies <PSIpsecPolicy[]>] [-TrafficSelectorPolicy <PSTrafficSelectorPolicy[]>] -Tag <Hashtable>
 [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fb68d-107">描述</span><span class="sxs-lookup"><span data-stu-id="fb68d-107">DESCRIPTION</span></span>
<span data-ttu-id="fb68d-108">**Set-AzVirtualNetworkGatewayConnection** Cmdlet 會設定虛擬網路閘道連接。</span><span class="sxs-lookup"><span data-stu-id="fb68d-108">The **Set-AzVirtualNetworkGatewayConnection** cmdlet configures a virtual network gateway connection.</span></span>

## <span data-ttu-id="fb68d-109">例子</span><span class="sxs-lookup"><span data-stu-id="fb68d-109">EXAMPLES</span></span>

### <span data-ttu-id="fb68d-110">範例 1：</span><span class="sxs-lookup"><span data-stu-id="fb68d-110">Example 1:</span></span>
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

### <span data-ttu-id="fb68d-111">範例 2：新增/更新現有 VirtualNetworkGatewayConnection 的標記</span><span class="sxs-lookup"><span data-stu-id="fb68d-111">Example 2: Add/Update tags to an existing VirtualNetworkGatewayConnection</span></span>
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

## <span data-ttu-id="fb68d-112">參數</span><span class="sxs-lookup"><span data-stu-id="fb68d-112">PARAMETERS</span></span>

### <span data-ttu-id="fb68d-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="fb68d-113">-AsJob</span></span>
<span data-ttu-id="fb68d-114">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="fb68d-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="fb68d-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fb68d-115">-DefaultProfile</span></span>
<span data-ttu-id="fb68d-116">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="fb68d-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fb68d-117">-EnableBgp</span><span class="sxs-lookup"><span data-stu-id="fb68d-117">-EnableBgp</span></span>
<span data-ttu-id="fb68d-118">是否要在 S2S VPN 中使用 BGP 會話</span><span class="sxs-lookup"><span data-stu-id="fb68d-118">Whether to use a BGP session over a S2S VPN tunnel</span></span>

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

### <span data-ttu-id="fb68d-119">-DpdTimeoutIn用秒</span><span class="sxs-lookup"><span data-stu-id="fb68d-119">-DpdTimeoutInSeconds</span></span>
<span data-ttu-id="fb68d-120">在數秒後，連接會暫停對等偵測</span><span class="sxs-lookup"><span data-stu-id="fb68d-120">Dead Peer Detection Timeout of the connection in seconds</span></span>

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

### <span data-ttu-id="fb68d-121">-ConnectionMode</span><span class="sxs-lookup"><span data-stu-id="fb68d-121">-ConnectionMode</span></span>
<span data-ttu-id="fb68d-122">虛擬網路閘道連接模式</span><span class="sxs-lookup"><span data-stu-id="fb68d-122">Virtual Network Gateway Connection Mode</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Required: False
Position: Named
Default value: Default
Accept wildcard characters: False
```

### <span data-ttu-id="fb68d-123">-強制</span><span class="sxs-lookup"><span data-stu-id="fb68d-123">-Force</span></span>
<span data-ttu-id="fb68d-124">強制執行命令，但不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="fb68d-124">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="fb68d-125">-IpsecPolicies</span><span class="sxs-lookup"><span data-stu-id="fb68d-125">-IpsecPolicies</span></span>
<span data-ttu-id="fb68d-126">IPSec 政策清單。</span><span class="sxs-lookup"><span data-stu-id="fb68d-126">A list of IPSec policies.</span></span>

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

### <span data-ttu-id="fb68d-127">-標記</span><span class="sxs-lookup"><span data-stu-id="fb68d-127">-Tag</span></span>
<span data-ttu-id="fb68d-128">代表資源標記的雜湊表。</span><span class="sxs-lookup"><span data-stu-id="fb68d-128">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="fb68d-129">-TrafficSelectorPolicy</span><span class="sxs-lookup"><span data-stu-id="fb68d-129">-TrafficSelectorPolicy</span></span>
<span data-ttu-id="fb68d-130">流量選取器規則清單。</span><span class="sxs-lookup"><span data-stu-id="fb68d-130">A list of Traffic Selector policies.</span></span>

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

### <span data-ttu-id="fb68d-131">-UseLocalAzureIpAddress</span><span class="sxs-lookup"><span data-stu-id="fb68d-131">-UseLocalAzureIpAddress</span></span>
<span data-ttu-id="fb68d-132">是否要將 PrivateIP 用於 S2S 連接</span><span class="sxs-lookup"><span data-stu-id="fb68d-132">Whether to use PrivateIP for a S2S connection</span></span>

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

### <span data-ttu-id="fb68d-133">-UsePolicyBasedTrafficSelectors</span><span class="sxs-lookup"><span data-stu-id="fb68d-133">-UsePolicyBasedTrafficSelectors</span></span>
<span data-ttu-id="fb68d-134">是否要針對 S2S 連接使用以策略為基礎的流量選取器</span><span class="sxs-lookup"><span data-stu-id="fb68d-134">Whether to use policy-based traffic selectors for a S2S connection</span></span>

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

### <span data-ttu-id="fb68d-135">-VirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="fb68d-135">-VirtualNetworkGatewayConnection</span></span>
<span data-ttu-id="fb68d-136">指定此 Cmdlet 用來修改虛擬網路閘道連接的 PSVirtualNetworkGatewayConnection 物件。</span><span class="sxs-lookup"><span data-stu-id="fb68d-136">Specifies the PSVirtualNetworkGatewayConnection object that this cmdlet uses to modify the virtual network gateway connection.</span></span>

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

### <span data-ttu-id="fb68d-137">-確認</span><span class="sxs-lookup"><span data-stu-id="fb68d-137">-Confirm</span></span>
<span data-ttu-id="fb68d-138">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="fb68d-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fb68d-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fb68d-139">-WhatIf</span></span>
<span data-ttu-id="fb68d-140">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="fb68d-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fb68d-141">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="fb68d-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fb68d-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fb68d-142">CommonParameters</span></span>
<span data-ttu-id="fb68d-143">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="fb68d-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fb68d-144">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="fb68d-144">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fb68d-145">輸入</span><span class="sxs-lookup"><span data-stu-id="fb68d-145">INPUTS</span></span>

### <span data-ttu-id="fb68d-146">Microsoft.Azure.Commands.Network.models.PSVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="fb68d-146">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayConnection</span></span>

### <span data-ttu-id="fb68d-147">System.Nullable'1[[System.Boolean， System.Private.CoreLib， Version=4.0.0.0， Culture=neutral， PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="fb68d-147">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="fb68d-148">Microsoft.Azure.Commands.Network.models.PSIpsecPolicy[]</span><span class="sxs-lookup"><span data-stu-id="fb68d-148">Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy[]</span></span>

### <span data-ttu-id="fb68d-149">Microsoft.Azure.Commands.Network.models.PSTrafficSelectorPolicy[]</span><span class="sxs-lookup"><span data-stu-id="fb68d-149">Microsoft.Azure.Commands.Network.Models.PSTrafficSelectorPolicy[]</span></span>

## <span data-ttu-id="fb68d-150">輸出</span><span class="sxs-lookup"><span data-stu-id="fb68d-150">OUTPUTS</span></span>

### <span data-ttu-id="fb68d-151">Microsoft.Azure.Commands.Network.models.PSVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="fb68d-151">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayConnection</span></span>

## <span data-ttu-id="fb68d-152">筆記</span><span class="sxs-lookup"><span data-stu-id="fb68d-152">NOTES</span></span>

## <span data-ttu-id="fb68d-153">相關連結</span><span class="sxs-lookup"><span data-stu-id="fb68d-153">RELATED LINKS</span></span>

[<span data-ttu-id="fb68d-154">Get-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="fb68d-154">Get-AzVirtualNetworkGatewayConnection</span></span>](./Get-AzVirtualNetworkGatewayConnection.md)

[<span data-ttu-id="fb68d-155">New-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="fb68d-155">New-AzVirtualNetworkGatewayConnection</span></span>](./New-AzVirtualNetworkGatewayConnection.md)

[<span data-ttu-id="fb68d-156">Remove-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="fb68d-156">Remove-AzVirtualNetworkGatewayConnection</span></span>](./Remove-AzVirtualNetworkGatewayConnection.md)


