---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azuredosprotectionplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmDdosProtectionPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmDdosProtectionPlan.md
ms.openlocfilehash: 87110fe779e128e8ef5d5d6de0504ec9fdca1b25
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93456959"
---
# <span data-ttu-id="57508-101">Remove-AzureRmDdosProtectionPlan</span><span class="sxs-lookup"><span data-stu-id="57508-101">Remove-AzureRmDdosProtectionPlan</span></span>

## <span data-ttu-id="57508-102">摘要</span><span class="sxs-lookup"><span data-stu-id="57508-102">SYNOPSIS</span></span>
<span data-ttu-id="57508-103">移除 DDoS 保護方案。</span><span class="sxs-lookup"><span data-stu-id="57508-103">Removes a DDoS protection plan.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="57508-104">句法</span><span class="sxs-lookup"><span data-stu-id="57508-104">SYNTAX</span></span>

```
Remove-AzureRmDdosProtectionPlan -ResourceGroupName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="57508-105">說明</span><span class="sxs-lookup"><span data-stu-id="57508-105">DESCRIPTION</span></span>
<span data-ttu-id="57508-106">Remove-AzureRmDdosProtectionPlan Cmdlet 會移除 DDoS 保護方案。</span><span class="sxs-lookup"><span data-stu-id="57508-106">The Remove-AzureRmDdosProtectionPlan cmdlet removes a DDoS protection plan.</span></span>

## <span data-ttu-id="57508-107">示例</span><span class="sxs-lookup"><span data-stu-id="57508-107">EXAMPLES</span></span>

### <span data-ttu-id="57508-108">範例1：移除空白的 DDoS 保護方案</span><span class="sxs-lookup"><span data-stu-id="57508-108">Example 1: Remove an empty DDoS protection plan</span></span>
```
D:\> Remove-AzureRmDdosProtectionPlan -ResourceGroupName ResourceGroupName -Name DdosProtectionPlan
```

<span data-ttu-id="57508-109">在這種情況下，我們會根據指定移除 DDoS 保護方案。</span><span class="sxs-lookup"><span data-stu-id="57508-109">In this case, we remove a DDoS protection plan as specified.</span></span>

### <span data-ttu-id="57508-110">範例2：移除與虛擬網路相關聯的 DDoS 保護方案</span><span class="sxs-lookup"><span data-stu-id="57508-110">Example 2: Remove a DDoS protection plan associated with a virtual network</span></span>
```
D:\> $vnet = Get-AzureRmVirtualNetwork -Name VnetName -ResourceGroupName ResourceGroupName
D:\> $vnet.DdosProtectionPlan = $null
D:\> $vnet.EnableDdosProtection = $false
D:\> $vnet | Set-AzureRmVirtualNetwork


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


D:\> Remove-AzureRmDdosProtectionPlan -ResourceGroupName ResourceGroupName -Name DdosProtectionPlan
```

<span data-ttu-id="57508-111">如果 DDoS 保護方案與虛擬網路相關聯，則無法刪除。</span><span class="sxs-lookup"><span data-stu-id="57508-111">DDoS protection plans cannot be deleted if they are associated with a virtual network.</span></span> <span data-ttu-id="57508-112">因此，第一個步驟是解除關聯兩個物件。</span><span class="sxs-lookup"><span data-stu-id="57508-112">So the first step is to disassociate both objects.</span></span> <span data-ttu-id="57508-113">在這裡，我們會取得與方案相關聯之最新的虛擬網路版本，並將屬性 **DdosProtectionPlan** 設為空白值，並將 [旗標] **EnableDdosProtection** (此標誌不能為 true，而不需要方案) 。</span><span class="sxs-lookup"><span data-stu-id="57508-113">Here, we get the most updated version of the virtual network associated with the plan, and we set the property **DdosProtectionPlan** to an empty value and the flag **EnableDdosProtection** (this flag cannot be true without a plan).</span></span>
<span data-ttu-id="57508-114">接著，我們會將本機變數組成 **AzureRmVirtualNetwork** ，以保留新的狀態。</span><span class="sxs-lookup"><span data-stu-id="57508-114">Then, we persist the new state by piping the local variable into **Set-AzureRmVirtualNetwork**.</span></span> <span data-ttu-id="57508-115">此時，該計畫已不再與虛擬網路建立關聯。</span><span class="sxs-lookup"><span data-stu-id="57508-115">At this point, the plan is no longer associated with the virtual network.</span></span>
<span data-ttu-id="57508-116">如果這是與計畫相關的最後一個專案，我們可以使用命令移除 AzureRmDdosProtectionPlan 來移除 DDoS 保護方案。</span><span class="sxs-lookup"><span data-stu-id="57508-116">If this is the last one associated with the plan, we can remove the DDoS protection plan by using the command Remove-AzureRmDdosProtectionPlan.</span></span>

## <span data-ttu-id="57508-117">參數</span><span class="sxs-lookup"><span data-stu-id="57508-117">PARAMETERS</span></span>

### <span data-ttu-id="57508-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="57508-118">-DefaultProfile</span></span>
<span data-ttu-id="57508-119">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="57508-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="57508-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="57508-120">-Name</span></span>
<span data-ttu-id="57508-121">指定要移除的 DDoS 保護方案名稱。</span><span class="sxs-lookup"><span data-stu-id="57508-121">Specifies the name of the DDoS protection plan to be removed.</span></span>

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

### <span data-ttu-id="57508-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="57508-122">-PassThru</span></span>
<span data-ttu-id="57508-123">傳回代表您正在使用之專案的物件。</span><span class="sxs-lookup"><span data-stu-id="57508-123">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="57508-124">根據預設，這個 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="57508-124">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="57508-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="57508-125">-ResourceGroupName</span></span>
<span data-ttu-id="57508-126">指定要移除之 DDoS 保護方案的 [資源] 群組。</span><span class="sxs-lookup"><span data-stu-id="57508-126">Specifies the resource group of the DDoS protection plan to be removed.</span></span>

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

### <span data-ttu-id="57508-127">-確認</span><span class="sxs-lookup"><span data-stu-id="57508-127">-Confirm</span></span>
<span data-ttu-id="57508-128">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="57508-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="57508-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="57508-129">-WhatIf</span></span>
<span data-ttu-id="57508-130">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="57508-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="57508-131">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="57508-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="57508-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="57508-132">CommonParameters</span></span>
<span data-ttu-id="57508-133">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="57508-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="57508-134">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="57508-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="57508-135">輸入</span><span class="sxs-lookup"><span data-stu-id="57508-135">INPUTS</span></span>

### <span data-ttu-id="57508-136">System.object</span><span class="sxs-lookup"><span data-stu-id="57508-136">System.String</span></span>

## <span data-ttu-id="57508-137">輸出</span><span class="sxs-lookup"><span data-stu-id="57508-137">OUTPUTS</span></span>

### <span data-ttu-id="57508-138">System.object</span><span class="sxs-lookup"><span data-stu-id="57508-138">System.Boolean</span></span>

## <span data-ttu-id="57508-139">筆記</span><span class="sxs-lookup"><span data-stu-id="57508-139">NOTES</span></span>

## <span data-ttu-id="57508-140">相關連結</span><span class="sxs-lookup"><span data-stu-id="57508-140">RELATED LINKS</span></span>

[<span data-ttu-id="57508-141">新-AzureRmDdosProtectionPlan</span><span class="sxs-lookup"><span data-stu-id="57508-141">New-AzureRmDdosProtectionPlan</span></span>](./New-AzureRmDdosProtectionPlan.md)

[<span data-ttu-id="57508-142">AzureRmDdosProtectionPlan</span><span class="sxs-lookup"><span data-stu-id="57508-142">Get-AzureRmDdosProtectionPlan</span></span>](./Get-AzureRmDdosProtectionPlan.md)

[<span data-ttu-id="57508-143">新-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="57508-143">New-AzureRmVirtualNetwork</span></span>](./New-AzureRmVirtualNetwork.md)

[<span data-ttu-id="57508-144">Set-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="57508-144">Set-AzureRmVirtualNetwork</span></span>](./Set-AzureRmVirtualNetwork.md)

[<span data-ttu-id="57508-145">AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="57508-145">Get-AzureRmVirtualNetwork</span></span>](./Get-AzureRmVirtualNetwork.md)
