---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azuredosprotectionplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmDdosProtectionPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmDdosProtectionPlan.md
ms.openlocfilehash: 79a9f0cb2b46150c7746112553949b1bbcbaf1dc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93448351"
---
# <span data-ttu-id="41c69-101">New-AzureRmDdosProtectionPlan</span><span class="sxs-lookup"><span data-stu-id="41c69-101">New-AzureRmDdosProtectionPlan</span></span>

## <span data-ttu-id="41c69-102">摘要</span><span class="sxs-lookup"><span data-stu-id="41c69-102">SYNOPSIS</span></span>
<span data-ttu-id="41c69-103">建立 DDoS 保護方案。</span><span class="sxs-lookup"><span data-stu-id="41c69-103">Creates a DDoS protection plan.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="41c69-104">句法</span><span class="sxs-lookup"><span data-stu-id="41c69-104">SYNTAX</span></span>

```
New-AzureRmDdosProtectionPlan -ResourceGroupName <String> -Name <String> -Location <String> [-Tag <Hashtable>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="41c69-105">說明</span><span class="sxs-lookup"><span data-stu-id="41c69-105">DESCRIPTION</span></span>
<span data-ttu-id="41c69-106">New-AzureRmDdosProtectionPlan Cmdlet 會建立 DDoS 保護方案。</span><span class="sxs-lookup"><span data-stu-id="41c69-106">The New-AzureRmDdosProtectionPlan cmdlet creates a DDoS protection plan.</span></span>

## <span data-ttu-id="41c69-107">示例</span><span class="sxs-lookup"><span data-stu-id="41c69-107">EXAMPLES</span></span>

### <span data-ttu-id="41c69-108">範例1：使用新的虛擬網路建立並關聯 DDoS 保護方案</span><span class="sxs-lookup"><span data-stu-id="41c69-108">Example 1: Create and associate a DDoS protection plan with a new virtual network</span></span>
```
D:\> $ddosProtectionPlan = New-AzureRmDdosProtectionPlan -ResourceGroupName ResourceGroupName -Name DdosProtectionPlanName -Location "West US"
D:\> $subnet = New-AzureRmVirtualNetworkSubnetConfig -Name SubnetName -AddressPrefix 10.0.1.0/24
D:\> $vnet = New-AzureRmvirtualNetwork -Name VnetName -ResourceGroupName ResourceGroupName -Location "West US" -AddressPrefix 10.0.0.0/16 -DnsServer 8.8.8.8 -Subnet $subnet -EnableDdoSProtection -DdosProtectionPlanId $ddosProtectionPlan.Id
```

<span data-ttu-id="41c69-109">首先，我們會使用 **新的-AzureRmDdosProtectionPlan** 命令來建立新的 DDoS 保護方案。</span><span class="sxs-lookup"><span data-stu-id="41c69-109">First, we create a new DDoS Protection plan with the **New-AzureRmDdosProtectionPlan** command.</span></span>
<span data-ttu-id="41c69-110">接著，我們會使用 **新的 AzureRmvirtualNetwork** 建立新的虛擬網路，我們會在參數 **DdosProtectionPlanId** 中指定新建立的方案的識別碼。</span><span class="sxs-lookup"><span data-stu-id="41c69-110">Then, we create a new virtual network with **New-AzureRmvirtualNetwork** and we specify the ID of the newly created plan in the parameter **DdosProtectionPlanId**.</span></span> <span data-ttu-id="41c69-111">在這種情況下，因為我們會將虛擬網路與方案進行關聯，所以我們也可以指定參數 **EnableDdoSProtection** 。</span><span class="sxs-lookup"><span data-stu-id="41c69-111">In this case, since we are associating the virtual network with a plan, we can also specify the parameter **EnableDdoSProtection**.</span></span>

### <span data-ttu-id="41c69-112">範例2：建立與現有虛擬網路的 DDoS 保護方案並加以關聯</span><span class="sxs-lookup"><span data-stu-id="41c69-112">Example 2: Create and associate a DDoS protection plan with an existing virtual network</span></span>
```
D:\> $ddosProtectionPlan = New-AzureRmDdosProtectionPlan -ResourceGroupName ResourceGroupName -Name DdosProtectionPlanName -Location "West US"
D:\> $vnet = Get-AzureRmVirtualNetwork -Name VnetName -ResourceGroupName ResourceGroupName
D:\> $vnet.DdosProtectionPlan = New-Object Microsoft.Azure.Commands.Network.Models.PSResourceId
D:\> $vnet.DdosProtectionPlan.Id = $ddosProtectionPlan.Id
D:\> $vnet.EnableDdosProtection = $true
D:\> $vnet | Set-AzureRmVirtualNetwork


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

<span data-ttu-id="41c69-113">首先，我們會使用 **新的-AzureRmDdosProtectionPlan** 命令來建立新的 DDoS 保護方案。</span><span class="sxs-lookup"><span data-stu-id="41c69-113">First, we create a new DDoS Protection plan with the **New-AzureRmDdosProtectionPlan** command.</span></span>
<span data-ttu-id="41c69-114">其次，我們會取得我們想要與計畫建立關聯的虛擬網路最新版本。</span><span class="sxs-lookup"><span data-stu-id="41c69-114">Second, we get the most updated version of the virtual network we want to associate with the plan.</span></span> <span data-ttu-id="41c69-115">我們會使用 **PSResourceId** 物件來更新屬性 **DdosProtectionPlan** ，其中包含新建立的方案之 ID 的參照。</span><span class="sxs-lookup"><span data-stu-id="41c69-115">We update the property **DdosProtectionPlan** with a **PSResourceId** object containing a reference to the ID of the newly created plan.</span></span> <span data-ttu-id="41c69-116">在這種情況下，如果我們將虛擬網路與 DDoS 保護方案關聯，我們也可以將標誌 **EnableDdosProtection** 設定為 true。</span><span class="sxs-lookup"><span data-stu-id="41c69-116">In this case, if we associate the virtual network with a DDoS protection plan, we can also set the flag **EnableDdosProtection** to true.</span></span>
<span data-ttu-id="41c69-117">最後，我們會將本機變數組成 **AzureRmVirtualNetwork** ，以保留新的狀態。</span><span class="sxs-lookup"><span data-stu-id="41c69-117">Finally, we persist the new state by piping the local variable into **Set-AzureRmVirtualNetwork**.</span></span>

## <span data-ttu-id="41c69-118">參數</span><span class="sxs-lookup"><span data-stu-id="41c69-118">PARAMETERS</span></span>

### <span data-ttu-id="41c69-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="41c69-119">-AsJob</span></span>
<span data-ttu-id="41c69-120">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="41c69-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="41c69-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="41c69-121">-DefaultProfile</span></span>
<span data-ttu-id="41c69-122">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="41c69-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="41c69-123">-位置</span><span class="sxs-lookup"><span data-stu-id="41c69-123">-Location</span></span>
<span data-ttu-id="41c69-124">指定要建立之 DDoS 保護方案的位置。</span><span class="sxs-lookup"><span data-stu-id="41c69-124">Specifies the location of the DDoS protection plan to be created.</span></span>

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

### <span data-ttu-id="41c69-125">-名稱</span><span class="sxs-lookup"><span data-stu-id="41c69-125">-Name</span></span>
<span data-ttu-id="41c69-126">指定要建立的 DDoS 保護方案名稱。</span><span class="sxs-lookup"><span data-stu-id="41c69-126">Specifies the name of the DDoS protection plan to be created.</span></span>

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

### <span data-ttu-id="41c69-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="41c69-127">-ResourceGroupName</span></span>
<span data-ttu-id="41c69-128">指定要建立之 DDoS 保護方案的 [資源] 群組。</span><span class="sxs-lookup"><span data-stu-id="41c69-128">Specifies the resource group of the DDoS protection plan to be created.</span></span>

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

### <span data-ttu-id="41c69-129">-Tag</span><span class="sxs-lookup"><span data-stu-id="41c69-129">-Tag</span></span>
<span data-ttu-id="41c69-130">代表資源標記的 hashtable。</span><span class="sxs-lookup"><span data-stu-id="41c69-130">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="41c69-131">-確認</span><span class="sxs-lookup"><span data-stu-id="41c69-131">-Confirm</span></span>
<span data-ttu-id="41c69-132">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="41c69-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="41c69-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="41c69-133">-WhatIf</span></span>
<span data-ttu-id="41c69-134">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="41c69-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="41c69-135">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="41c69-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="41c69-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="41c69-136">CommonParameters</span></span>
<span data-ttu-id="41c69-137">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="41c69-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="41c69-138">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="41c69-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="41c69-139">輸入</span><span class="sxs-lookup"><span data-stu-id="41c69-139">INPUTS</span></span>

### <span data-ttu-id="41c69-140">System.object</span><span class="sxs-lookup"><span data-stu-id="41c69-140">System.String</span></span>

### <span data-ttu-id="41c69-141">[System.object] 集合. Hashtable</span><span class="sxs-lookup"><span data-stu-id="41c69-141">System.Collections.Hashtable</span></span>

## <span data-ttu-id="41c69-142">輸出</span><span class="sxs-lookup"><span data-stu-id="41c69-142">OUTPUTS</span></span>

### <span data-ttu-id="41c69-143">Microsoft.Azure.Commands.Network.Models.PSDdosProtectionPlan</span><span class="sxs-lookup"><span data-stu-id="41c69-143">Microsoft.Azure.Commands.Network.Models.PSDdosProtectionPlan</span></span>

## <span data-ttu-id="41c69-144">筆記</span><span class="sxs-lookup"><span data-stu-id="41c69-144">NOTES</span></span>

## <span data-ttu-id="41c69-145">相關連結</span><span class="sxs-lookup"><span data-stu-id="41c69-145">RELATED LINKS</span></span>

[<span data-ttu-id="41c69-146">AzureRmDdosProtectionPlan</span><span class="sxs-lookup"><span data-stu-id="41c69-146">Get-AzureRmDdosProtectionPlan</span></span>](./Get-AzureRmDdosProtectionPlan.md)

[<span data-ttu-id="41c69-147">移除-AzureRmDdosProtectionPlan</span><span class="sxs-lookup"><span data-stu-id="41c69-147">Remove-AzureRmDdosProtectionPlan</span></span>](./Remove-AzureRmDdosProtectionPlan.md)

[<span data-ttu-id="41c69-148">新-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="41c69-148">New-AzureRmVirtualNetwork</span></span>](./New-AzureRmVirtualNetwork.md)

[<span data-ttu-id="41c69-149">Set-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="41c69-149">Set-AzureRmVirtualNetwork</span></span>](./Set-AzureRmVirtualNetwork.md)

[<span data-ttu-id="41c69-150">AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="41c69-150">Get-AzureRmVirtualNetwork</span></span>](./Get-AzureRmVirtualNetwork.md)
