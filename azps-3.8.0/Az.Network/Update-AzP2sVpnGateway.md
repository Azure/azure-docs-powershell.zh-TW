---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/update-azp2svpngateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzP2sVpnGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzP2sVpnGateway.md
ms.openlocfilehash: 39fb3223b1a80b831874bbd833d6d0c97aace53f
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93796862"
---
# <span data-ttu-id="97eeb-101">Update-AzP2sVpnGateway</span><span class="sxs-lookup"><span data-stu-id="97eeb-101">Update-AzP2sVpnGateway</span></span>

## <span data-ttu-id="97eeb-102">摘要</span><span class="sxs-lookup"><span data-stu-id="97eeb-102">SYNOPSIS</span></span>
<span data-ttu-id="97eeb-103">在 [VirtualHub] 底下的 [網站連線] 底下，更新現有的 P2SVpnGateway。</span><span class="sxs-lookup"><span data-stu-id="97eeb-103">Update an existing P2SVpnGateway under VirtualHub for point to site connectivity.</span></span>

## <span data-ttu-id="97eeb-104">句法</span><span class="sxs-lookup"><span data-stu-id="97eeb-104">SYNTAX</span></span>

### <span data-ttu-id="97eeb-105">ByP2SVpnGatewayNameNoVpnServerConfigurationUpdate (預設) </span><span class="sxs-lookup"><span data-stu-id="97eeb-105">ByP2SVpnGatewayNameNoVpnServerConfigurationUpdate (Default)</span></span>
```
Update-AzP2sVpnGateway -ResourceGroupName <String> -Name <String> [-VpnClientAddressPool <String[]>]
 [-VpnGatewayScaleUnit <UInt32>] [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="97eeb-106">ByP2SVpnGatewayNameByVpnServerConfigurationObject</span><span class="sxs-lookup"><span data-stu-id="97eeb-106">ByP2SVpnGatewayNameByVpnServerConfigurationObject</span></span>
```
Update-AzP2sVpnGateway -ResourceGroupName <String> -Name <String> [-VpnClientAddressPool <String[]>]
 [-VpnServerConfiguration <PSVpnServerConfiguration>] [-VpnGatewayScaleUnit <UInt32>] [-Tag <Hashtable>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="97eeb-107">ByP2SVpnGatewayNameByVpnServerConfigurationResourceId</span><span class="sxs-lookup"><span data-stu-id="97eeb-107">ByP2SVpnGatewayNameByVpnServerConfigurationResourceId</span></span>
```
Update-AzP2sVpnGateway -ResourceGroupName <String> -Name <String> [-VpnClientAddressPool <String[]>]
 -VpnServerConfigurationId <String> [-VpnGatewayScaleUnit <UInt32>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="97eeb-108">ByP2SVpnGatewayObjectNoVpnServerConfigurationUpdate</span><span class="sxs-lookup"><span data-stu-id="97eeb-108">ByP2SVpnGatewayObjectNoVpnServerConfigurationUpdate</span></span>
```
Update-AzP2sVpnGateway -InputObject <PSP2SVpnGateway> [-VpnClientAddressPool <String[]>]
 [-VpnGatewayScaleUnit <UInt32>] [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="97eeb-109">ByP2SVpnGatewayObjectByVpnServerConfigurationObject</span><span class="sxs-lookup"><span data-stu-id="97eeb-109">ByP2SVpnGatewayObjectByVpnServerConfigurationObject</span></span>
```
Update-AzP2sVpnGateway -InputObject <PSP2SVpnGateway> [-VpnClientAddressPool <String[]>]
 [-VpnServerConfiguration <PSVpnServerConfiguration>] [-VpnGatewayScaleUnit <UInt32>] [-Tag <Hashtable>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="97eeb-110">ByP2SVpnGatewayObjectByVpnServerConfigurationResourceId</span><span class="sxs-lookup"><span data-stu-id="97eeb-110">ByP2SVpnGatewayObjectByVpnServerConfigurationResourceId</span></span>
```
Update-AzP2sVpnGateway -InputObject <PSP2SVpnGateway> [-VpnClientAddressPool <String[]>]
 -VpnServerConfigurationId <String> [-VpnGatewayScaleUnit <UInt32>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="97eeb-111">ByP2SVpnGatewayResourceIdNoVpnServerConfigurationUpdate</span><span class="sxs-lookup"><span data-stu-id="97eeb-111">ByP2SVpnGatewayResourceIdNoVpnServerConfigurationUpdate</span></span>
```
Update-AzP2sVpnGateway -ResourceId <String> [-VpnClientAddressPool <String[]>] [-VpnGatewayScaleUnit <UInt32>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="97eeb-112">ByP2SVpnGatewayResourceIdByVpnServerConfigurationObject</span><span class="sxs-lookup"><span data-stu-id="97eeb-112">ByP2SVpnGatewayResourceIdByVpnServerConfigurationObject</span></span>
```
Update-AzP2sVpnGateway -ResourceId <String> [-VpnClientAddressPool <String[]>]
 [-VpnServerConfiguration <PSVpnServerConfiguration>] [-VpnGatewayScaleUnit <UInt32>] [-Tag <Hashtable>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="97eeb-113">ByP2SVpnGatewayResourceIdByVpnServerConfigurationResourceId</span><span class="sxs-lookup"><span data-stu-id="97eeb-113">ByP2SVpnGatewayResourceIdByVpnServerConfigurationResourceId</span></span>
```
Update-AzP2sVpnGateway -ResourceId <String> [-VpnClientAddressPool <String[]>]
 -VpnServerConfigurationId <String> [-VpnGatewayScaleUnit <UInt32>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="97eeb-114">說明</span><span class="sxs-lookup"><span data-stu-id="97eeb-114">DESCRIPTION</span></span>
<span data-ttu-id="97eeb-115">**AzP2sVpnGateway** Cmdlet 可讓您在 VirtualHub 中使用新的 VpnClientAddressPool 或新 VpnServerConfiguration 或變更 VpnGatewayScaleUnit 來更新現有 P2SVpnGateway。</span><span class="sxs-lookup"><span data-stu-id="97eeb-115">The **Update-AzP2sVpnGateway** cmdlet enables you to update an existing P2SVpnGateway under VirtualHub with new VpnClientAddressPool or new VpnServerConfiguration or change of VpnGatewayScaleUnit.</span></span>

## <span data-ttu-id="97eeb-116">示例</span><span class="sxs-lookup"><span data-stu-id="97eeb-116">EXAMPLES</span></span>

### <span data-ttu-id="97eeb-117">範例1</span><span class="sxs-lookup"><span data-stu-id="97eeb-117">Example 1</span></span>
```powershell
PS C:\> $vpnClientAddressSpaces = New-Object string[] 1 
PS C:\> $vpnClientAddressSpaces[0] = "101.10.0.0/16"
PS C:\> Update-AzP2sVpnGateway -ResourceGroupName P2SCortexGATesting -Name 683482ade8564515aed4b8448c9757ea-westus-gw -VpnClientAddressPool $vpnClientAddressSpaces                                    

ResourceGroupName              : P2SCortexGATesting
Name                           : 683482ade8564515aed4b8448c9757ea-westus-gw
Id                             : /subscriptions/b1f1deed-af60-4bab-9223-65d340462e24/resourceGroups/P2SCortexGATesting/providers/Microsoft.Network/p2sVpnGateways/683482ade8564515a
                                 ed4b8448c9757ea-westus-gw
Location                       : westus
VpnGatewayScaleUnit            : 1
VirtualHub                     : /subscriptions/b1f1deed-af60-4bab-9223-65d340462e24/resourceGroups/P2SCortexGATesting/providers/Microsoft.Network/virtualHubs/NilamdWestUsVirtualH
                                 ub
VpnServerConfiguration         : /subscriptions/b1f1deed-af60-4bab-9223-65d340462e24/resourceGroups/P2SCortexGATesting/providers/Microsoft.Network/vpnServerConfigurations/NilamdWe
                                 stUsConfig
VpnServerConfigurationLocation :
VpnClientConnectionHealth      : null
Type                           : Microsoft.Network/p2sVpnGateways
ProvisioningState              : Succeeded
P2SConnectionConfigurations    : [
                                   {
                                     "ProvisioningState": "Succeeded",
                                     "VpnClientAddressPool": {
                                       "AddressPrefixes": [
                                         "101.10.0.0/16"
                                       ]
                                     },
                                     "Name": "P2SConnectionConfigDefault",
                                     "Etag": "W/\"d7debc2f-ccbb-4f00-bddc-42c99b52fda3\"",
                                     "Id": "/subscriptions/b1f1deed-af60-4bab-9223-65d340462e24/resourceGroups/P2SCortexGATesting/providers/Microsoft.Network/p2sVpnGateways/683482
                                 ade8564515aed4b8448c9757ea-westus-gw/p2sConnectionConfigurations/P2SConnectionConfigDefault"
                                   }
                                 ]
```

<span data-ttu-id="97eeb-118">**AzP2sVpnGateway** Cmdlet 可讓您在 VirtualHub 中使用新的 VpnClientAddressPool 來更新現有 P2SVpnGateway。</span><span class="sxs-lookup"><span data-stu-id="97eeb-118">The **Update-AzP2sVpnGateway** cmdlet enables you to update an existing P2SVpnGateway under VirtualHub with new VpnClientAddressPool.</span></span> <span data-ttu-id="97eeb-119">當指向網站用戶端與此 P2SVpnGateway 連線時，此 VpnClientAddressPool 的其中一個 ip 位址會指派給該用戶端。</span><span class="sxs-lookup"><span data-stu-id="97eeb-119">When Point to site client connects with this P2SVpnGateway, one of the ip address from this VpnClientAddressPool gets allocated to that client.</span></span>

## <span data-ttu-id="97eeb-120">參數</span><span class="sxs-lookup"><span data-stu-id="97eeb-120">PARAMETERS</span></span>

### <span data-ttu-id="97eeb-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="97eeb-121">-AsJob</span></span>
<span data-ttu-id="97eeb-122">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="97eeb-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="97eeb-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="97eeb-123">-DefaultProfile</span></span>
<span data-ttu-id="97eeb-124">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="97eeb-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="97eeb-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="97eeb-125">-InputObject</span></span>
<span data-ttu-id="97eeb-126">要修改的 p2s vpn 閘道物件</span><span class="sxs-lookup"><span data-stu-id="97eeb-126">The p2s vpn gateway object to be modified</span></span>

```yaml
Type: PSP2SVpnGateway
Parameter Sets: ByP2SVpnGatewayObjectNoVpnServerConfigurationUpdate, ByP2SVpnGatewayObjectByVpnServerConfigurationObject, ByP2SVpnGatewayObjectByVpnServerConfigurationResourceId
Aliases: P2SVpnGateway

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="97eeb-127">-名稱</span><span class="sxs-lookup"><span data-stu-id="97eeb-127">-Name</span></span>
<span data-ttu-id="97eeb-128">P2S vpn 閘道名稱。</span><span class="sxs-lookup"><span data-stu-id="97eeb-128">The P2S vpn gateway name.</span></span>

```yaml
Type: String
Parameter Sets: ByP2SVpnGatewayNameNoVpnServerConfigurationUpdate, ByP2SVpnGatewayNameByVpnServerConfigurationObject, ByP2SVpnGatewayNameByVpnServerConfigurationResourceId
Aliases: ResourceName, P2SVpnGatewayName, GatewayName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="97eeb-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="97eeb-129">-ResourceGroupName</span></span>
<span data-ttu-id="97eeb-130">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="97eeb-130">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByP2SVpnGatewayNameNoVpnServerConfigurationUpdate, ByP2SVpnGatewayNameByVpnServerConfigurationObject, ByP2SVpnGatewayNameByVpnServerConfigurationResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="97eeb-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="97eeb-131">-ResourceId</span></span>
<span data-ttu-id="97eeb-132">要修改之 P2SVpnGateway 的 Azure 資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="97eeb-132">The Azure resource ID of the P2SVpnGateway to be modified.</span></span>

```yaml
Type: String
Parameter Sets: ByP2SVpnGatewayResourceIdNoVpnServerConfigurationUpdate, ByP2SVpnGatewayResourceIdByVpnServerConfigurationObject, ByP2SVpnGatewayResourceIdByVpnServerConfigurationResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="97eeb-133">-Tag</span><span class="sxs-lookup"><span data-stu-id="97eeb-133">-Tag</span></span>
<span data-ttu-id="97eeb-134">代表資源標記的 hashtable。</span><span class="sxs-lookup"><span data-stu-id="97eeb-134">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="97eeb-135">-VpnClientAddressPool</span><span class="sxs-lookup"><span data-stu-id="97eeb-135">-VpnClientAddressPool</span></span>
<span data-ttu-id="97eeb-136">P2S VpnClient AddressPool P2SVpnGateway P2SConnectionConfiguration。</span><span class="sxs-lookup"><span data-stu-id="97eeb-136">P2S VpnClient AddressPool for this P2SVpnGateway P2SConnectionConfiguration.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="97eeb-137">-VpnGatewayScaleUnit</span><span class="sxs-lookup"><span data-stu-id="97eeb-137">-VpnGatewayScaleUnit</span></span>
<span data-ttu-id="97eeb-138">此 P2SVpnGateway 的縮放單位。</span><span class="sxs-lookup"><span data-stu-id="97eeb-138">The scale unit for this P2SVpnGateway.</span></span>

```yaml
Type: UInt32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="97eeb-139">-VpnServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="97eeb-139">-VpnServerConfiguration</span></span>
<span data-ttu-id="97eeb-140">要附加到此 P2SVpnGateway 的 VpnServerConfiguration。</span><span class="sxs-lookup"><span data-stu-id="97eeb-140">The VpnServerConfiguration to be attached to this P2SVpnGateway.</span></span>

```yaml
Type: PSVpnServerConfiguration
Parameter Sets: ByP2SVpnGatewayNameByVpnServerConfigurationObject, ByP2SVpnGatewayObjectByVpnServerConfigurationObject, ByP2SVpnGatewayResourceIdByVpnServerConfigurationObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="97eeb-141">-VpnServerConfigurationId</span><span class="sxs-lookup"><span data-stu-id="97eeb-141">-VpnServerConfigurationId</span></span>
<span data-ttu-id="97eeb-142">此 P2SVpnGateway 將附加到的 Vpn 伺服器設定物件的識別碼。</span><span class="sxs-lookup"><span data-stu-id="97eeb-142">The id of Vpn server configuration object this P2SVpnGateway will be attached to.</span></span>

```yaml
Type: String
Parameter Sets: ByP2SVpnGatewayNameByVpnServerConfigurationResourceId, ByP2SVpnGatewayObjectByVpnServerConfigurationResourceId, ByP2SVpnGatewayResourceIdByVpnServerConfigurationResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="97eeb-143">-確認</span><span class="sxs-lookup"><span data-stu-id="97eeb-143">-Confirm</span></span>
<span data-ttu-id="97eeb-144">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="97eeb-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="97eeb-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="97eeb-145">-WhatIf</span></span>
<span data-ttu-id="97eeb-146">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="97eeb-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="97eeb-147">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="97eeb-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="97eeb-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="97eeb-148">CommonParameters</span></span>
<span data-ttu-id="97eeb-149">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="97eeb-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="97eeb-150">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="97eeb-150">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="97eeb-151">輸入</span><span class="sxs-lookup"><span data-stu-id="97eeb-151">INPUTS</span></span>

### <span data-ttu-id="97eeb-152">PSP2SVpnGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="97eeb-152">Microsoft.Azure.Commands.Network.Models.PSP2SVpnGateway</span></span>
<span data-ttu-id="97eeb-153">PSVpnServerConfiguration 中的 [system.object] 命令。</span><span class="sxs-lookup"><span data-stu-id="97eeb-153">System.String Microsoft.Azure.Commands.Network.Models.PSVpnServerConfiguration</span></span>

## <span data-ttu-id="97eeb-154">輸出</span><span class="sxs-lookup"><span data-stu-id="97eeb-154">OUTPUTS</span></span>

### <span data-ttu-id="97eeb-155">PSP2SVpnGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="97eeb-155">Microsoft.Azure.Commands.Network.Models.PSP2SVpnGateway</span></span>

## <span data-ttu-id="97eeb-156">筆記</span><span class="sxs-lookup"><span data-stu-id="97eeb-156">NOTES</span></span>

## <span data-ttu-id="97eeb-157">相關連結</span><span class="sxs-lookup"><span data-stu-id="97eeb-157">RELATED LINKS</span></span>
