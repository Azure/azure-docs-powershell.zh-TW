---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/update-azvirtualhubvnetconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVirtualHubVnetConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVirtualHubVnetConnection.md
ms.openlocfilehash: e3ba40bf4527571ed6b3396a9208a9a0931a7be7
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93799109"
---
# <span data-ttu-id="4a9ee-101">Update-AzVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="4a9ee-101">Update-AzVirtualHubVnetConnection</span></span>

## <span data-ttu-id="4a9ee-102">摘要</span><span class="sxs-lookup"><span data-stu-id="4a9ee-102">SYNOPSIS</span></span>
<span data-ttu-id="4a9ee-103">更新現有的 HubVirtualNetworkConnection。</span><span class="sxs-lookup"><span data-stu-id="4a9ee-103">Updates an existing HubVirtualNetworkConnection.</span></span>

## <span data-ttu-id="4a9ee-104">句法</span><span class="sxs-lookup"><span data-stu-id="4a9ee-104">SYNTAX</span></span>

### <span data-ttu-id="4a9ee-105">ByHubVirtualNetworkConnectionName (預設) </span><span class="sxs-lookup"><span data-stu-id="4a9ee-105">ByHubVirtualNetworkConnectionName (Default)</span></span>
```
Update-AzVirtualHubVnetConnection -ResourceGroupName <String> -ParentResourceName <String> -Name <String>
 -EnableInternetSecurity <Boolean> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="4a9ee-106">ByHubVirtualNetworkConnectionObject</span><span class="sxs-lookup"><span data-stu-id="4a9ee-106">ByHubVirtualNetworkConnectionObject</span></span>
```
Update-AzVirtualHubVnetConnection -InputObject <PSHubVirtualNetworkConnection>
 -EnableInternetSecurity <Boolean> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="4a9ee-107">ByHubVirtualNetworkConnectionResourceId</span><span class="sxs-lookup"><span data-stu-id="4a9ee-107">ByHubVirtualNetworkConnectionResourceId</span></span>
```
Update-AzVirtualHubVnetConnection -ResourceId <String> -EnableInternetSecurity <Boolean> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4a9ee-108">說明</span><span class="sxs-lookup"><span data-stu-id="4a9ee-108">DESCRIPTION</span></span>
<span data-ttu-id="4a9ee-109">更新現有的 HubVirtualNetworkConnection。</span><span class="sxs-lookup"><span data-stu-id="4a9ee-109">Updates an existing HubVirtualNetworkConnection.</span></span>

## <span data-ttu-id="4a9ee-110">示例</span><span class="sxs-lookup"><span data-stu-id="4a9ee-110">EXAMPLES</span></span>

### <span data-ttu-id="4a9ee-111">範例1</span><span class="sxs-lookup"><span data-stu-id="4a9ee-111">Example 1</span></span>
```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $frontendSubnet = New-AzVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24"
PS C:\> $backendSubnet  = New-AzVirtualNetworkSubnetConfig -Name backendSubnet  -AddressPrefix "10.0.2.0/24"
PS C:\> $remoteVirtualNetwork = New-AzVirtualNetwork -Name "MyVirtualNetwork" -ResourceGroupName "testRG" -Location "West US" -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet,$backendSubnet
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName "testRG" -Name "myVirtualWAN" -Location "West US"
PS C:\> New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.1.0/24"
PS C:\> New-AzVirtualHubVnetConnection -ResourceGroupName "testRG" -VirtualHubName "westushub" -Name "testvnetconnection" -RemoteVirtualNetwork $remoteVirtualNetwork
PS C:\> Update-AzVirtualHubVnetConnection -ResourceGroupName "testRG" -VirtualHubName "westushub" -Name "testvnetconnection" -EnableInternetSecurity $true
Name                   : testvnetconnection
Id                     : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualHubs/westushub/hubVirtualNetworkConnections/testvnetconnection
RemoteVirtualNetwork   : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualNetworks/MyVirtualNetwork
EnableInternetSecurity : True
ProvisioningState      : Succeeded
```

<span data-ttu-id="4a9ee-112">上述將會在 Azure 中的該資源群組中建立資源群組、虛擬 WAN、虛擬網路、虛擬中心（在美國）。</span><span class="sxs-lookup"><span data-stu-id="4a9ee-112">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub in Central US in that resource group in Azure.</span></span> <span data-ttu-id="4a9ee-113">同時也會建立一個虛擬網路連線，讓它對虛擬中樞而言是虛擬網路。</span><span class="sxs-lookup"><span data-stu-id="4a9ee-113">A Virtual Network Connection is also created which is peer the Virtual Network to the Virtual Hub.</span></span> <span data-ttu-id="4a9ee-114">然後更新此虛擬網路連線以啟用網際網路安全性。</span><span class="sxs-lookup"><span data-stu-id="4a9ee-114">This Virtual Network Connection is then updated to enable internet security.</span></span>

## <span data-ttu-id="4a9ee-115">參數</span><span class="sxs-lookup"><span data-stu-id="4a9ee-115">PARAMETERS</span></span>

### <span data-ttu-id="4a9ee-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4a9ee-116">-AsJob</span></span>
<span data-ttu-id="4a9ee-117">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="4a9ee-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="4a9ee-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4a9ee-118">-DefaultProfile</span></span>
<span data-ttu-id="4a9ee-119">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="4a9ee-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4a9ee-120">-EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="4a9ee-120">-EnableInternetSecurity</span></span>
<span data-ttu-id="4a9ee-121">針對此連線啟用網際網路安全性。</span><span class="sxs-lookup"><span data-stu-id="4a9ee-121">Enable internet security for this connection.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:
Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4a9ee-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4a9ee-122">-InputObject</span></span>
<span data-ttu-id="4a9ee-123">要修改的 hubvirtualnetworkconnection 資源。</span><span class="sxs-lookup"><span data-stu-id="4a9ee-123">The hubvirtualnetworkconnection resource to modify.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSHubVirtualNetworkConnection
Parameter Sets: ByHubVirtualNetworkConnectionObject
Aliases: HubVirtualNetworkConnection
Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4a9ee-124">-名稱</span><span class="sxs-lookup"><span data-stu-id="4a9ee-124">-Name</span></span>
<span data-ttu-id="4a9ee-125">資源名稱。</span><span class="sxs-lookup"><span data-stu-id="4a9ee-125">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByHubVirtualNetworkConnectionName
Aliases: ResourceName, HubVirtualNetworkConnectionName
Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4a9ee-126">-ParentResourceName</span><span class="sxs-lookup"><span data-stu-id="4a9ee-126">-ParentResourceName</span></span>
<span data-ttu-id="4a9ee-127">父資源名稱。</span><span class="sxs-lookup"><span data-stu-id="4a9ee-127">The parent resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByHubVirtualNetworkConnectionName
Aliases: VirtualHubName, ParentVirtualHubName
Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4a9ee-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4a9ee-128">-ResourceGroupName</span></span>
<span data-ttu-id="4a9ee-129">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="4a9ee-129">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByHubVirtualNetworkConnectionName
Aliases:
Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4a9ee-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4a9ee-130">-ResourceId</span></span>
<span data-ttu-id="4a9ee-131">要修改之 hubvirtualnetworkconnection 資源的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="4a9ee-131">The resource id of the hubvirtualnetworkconnection resource to modify.</span></span>

```yaml
Type: System.String
Parameter Sets: ByHubVirtualNetworkConnectionResourceId
Aliases: HubVirtualNetworkConnectionId
Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4a9ee-132">-確認</span><span class="sxs-lookup"><span data-stu-id="4a9ee-132">-Confirm</span></span>
<span data-ttu-id="4a9ee-133">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="4a9ee-133">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4a9ee-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4a9ee-134">-WhatIf</span></span>
<span data-ttu-id="4a9ee-135">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="4a9ee-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4a9ee-136">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="4a9ee-136">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4a9ee-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4a9ee-137">CommonParameters</span></span>
<span data-ttu-id="4a9ee-138">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="4a9ee-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4a9ee-139">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="4a9ee-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4a9ee-140">輸入</span><span class="sxs-lookup"><span data-stu-id="4a9ee-140">INPUTS</span></span>

### <span data-ttu-id="4a9ee-141">System.object</span><span class="sxs-lookup"><span data-stu-id="4a9ee-141">System.String</span></span>

### <span data-ttu-id="4a9ee-142">PSHubVirtualNetworkConnection 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="4a9ee-142">Microsoft.Azure.Commands.Network.Models.PSHubVirtualNetworkConnection</span></span>

## <span data-ttu-id="4a9ee-143">輸出</span><span class="sxs-lookup"><span data-stu-id="4a9ee-143">OUTPUTS</span></span>

### <span data-ttu-id="4a9ee-144">PSHubVirtualNetworkConnection 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="4a9ee-144">Microsoft.Azure.Commands.Network.Models.PSHubVirtualNetworkConnection</span></span>

## <span data-ttu-id="4a9ee-145">筆記</span><span class="sxs-lookup"><span data-stu-id="4a9ee-145">NOTES</span></span>

## <span data-ttu-id="4a9ee-146">相關連結</span><span class="sxs-lookup"><span data-stu-id="4a9ee-146">RELATED LINKS</span></span>