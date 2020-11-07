---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azp2svpngateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzP2sVpnGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzP2sVpnGateway.md
ms.openlocfilehash: 6d16703b7f0492bb2c37291e135cb1b9c836a572
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93957716"
---
# <span data-ttu-id="20a61-101">New-AzP2sVpnGateway</span><span class="sxs-lookup"><span data-stu-id="20a61-101">New-AzP2sVpnGateway</span></span>

## <span data-ttu-id="20a61-102">摘要</span><span class="sxs-lookup"><span data-stu-id="20a61-102">SYNOPSIS</span></span>
<span data-ttu-id="20a61-103">在 [VirtualHub] 下建立新的 P2SVpnGateway，以指向 [網站連線]。</span><span class="sxs-lookup"><span data-stu-id="20a61-103">Create a new P2SVpnGateway under VirtualHub for point to site connectivity.</span></span>

## <span data-ttu-id="20a61-104">句法</span><span class="sxs-lookup"><span data-stu-id="20a61-104">SYNTAX</span></span>

### <span data-ttu-id="20a61-105">ByVirtualHubNameByVpnServerConfigurationObject (預設) </span><span class="sxs-lookup"><span data-stu-id="20a61-105">ByVirtualHubNameByVpnServerConfigurationObject (Default)</span></span>
```
New-AzP2sVpnGateway -ResourceGroupName <String> -Name <String> -VpnGatewayScaleUnit <UInt32>
 -VirtualHubName <String> [-VpnServerConfiguration <PSVpnServerConfiguration>] -VpnClientAddressPool <String[]>
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="20a61-106">ByVirtualHubNameByVpnServerConfigurationResourceId</span><span class="sxs-lookup"><span data-stu-id="20a61-106">ByVirtualHubNameByVpnServerConfigurationResourceId</span></span>
```
New-AzP2sVpnGateway -ResourceGroupName <String> -Name <String> -VpnGatewayScaleUnit <UInt32>
 -VirtualHubName <String> -VpnServerConfigurationId <String> -VpnClientAddressPool <String[]>
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="20a61-107">ByVirtualHubObjectByVpnServerConfigurationObject</span><span class="sxs-lookup"><span data-stu-id="20a61-107">ByVirtualHubObjectByVpnServerConfigurationObject</span></span>
```
New-AzP2sVpnGateway -ResourceGroupName <String> -Name <String> -VpnGatewayScaleUnit <UInt32>
 -VirtualHub <PSVirtualHub> [-VpnServerConfiguration <PSVpnServerConfiguration>]
 -VpnClientAddressPool <String[]> [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="20a61-108">ByVirtualHubObjectByVpnServerConfigurationResourceId</span><span class="sxs-lookup"><span data-stu-id="20a61-108">ByVirtualHubObjectByVpnServerConfigurationResourceId</span></span>
```
New-AzP2sVpnGateway -ResourceGroupName <String> -Name <String> -VpnGatewayScaleUnit <UInt32>
 -VirtualHub <PSVirtualHub> -VpnServerConfigurationId <String> -VpnClientAddressPool <String[]>
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="20a61-109">ByVirtualHubResourceIdByVpnServerConfigurationObject</span><span class="sxs-lookup"><span data-stu-id="20a61-109">ByVirtualHubResourceIdByVpnServerConfigurationObject</span></span>
```
New-AzP2sVpnGateway -ResourceGroupName <String> -Name <String> -VpnGatewayScaleUnit <UInt32>
 -VirtualHubId <String> [-VpnServerConfiguration <PSVpnServerConfiguration>] -VpnClientAddressPool <String[]>
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="20a61-110">ByVirtualHubResourceIdByVpnServerConfigurationResourceId</span><span class="sxs-lookup"><span data-stu-id="20a61-110">ByVirtualHubResourceIdByVpnServerConfigurationResourceId</span></span>
```
New-AzP2sVpnGateway -ResourceGroupName <String> -Name <String> -VpnGatewayScaleUnit <UInt32>
 -VirtualHubId <String> -VpnServerConfigurationId <String> -VpnClientAddressPool <String[]> [-Tag <Hashtable>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="20a61-111">說明</span><span class="sxs-lookup"><span data-stu-id="20a61-111">DESCRIPTION</span></span>
<span data-ttu-id="20a61-112">**新的-AzP2sVpnGateway** Cmdlet 可讓您在 VirtualHub 下建立新的 P2SVpnGateway，以從指向網站用戶端到 Azure VirtualWan。</span><span class="sxs-lookup"><span data-stu-id="20a61-112">The **New-AzP2sVpnGateway** cmdlet enables you to create a new P2SVpnGateway under VirtualHub for Point to site connectivity from Point to site clients to Azure VirtualWan.</span></span>

## <span data-ttu-id="20a61-113">示例</span><span class="sxs-lookup"><span data-stu-id="20a61-113">EXAMPLES</span></span>

### <span data-ttu-id="20a61-114">範例1</span><span class="sxs-lookup"><span data-stu-id="20a61-114">Example 1</span></span>
```powershell
PS C:\> $virtualHub = Get-AzVirtualHub -ResourceGroupName P2SCortexGATesting -Name WestUsVirtualHub
PS C:\> $vpnServerConfig1 = Get-AzVpnServerConfiguration -ResourceGroupName P2SCortexGATesting -Name WestUsConfig
PS C:\> $vpnClientAddressSpaces = New-Object string[] 1
PS C:\> $vpnClientAddressSpaces[0] = "192.168.2.0/24"
PS C:\> $createdP2SVpnGateway = New-AzP2sVpnGateway -ResourceGroupName P2SCortexGATesting -Name 683482ade8564515aed4b8448c9757ea-westus-gw -VirtualHub $virtualHub -VpnGatewayScaleUnit 1 -VpnClientAddressPool $vpnClientAddressSpaces -VpnServerConfiguration $vpnServerConfig1

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

<span data-ttu-id="20a61-115">**新的-AzP2sVpnGateway** Cmdlet 可讓您在 VirtualHub 中建立新的 P2SVpnGateway，以指向 [網站連線]。</span><span class="sxs-lookup"><span data-stu-id="20a61-115">The **New-AzP2sVpnGateway** cmdlet enables you to create a new P2SVpnGateway under VirtualHub for Point to site connectivity.</span></span>

## <span data-ttu-id="20a61-116">參數</span><span class="sxs-lookup"><span data-stu-id="20a61-116">PARAMETERS</span></span>

### <span data-ttu-id="20a61-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="20a61-117">-AsJob</span></span>
<span data-ttu-id="20a61-118">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="20a61-118">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="20a61-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="20a61-119">-DefaultProfile</span></span>
<span data-ttu-id="20a61-120">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="20a61-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="20a61-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="20a61-121">-Name</span></span>
<span data-ttu-id="20a61-122">資源名稱。</span><span class="sxs-lookup"><span data-stu-id="20a61-122">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName, P2SVpnGatewayName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="20a61-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="20a61-123">-ResourceGroupName</span></span>
<span data-ttu-id="20a61-124">資源名稱。</span><span class="sxs-lookup"><span data-stu-id="20a61-124">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="20a61-125">-Tag</span><span class="sxs-lookup"><span data-stu-id="20a61-125">-Tag</span></span>
<span data-ttu-id="20a61-126">代表資源標記的 hashtable。</span><span class="sxs-lookup"><span data-stu-id="20a61-126">A hashtable which represents resource tags.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="20a61-127">-VirtualHub</span><span class="sxs-lookup"><span data-stu-id="20a61-127">-VirtualHub</span></span>
<span data-ttu-id="20a61-128">此 P2SVpnGateway 需要關聯的 VirtualHub。</span><span class="sxs-lookup"><span data-stu-id="20a61-128">The VirtualHub this P2SVpnGateway needs to be associated with.</span></span>

```yaml
Type: PSVirtualHub
Parameter Sets: ByVirtualHubObjectByVpnServerConfigurationObject, ByVirtualHubObjectByVpnServerConfigurationResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="20a61-129">-VirtualHubId</span><span class="sxs-lookup"><span data-stu-id="20a61-129">-VirtualHubId</span></span>
<span data-ttu-id="20a61-130">此 P2SVpnGateway 需要關聯之 VirtualHub 的識別碼。</span><span class="sxs-lookup"><span data-stu-id="20a61-130">The Id of the VirtualHub this P2SVpnGateway needs to be associated with.</span></span>

```yaml
Type: String
Parameter Sets: ByVirtualHubResourceIdByVpnServerConfigurationObject, ByVirtualHubResourceIdByVpnServerConfigurationResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="20a61-131">-VirtualHubName</span><span class="sxs-lookup"><span data-stu-id="20a61-131">-VirtualHubName</span></span>
<span data-ttu-id="20a61-132">此 P2SVpnGateway 需要關聯之 VirtualHub 的識別碼。</span><span class="sxs-lookup"><span data-stu-id="20a61-132">The Id of the VirtualHub this P2SVpnGateway needs to be associated with.</span></span>

```yaml
Type: String
Parameter Sets: ByVirtualHubNameByVpnServerConfigurationObject, ByVirtualHubNameByVpnServerConfigurationResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="20a61-133">-VpnClientAddressPool</span><span class="sxs-lookup"><span data-stu-id="20a61-133">-VpnClientAddressPool</span></span>
<span data-ttu-id="20a61-134">P2S VpnClient AddressPool P2SVpnGateway P2SConnectionConfiguration。</span><span class="sxs-lookup"><span data-stu-id="20a61-134">P2S VpnClient AddressPool for this P2SVpnGateway P2SConnectionConfiguration.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="20a61-135">-VpnGatewayScaleUnit</span><span class="sxs-lookup"><span data-stu-id="20a61-135">-VpnGatewayScaleUnit</span></span>
<span data-ttu-id="20a61-136">此 P2SVpnGateway 的縮放單位。</span><span class="sxs-lookup"><span data-stu-id="20a61-136">The scale unit for this P2SVpnGateway.</span></span>

```yaml
Type: UInt32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="20a61-137">-VpnServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="20a61-137">-VpnServerConfiguration</span></span>
<span data-ttu-id="20a61-138">要附加到此 P2SVpnGateway 的 VpnServerConfiguration。</span><span class="sxs-lookup"><span data-stu-id="20a61-138">The VpnServerConfiguration to be attached to this P2SVpnGateway.</span></span>

```yaml
Type: PSVpnServerConfiguration
Parameter Sets: ByVirtualHubNameByVpnServerConfigurationObject, ByVirtualHubObjectByVpnServerConfigurationObject, ByVirtualHubResourceIdByVpnServerConfigurationObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="20a61-139">-VpnServerConfigurationId</span><span class="sxs-lookup"><span data-stu-id="20a61-139">-VpnServerConfigurationId</span></span>
<span data-ttu-id="20a61-140">此 P2SVpnGateway 將附加到的 Vpn 伺服器設定物件的識別碼。</span><span class="sxs-lookup"><span data-stu-id="20a61-140">The id of Vpn server configuration object this P2SVpnGateway will be attached to.</span></span>

```yaml
Type: String
Parameter Sets: ByVirtualHubNameByVpnServerConfigurationResourceId, ByVirtualHubObjectByVpnServerConfigurationResourceId, ByVirtualHubResourceIdByVpnServerConfigurationResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="20a61-141">-確認</span><span class="sxs-lookup"><span data-stu-id="20a61-141">-Confirm</span></span>
<span data-ttu-id="20a61-142">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="20a61-142">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="20a61-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="20a61-143">-WhatIf</span></span>
<span data-ttu-id="20a61-144">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="20a61-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="20a61-145">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="20a61-145">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="20a61-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="20a61-146">CommonParameters</span></span>
<span data-ttu-id="20a61-147">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="20a61-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="20a61-148">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="20a61-148">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="20a61-149">輸入</span><span class="sxs-lookup"><span data-stu-id="20a61-149">INPUTS</span></span>

### <span data-ttu-id="20a61-150">PSVirtualHub 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="20a61-150">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>
<span data-ttu-id="20a61-151">PSVpnServerConfiguration 中的 [system.object] 命令。</span><span class="sxs-lookup"><span data-stu-id="20a61-151">System.String Microsoft.Azure.Commands.Network.Models.PSVpnServerConfiguration</span></span>

## <span data-ttu-id="20a61-152">輸出</span><span class="sxs-lookup"><span data-stu-id="20a61-152">OUTPUTS</span></span>

### <span data-ttu-id="20a61-153">PSP2SVpnGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="20a61-153">Microsoft.Azure.Commands.Network.Models.PSP2SVpnGateway</span></span>

## <span data-ttu-id="20a61-154">筆記</span><span class="sxs-lookup"><span data-stu-id="20a61-154">NOTES</span></span>

## <span data-ttu-id="20a61-155">相關連結</span><span class="sxs-lookup"><span data-stu-id="20a61-155">RELATED LINKS</span></span>
