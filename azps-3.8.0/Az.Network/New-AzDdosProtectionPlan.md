---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azddosprotectionplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzDdosProtectionPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzDdosProtectionPlan.md
ms.openlocfilehash: 39d45085c7f53bfeec6e18f38602fca48a3cefa3
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93966202"
---
# <span data-ttu-id="8f7fa-101">New-AzDdosProtectionPlan</span><span class="sxs-lookup"><span data-stu-id="8f7fa-101">New-AzDdosProtectionPlan</span></span>

## <span data-ttu-id="8f7fa-102">摘要</span><span class="sxs-lookup"><span data-stu-id="8f7fa-102">SYNOPSIS</span></span>
<span data-ttu-id="8f7fa-103">建立 DDoS 保護方案。</span><span class="sxs-lookup"><span data-stu-id="8f7fa-103">Creates a DDoS protection plan.</span></span>

## <span data-ttu-id="8f7fa-104">句法</span><span class="sxs-lookup"><span data-stu-id="8f7fa-104">SYNTAX</span></span>

```
New-AzDdosProtectionPlan -ResourceGroupName <String> -Name <String> -Location <String> [-Tag <Hashtable>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8f7fa-105">說明</span><span class="sxs-lookup"><span data-stu-id="8f7fa-105">DESCRIPTION</span></span>
<span data-ttu-id="8f7fa-106">New-AzDdosProtectionPlan Cmdlet 會建立 DDoS 保護方案。</span><span class="sxs-lookup"><span data-stu-id="8f7fa-106">The New-AzDdosProtectionPlan cmdlet creates a DDoS protection plan.</span></span>

## <span data-ttu-id="8f7fa-107">示例</span><span class="sxs-lookup"><span data-stu-id="8f7fa-107">EXAMPLES</span></span>

### <span data-ttu-id="8f7fa-108">範例1：使用新的虛擬網路建立並關聯 DDoS 保護方案</span><span class="sxs-lookup"><span data-stu-id="8f7fa-108">Example 1: Create and associate a DDoS protection plan with a new virtual network</span></span>
```
D:\> $ddosProtectionPlan = New-AzDdosProtectionPlan -ResourceGroupName ResourceGroupName -Name DdosProtectionPlanName -Location "West US"
D:\> $subnet = New-AzVirtualNetworkSubnetConfig -Name SubnetName -AddressPrefix 10.0.1.0/24
D:\> $vnet = New-AzVirtualNetwork -Name VnetName -ResourceGroupName ResourceGroupName -Location "West US" -AddressPrefix 10.0.0.0/16 -DnsServer 8.8.8.8 -Subnet $subnet -EnableDdoSProtection -DdosProtectionPlanId $ddosProtectionPlan.Id
```

<span data-ttu-id="8f7fa-109">首先，我們會使用 **新的-AzDdosProtectionPlan** 命令來建立新的 DDoS 保護方案。</span><span class="sxs-lookup"><span data-stu-id="8f7fa-109">First, we create a new DDoS Protection plan with the **New-AzDdosProtectionPlan** command.</span></span>
<span data-ttu-id="8f7fa-110">接著，我們會使用 **新的 AzVirtualNetwork** 建立新的虛擬網路，我們會在參數 **DdosProtectionPlanId** 中指定新建立的方案的識別碼。</span><span class="sxs-lookup"><span data-stu-id="8f7fa-110">Then, we create a new virtual network with **New-AzVirtualNetwork** and we specify the ID of the newly created plan in the parameter **DdosProtectionPlanId**.</span></span> <span data-ttu-id="8f7fa-111">在這種情況下，因為我們會將虛擬網路與方案進行關聯，所以我們也可以指定參數 **EnableDdoSProtection** 。</span><span class="sxs-lookup"><span data-stu-id="8f7fa-111">In this case, since we are associating the virtual network with a plan, we can also specify the parameter **EnableDdoSProtection**.</span></span>

### <span data-ttu-id="8f7fa-112">範例2：建立與現有虛擬網路的 DDoS 保護方案並加以關聯</span><span class="sxs-lookup"><span data-stu-id="8f7fa-112">Example 2: Create and associate a DDoS protection plan with an existing virtual network</span></span>
```
D:\> $ddosProtectionPlan = New-AzDdosProtectionPlan -ResourceGroupName ResourceGroupName -Name DdosProtectionPlanName -Location "West US"
D:\> $vnet = Get-AzVirtualNetwork -Name VnetName -ResourceGroupName ResourceGroupName
D:\> $vnet.DdosProtectionPlan = New-Object Microsoft.Azure.Commands.Network.Models.PSResourceId
D:\> $vnet.DdosProtectionPlan.Id = $ddosProtectionPlan.Id
D:\> $vnet.EnableDdosProtection = $true
D:\> $vnet | Set-AzVirtualNetwork


Name                   : VnetName
ResourceGroupName      : ResourceGroupName
Location               : westus
Id                     : /subscriptions/d1dbd366-9871-45ac-84b7-fb318152a9e0/resourceGroups/ResourceGroupName/providers/Microsoft.Network/virtualNetworks/VnetName
Etag                   : W/"fbf41754-3c13-43fd-bb5b-fcc37d5e1cbb"
ResourceGuid           : fcb7bc1e-ee0d-4005-b3f1-feda76e3756c
ProvisioningState      : Succeeded
Tags                   :
AddressSpace           : {
                           "AddressPrefixes": [
                             "10.0.0.0/16"
                           ]
                         }
DhcpOptions            : {
                           "DnsServers": [
                             "8.8.8.8"
                           ]
                         }
Subnets                : [
                           {
                             "Name": "SubnetName",
                             "Etag": "W/\"fbf41754-3c13-43fd-bb5b-fcc37d5e1cbb\"",
                             "Id": "/subscriptions/d1dbd366-9871-45ac-84b7-fb318152a9e0/resourceGroups/ResourceGroupName/providers/Microsoft.Network/virtualNetworks/VnetName/subnets/SubnetName",
                             "AddressPrefix": "10.0.1.0/24",
                             "IpConfigurations": [],
                             "ResourceNavigationLinks": [],
                             "ServiceEndpoints": [],
                             "ProvisioningState": "Succeeded"
                           }
                         ]
VirtualNetworkPeerings : []
EnableDdosProtection   : true
DdosProtectionPlan     : {
                           "Id": "/subscriptions/d1dbd366-9871-45ac-84b7-fb318152a9e0/resourceGroups/ResourceGroupName/providers/Microsoft.Network/ddosProtectionPlans/DdosProtectionPlanName"
                         }
EnableVmProtection     : false
```

<span data-ttu-id="8f7fa-113">首先，我們會使用 **新的-AzDdosProtectionPlan** 命令來建立新的 DDoS 保護方案。</span><span class="sxs-lookup"><span data-stu-id="8f7fa-113">First, we create a new DDoS Protection plan with the **New-AzDdosProtectionPlan** command.</span></span>
<span data-ttu-id="8f7fa-114">其次，我們會取得我們想要與計畫建立關聯的虛擬網路最新版本。</span><span class="sxs-lookup"><span data-stu-id="8f7fa-114">Second, we get the most updated version of the virtual network we want to associate with the plan.</span></span> <span data-ttu-id="8f7fa-115">我們會使用 **PSResourceId** 物件來更新屬性 **DdosProtectionPlan** ，其中包含新建立的方案之 ID 的參照。</span><span class="sxs-lookup"><span data-stu-id="8f7fa-115">We update the property **DdosProtectionPlan** with a **PSResourceId** object containing a reference to the ID of the newly created plan.</span></span> <span data-ttu-id="8f7fa-116">在這種情況下，如果我們將虛擬網路與 DDoS 保護方案關聯，我們也可以將標誌 **EnableDdosProtection** 設定為 true。</span><span class="sxs-lookup"><span data-stu-id="8f7fa-116">In this case, if we associate the virtual network with a DDoS protection plan, we can also set the flag **EnableDdosProtection** to true.</span></span>
<span data-ttu-id="8f7fa-117">最後，我們會將本機變數組成 **AzVirtualNetwork** ，以保留新的狀態。</span><span class="sxs-lookup"><span data-stu-id="8f7fa-117">Finally, we persist the new state by piping the local variable into **Set-AzVirtualNetwork**.</span></span>

## <span data-ttu-id="8f7fa-118">參數</span><span class="sxs-lookup"><span data-stu-id="8f7fa-118">PARAMETERS</span></span>

### <span data-ttu-id="8f7fa-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8f7fa-119">-AsJob</span></span>
<span data-ttu-id="8f7fa-120">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="8f7fa-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="8f7fa-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8f7fa-121">-DefaultProfile</span></span>
<span data-ttu-id="8f7fa-122">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="8f7fa-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8f7fa-123">-位置</span><span class="sxs-lookup"><span data-stu-id="8f7fa-123">-Location</span></span>
<span data-ttu-id="8f7fa-124">指定要建立之 DDoS 保護方案的位置。</span><span class="sxs-lookup"><span data-stu-id="8f7fa-124">Specifies the location of the DDoS protection plan to be created.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8f7fa-125">-名稱</span><span class="sxs-lookup"><span data-stu-id="8f7fa-125">-Name</span></span>
<span data-ttu-id="8f7fa-126">指定要建立的 DDoS 保護方案名稱。</span><span class="sxs-lookup"><span data-stu-id="8f7fa-126">Specifies the name of the DDoS protection plan to be created.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8f7fa-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8f7fa-127">-ResourceGroupName</span></span>
<span data-ttu-id="8f7fa-128">指定要建立之 DDoS 保護方案的 [資源] 群組。</span><span class="sxs-lookup"><span data-stu-id="8f7fa-128">Specifies the resource group of the DDoS protection plan to be created.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8f7fa-129">-Tag</span><span class="sxs-lookup"><span data-stu-id="8f7fa-129">-Tag</span></span>
<span data-ttu-id="8f7fa-130">代表資源標記的 hashtable。</span><span class="sxs-lookup"><span data-stu-id="8f7fa-130">A hashtable which represents resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8f7fa-131">-確認</span><span class="sxs-lookup"><span data-stu-id="8f7fa-131">-Confirm</span></span>
<span data-ttu-id="8f7fa-132">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="8f7fa-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8f7fa-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8f7fa-133">-WhatIf</span></span>
<span data-ttu-id="8f7fa-134">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="8f7fa-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8f7fa-135">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="8f7fa-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8f7fa-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8f7fa-136">CommonParameters</span></span>
<span data-ttu-id="8f7fa-137">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="8f7fa-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8f7fa-138">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="8f7fa-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8f7fa-139">輸入</span><span class="sxs-lookup"><span data-stu-id="8f7fa-139">INPUTS</span></span>

### <span data-ttu-id="8f7fa-140">System.object</span><span class="sxs-lookup"><span data-stu-id="8f7fa-140">System.String</span></span>

### <span data-ttu-id="8f7fa-141">[System.object] 集合. Hashtable</span><span class="sxs-lookup"><span data-stu-id="8f7fa-141">System.Collections.Hashtable</span></span>

## <span data-ttu-id="8f7fa-142">輸出</span><span class="sxs-lookup"><span data-stu-id="8f7fa-142">OUTPUTS</span></span>

### <span data-ttu-id="8f7fa-143">Microsoft.Azure.Commands.Network.Models.PSDdosProtectionPlan</span><span class="sxs-lookup"><span data-stu-id="8f7fa-143">Microsoft.Azure.Commands.Network.Models.PSDdosProtectionPlan</span></span>

## <span data-ttu-id="8f7fa-144">筆記</span><span class="sxs-lookup"><span data-stu-id="8f7fa-144">NOTES</span></span>

## <span data-ttu-id="8f7fa-145">相關連結</span><span class="sxs-lookup"><span data-stu-id="8f7fa-145">RELATED LINKS</span></span>

[<span data-ttu-id="8f7fa-146">AzDdosProtectionPlan</span><span class="sxs-lookup"><span data-stu-id="8f7fa-146">Get-AzDdosProtectionPlan</span></span>](./Get-AzDdosProtectionPlan.md)

[<span data-ttu-id="8f7fa-147">移除-AzDdosProtectionPlan</span><span class="sxs-lookup"><span data-stu-id="8f7fa-147">Remove-AzDdosProtectionPlan</span></span>](./Remove-AzDdosProtectionPlan.md)

[<span data-ttu-id="8f7fa-148">新-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="8f7fa-148">New-AzVirtualNetwork</span></span>](./New-AzVirtualNetwork.md)

[<span data-ttu-id="8f7fa-149">Set-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="8f7fa-149">Set-AzVirtualNetwork</span></span>](./Set-AzVirtualNetwork.md)

[<span data-ttu-id="8f7fa-150">AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="8f7fa-150">Get-AzVirtualNetwork</span></span>](./Get-AzVirtualNetwork.md)