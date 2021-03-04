---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azddosprotectionplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzDdosProtectionPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzDdosProtectionPlan.md
ms.openlocfilehash: 0a8386a4ed91fa6e35adafbdc8ec532bb781f75e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101903565"
---
# <span data-ttu-id="0316b-101">New-AzDdosProtectionPlan</span><span class="sxs-lookup"><span data-stu-id="0316b-101">New-AzDdosProtectionPlan</span></span>

## <span data-ttu-id="0316b-102">簡介</span><span class="sxs-lookup"><span data-stu-id="0316b-102">SYNOPSIS</span></span>
<span data-ttu-id="0316b-103">建立 DDoS 保護計劃。</span><span class="sxs-lookup"><span data-stu-id="0316b-103">Creates a DDoS protection plan.</span></span>

## <span data-ttu-id="0316b-104">語法</span><span class="sxs-lookup"><span data-stu-id="0316b-104">SYNTAX</span></span>

```
New-AzDdosProtectionPlan -ResourceGroupName <String> -Name <String> -Location <String> [-Tag <Hashtable>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0316b-105">描述</span><span class="sxs-lookup"><span data-stu-id="0316b-105">DESCRIPTION</span></span>
<span data-ttu-id="0316b-106">Cmdlet New-AzDdosProtectionPlan建立 DDoS 保護計劃。</span><span class="sxs-lookup"><span data-stu-id="0316b-106">The New-AzDdosProtectionPlan cmdlet creates a DDoS protection plan.</span></span>

## <span data-ttu-id="0316b-107">例子</span><span class="sxs-lookup"><span data-stu-id="0316b-107">EXAMPLES</span></span>

### <span data-ttu-id="0316b-108">範例 1：建立 DDoS 保護計劃與新虛擬網路的關聯</span><span class="sxs-lookup"><span data-stu-id="0316b-108">Example 1: Create and associate a DDoS protection plan with a new virtual network</span></span>
```
D:\> $ddosProtectionPlan = New-AzDdosProtectionPlan -ResourceGroupName ResourceGroupName -Name DdosProtectionPlanName -Location "West US"
D:\> $subnet = New-AzVirtualNetworkSubnetConfig -Name SubnetName -AddressPrefix 10.0.1.0/24
D:\> $vnet = New-AzVirtualNetwork -Name VnetName -ResourceGroupName ResourceGroupName -Location "West US" -AddressPrefix 10.0.0.0/16 -DnsServer 8.8.8.8 -Subnet $subnet -EnableDdoSProtection -DdosProtectionPlanId $ddosProtectionPlan.Id
```

<span data-ttu-id="0316b-109">首先，我們使用 **New-AzDdosProtectionPlan** 命令來建立新的 DDoS Protection 方案。</span><span class="sxs-lookup"><span data-stu-id="0316b-109">First, we create a new DDoS Protection plan with the **New-AzDdosProtectionPlan** command.</span></span>
<span data-ttu-id="0316b-110">然後，我們使用 **New-AzVirtualNetwork** 建立新虛擬網路，然後在參數 **DdosProtectionPlanId** 中指定新建立計畫的識別碼。</span><span class="sxs-lookup"><span data-stu-id="0316b-110">Then, we create a new virtual network with **New-AzVirtualNetwork** and we specify the ID of the newly created plan in the parameter **DdosProtectionPlanId**.</span></span> <span data-ttu-id="0316b-111">在這個案例中，由於我們要將虛擬網路與計畫建立關聯，所以我們也可以指定 **EnableDdoSProtection 參數**。</span><span class="sxs-lookup"><span data-stu-id="0316b-111">In this case, since we are associating the virtual network with a plan, we can also specify the parameter **EnableDdoSProtection**.</span></span>

### <span data-ttu-id="0316b-112">範例 2：建立 DDoS 保護計劃與現有虛擬網路的關聯</span><span class="sxs-lookup"><span data-stu-id="0316b-112">Example 2: Create and associate a DDoS protection plan with an existing virtual network</span></span>
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

<span data-ttu-id="0316b-113">首先，我們使用 **New-AzDdosProtectionPlan** 命令來建立新的 DDoS Protection 方案。</span><span class="sxs-lookup"><span data-stu-id="0316b-113">First, we create a new DDoS Protection plan with the **New-AzDdosProtectionPlan** command.</span></span>
<span data-ttu-id="0316b-114">第二，我們會取得與計畫建立關聯的最新版本的虛擬網路。</span><span class="sxs-lookup"><span data-stu-id="0316b-114">Second, we get the most updated version of the virtual network we want to associate with the plan.</span></span> <span data-ttu-id="0316b-115">我們會使用 **PSResourceId** 物件更新 **屬性 DdosProtectionPlan，** 該物件包含新建立之計畫識別碼的參照。</span><span class="sxs-lookup"><span data-stu-id="0316b-115">We update the property **DdosProtectionPlan** with a **PSResourceId** object containing a reference to the ID of the newly created plan.</span></span> <span data-ttu-id="0316b-116">在這種情況下，如果我們將虛擬網路與 DDoS 保護計劃建立關聯，也可以將 **EnableDdosProtection** 標為 True。</span><span class="sxs-lookup"><span data-stu-id="0316b-116">In this case, if we associate the virtual network with a DDoS protection plan, we can also set the flag **EnableDdosProtection** to true.</span></span>
<span data-ttu-id="0316b-117">最後，我們將本地變數放入 **Set-AzVirtualNetwork** 中，以持續新的狀態。</span><span class="sxs-lookup"><span data-stu-id="0316b-117">Finally, we persist the new state by piping the local variable into **Set-AzVirtualNetwork**.</span></span>

## <span data-ttu-id="0316b-118">參數</span><span class="sxs-lookup"><span data-stu-id="0316b-118">PARAMETERS</span></span>

### <span data-ttu-id="0316b-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0316b-119">-AsJob</span></span>
<span data-ttu-id="0316b-120">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="0316b-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="0316b-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0316b-121">-DefaultProfile</span></span>
<span data-ttu-id="0316b-122">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="0316b-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0316b-123">-位置</span><span class="sxs-lookup"><span data-stu-id="0316b-123">-Location</span></span>
<span data-ttu-id="0316b-124">指定要建立 DDoS 保護計劃的位置。</span><span class="sxs-lookup"><span data-stu-id="0316b-124">Specifies the location of the DDoS protection plan to be created.</span></span>

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

### <span data-ttu-id="0316b-125">-名稱</span><span class="sxs-lookup"><span data-stu-id="0316b-125">-Name</span></span>
<span data-ttu-id="0316b-126">指定要建立 DDoS 保護計劃的名稱。</span><span class="sxs-lookup"><span data-stu-id="0316b-126">Specifies the name of the DDoS protection plan to be created.</span></span>

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

### <span data-ttu-id="0316b-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0316b-127">-ResourceGroupName</span></span>
<span data-ttu-id="0316b-128">指定要建立 DDoS 保護計劃的資源群組。</span><span class="sxs-lookup"><span data-stu-id="0316b-128">Specifies the resource group of the DDoS protection plan to be created.</span></span>

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

### <span data-ttu-id="0316b-129">-標記</span><span class="sxs-lookup"><span data-stu-id="0316b-129">-Tag</span></span>
<span data-ttu-id="0316b-130">代表資源標記的雜湊表。</span><span class="sxs-lookup"><span data-stu-id="0316b-130">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="0316b-131">-確認</span><span class="sxs-lookup"><span data-stu-id="0316b-131">-Confirm</span></span>
<span data-ttu-id="0316b-132">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="0316b-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0316b-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0316b-133">-WhatIf</span></span>
<span data-ttu-id="0316b-134">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="0316b-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0316b-135">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="0316b-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0316b-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0316b-136">CommonParameters</span></span>
<span data-ttu-id="0316b-137">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="0316b-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0316b-138">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="0316b-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0316b-139">輸入</span><span class="sxs-lookup"><span data-stu-id="0316b-139">INPUTS</span></span>

### <span data-ttu-id="0316b-140">System.String</span><span class="sxs-lookup"><span data-stu-id="0316b-140">System.String</span></span>

### <span data-ttu-id="0316b-141">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="0316b-141">System.Collections.Hashtable</span></span>

## <span data-ttu-id="0316b-142">輸出</span><span class="sxs-lookup"><span data-stu-id="0316b-142">OUTPUTS</span></span>

### <span data-ttu-id="0316b-143">Microsoft.Azure.Commands.Network.Models.PSDdosProtectionPlan</span><span class="sxs-lookup"><span data-stu-id="0316b-143">Microsoft.Azure.Commands.Network.Models.PSDdosProtectionPlan</span></span>

## <span data-ttu-id="0316b-144">筆記</span><span class="sxs-lookup"><span data-stu-id="0316b-144">NOTES</span></span>

## <span data-ttu-id="0316b-145">相關連結</span><span class="sxs-lookup"><span data-stu-id="0316b-145">RELATED LINKS</span></span>

[<span data-ttu-id="0316b-146">Get-AzDdosProtectionPlan</span><span class="sxs-lookup"><span data-stu-id="0316b-146">Get-AzDdosProtectionPlan</span></span>](./Get-AzDdosProtectionPlan.md)

[<span data-ttu-id="0316b-147">Remove-AzDdosProtectionPlan</span><span class="sxs-lookup"><span data-stu-id="0316b-147">Remove-AzDdosProtectionPlan</span></span>](./Remove-AzDdosProtectionPlan.md)

[<span data-ttu-id="0316b-148">New-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="0316b-148">New-AzVirtualNetwork</span></span>](./New-AzVirtualNetwork.md)

[<span data-ttu-id="0316b-149">Set-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="0316b-149">Set-AzVirtualNetwork</span></span>](./Set-AzVirtualNetwork.md)

[<span data-ttu-id="0316b-150">Get-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="0316b-150">Get-AzVirtualNetwork</span></span>](./Get-AzVirtualNetwork.md)