---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/remove-azddosprotectionplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzDdosProtectionPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzDdosProtectionPlan.md
ms.openlocfilehash: 8aad20fc16d160ba024dd3d4a9b6f14b65ad951e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101908085"
---
# <span data-ttu-id="5b24d-101">Remove-AzDdosProtectionPlan</span><span class="sxs-lookup"><span data-stu-id="5b24d-101">Remove-AzDdosProtectionPlan</span></span>

## <span data-ttu-id="5b24d-102">簡介</span><span class="sxs-lookup"><span data-stu-id="5b24d-102">SYNOPSIS</span></span>
<span data-ttu-id="5b24d-103">移除 DDoS 保護計劃。</span><span class="sxs-lookup"><span data-stu-id="5b24d-103">Removes a DDoS protection plan.</span></span>

## <span data-ttu-id="5b24d-104">語法</span><span class="sxs-lookup"><span data-stu-id="5b24d-104">SYNTAX</span></span>

```
Remove-AzDdosProtectionPlan -ResourceGroupName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5b24d-105">描述</span><span class="sxs-lookup"><span data-stu-id="5b24d-105">DESCRIPTION</span></span>
<span data-ttu-id="5b24d-106">Cmdlet Remove-AzDdosProtectionPlan移除 DDoS 保護計劃。</span><span class="sxs-lookup"><span data-stu-id="5b24d-106">The Remove-AzDdosProtectionPlan cmdlet removes a DDoS protection plan.</span></span>

## <span data-ttu-id="5b24d-107">例子</span><span class="sxs-lookup"><span data-stu-id="5b24d-107">EXAMPLES</span></span>

### <span data-ttu-id="5b24d-108">範例 1：移除空白的 DDoS 保護計劃</span><span class="sxs-lookup"><span data-stu-id="5b24d-108">Example 1: Remove an empty DDoS protection plan</span></span>
```
D:\> Remove-AzDdosProtectionPlan -ResourceGroupName ResourceGroupName -Name DdosProtectionPlan
```

<span data-ttu-id="5b24d-109">在此例中，我們會移除指定的 DDoS 保護方案。</span><span class="sxs-lookup"><span data-stu-id="5b24d-109">In this case, we remove a DDoS protection plan as specified.</span></span>

### <span data-ttu-id="5b24d-110">範例 2：移除與虛擬網路相關聯的 DDoS 保護計劃</span><span class="sxs-lookup"><span data-stu-id="5b24d-110">Example 2: Remove a DDoS protection plan associated with a virtual network</span></span>
```
D:\> $vnet = Get-AzVirtualNetwork -Name VnetName -ResourceGroupName ResourceGroupName
D:\> $vnet.DdosProtectionPlan = $null
D:\> $vnet.EnableDdosProtection = $false
D:\> $vnet | Set-AzVirtualNetwork


Name                   : VnetName
ResourceGroupName      : ResourceGroupName
Location               : westus
Id                     : /subscriptions/d1dbd366-9871-45ac-84b7-fb318152a9e0/resourceGroups/ResourceGroupName/providers/Microsoft.Network/virtualNetworks/VnetName
Etag                   : W/"65947351-747e-4686-aa8b-c40da58f6c8b"
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
                             "Etag": "W/\"65947351-747e-4686-aa8b-c40da58f6c8b\"",
                             "Id": "/subscriptions/d1dbd366-9871-45ac-84b7-fb318152a9e0/resourceGroups/ResourceGroupName/providers/Microsoft.Network/virtualNetworks/VnetName/subnets/SubnetName",
                             "AddressPrefix": "10.0.1.0/24",
                             "IpConfigurations": [],
                             "ResourceNavigationLinks": [],
                             "ServiceEndpoints": [],
                             "ProvisioningState": "Succeeded"
                           }
                         ]
VirtualNetworkPeerings : []
EnableDdosProtection   : false
DdosProtectionPlan     : null
EnableVmProtection     : false


D:\> Remove-AzDdosProtectionPlan -ResourceGroupName ResourceGroupName -Name DdosProtectionPlan
```

<span data-ttu-id="5b24d-111">如果 DDoS 保護方案與虛擬網路相關聯，就無法刪除。</span><span class="sxs-lookup"><span data-stu-id="5b24d-111">DDoS protection plans cannot be deleted if they are associated with a virtual network.</span></span> <span data-ttu-id="5b24d-112">因此，第一個步驟是取消兩個物件的關聯。</span><span class="sxs-lookup"><span data-stu-id="5b24d-112">So the first step is to disassociate both objects.</span></span> <span data-ttu-id="5b24d-113">在這裡，我們會取得與計畫關聯的最新版本的虛擬網路，並且將 **屬性 DdosProtectionPlan** 設定為空白值，而標有 **EnableDdosProtection** (此標號若沒有計劃) 就無法成立。</span><span class="sxs-lookup"><span data-stu-id="5b24d-113">Here, we get the most updated version of the virtual network associated with the plan, and we set the property **DdosProtectionPlan** to an empty value and the flag **EnableDdosProtection** (this flag cannot be true without a plan).</span></span>
<span data-ttu-id="5b24d-114">接著，我們將本地變數放入 **Set-AzVirtualNetwork** 中，以持續新的狀態。</span><span class="sxs-lookup"><span data-stu-id="5b24d-114">Then, we persist the new state by piping the local variable into **Set-AzVirtualNetwork**.</span></span> <span data-ttu-id="5b24d-115">此時，計畫不再與虛擬網路關聯。</span><span class="sxs-lookup"><span data-stu-id="5b24d-115">At this point, the plan is no longer associated with the virtual network.</span></span>
<span data-ttu-id="5b24d-116">如果這是最後一個與計畫相關聯的計畫，可以使用 Remove-AzDdosProtectionPlan 命令移除 DDoS 保護計劃。</span><span class="sxs-lookup"><span data-stu-id="5b24d-116">If this is the last one associated with the plan, we can remove the DDoS protection plan by using the command Remove-AzDdosProtectionPlan.</span></span>

## <span data-ttu-id="5b24d-117">參數</span><span class="sxs-lookup"><span data-stu-id="5b24d-117">PARAMETERS</span></span>

### <span data-ttu-id="5b24d-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5b24d-118">-DefaultProfile</span></span>
<span data-ttu-id="5b24d-119">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="5b24d-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5b24d-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="5b24d-120">-Name</span></span>
<span data-ttu-id="5b24d-121">指定要移除的 DDoS 保護計劃名稱。</span><span class="sxs-lookup"><span data-stu-id="5b24d-121">Specifies the name of the DDoS protection plan to be removed.</span></span>

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

### <span data-ttu-id="5b24d-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5b24d-122">-PassThru</span></span>
<span data-ttu-id="5b24d-123">會返回代表您處理之專案的物件。</span><span class="sxs-lookup"><span data-stu-id="5b24d-123">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="5b24d-124">根據預設，此 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="5b24d-124">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="5b24d-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5b24d-125">-ResourceGroupName</span></span>
<span data-ttu-id="5b24d-126">指定要移除的 DDoS 保護計劃資源群組。</span><span class="sxs-lookup"><span data-stu-id="5b24d-126">Specifies the resource group of the DDoS protection plan to be removed.</span></span>

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

### <span data-ttu-id="5b24d-127">-確認</span><span class="sxs-lookup"><span data-stu-id="5b24d-127">-Confirm</span></span>
<span data-ttu-id="5b24d-128">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="5b24d-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5b24d-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5b24d-129">-WhatIf</span></span>
<span data-ttu-id="5b24d-130">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="5b24d-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5b24d-131">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="5b24d-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5b24d-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5b24d-132">CommonParameters</span></span>
<span data-ttu-id="5b24d-133">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="5b24d-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5b24d-134">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="5b24d-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5b24d-135">輸入</span><span class="sxs-lookup"><span data-stu-id="5b24d-135">INPUTS</span></span>

### <span data-ttu-id="5b24d-136">System.String</span><span class="sxs-lookup"><span data-stu-id="5b24d-136">System.String</span></span>

## <span data-ttu-id="5b24d-137">輸出</span><span class="sxs-lookup"><span data-stu-id="5b24d-137">OUTPUTS</span></span>

### <span data-ttu-id="5b24d-138">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="5b24d-138">System.Boolean</span></span>

## <span data-ttu-id="5b24d-139">筆記</span><span class="sxs-lookup"><span data-stu-id="5b24d-139">NOTES</span></span>

## <span data-ttu-id="5b24d-140">相關連結</span><span class="sxs-lookup"><span data-stu-id="5b24d-140">RELATED LINKS</span></span>

[<span data-ttu-id="5b24d-141">New-AzDdosProtectionPlan</span><span class="sxs-lookup"><span data-stu-id="5b24d-141">New-AzDdosProtectionPlan</span></span>](./New-AzDdosProtectionPlan.md)

[<span data-ttu-id="5b24d-142">Get-AzDdosProtectionPlan</span><span class="sxs-lookup"><span data-stu-id="5b24d-142">Get-AzDdosProtectionPlan</span></span>](./Get-AzDdosProtectionPlan.md)

[<span data-ttu-id="5b24d-143">New-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="5b24d-143">New-AzVirtualNetwork</span></span>](./New-AzVirtualNetwork.md)

[<span data-ttu-id="5b24d-144">Set-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="5b24d-144">Set-AzVirtualNetwork</span></span>](./Set-AzVirtualNetwork.md)

[<span data-ttu-id="5b24d-145">Get-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="5b24d-145">Get-AzVirtualNetwork</span></span>](./Get-AzVirtualNetwork.md)