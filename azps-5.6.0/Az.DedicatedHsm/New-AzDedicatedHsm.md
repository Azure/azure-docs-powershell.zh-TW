---
external help file: ''
Module Name: Az.DedicatedHsm
online version: https://docs.microsoft.com/powershell/module/az.dedicatedhsm/new-azdedicatedhsm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DedicatedHsm/help/New-AzDedicatedHsm.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DedicatedHsm/help/New-AzDedicatedHsm.md
ms.openlocfilehash: 9d2d1ee1dd17b9d1783ba267b2f656be6adce05b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101905517"
---
# <span data-ttu-id="770b8-101">New-AzDedicatedHsm</span><span class="sxs-lookup"><span data-stu-id="770b8-101">New-AzDedicatedHsm</span></span>

## <span data-ttu-id="770b8-102">簡介</span><span class="sxs-lookup"><span data-stu-id="770b8-102">SYNOPSIS</span></span>
<span data-ttu-id="770b8-103">在指定的訂閱中建立或更新專用 HSM。</span><span class="sxs-lookup"><span data-stu-id="770b8-103">Create or Update a dedicated HSM in the specified subscription.</span></span>

## <span data-ttu-id="770b8-104">語法</span><span class="sxs-lookup"><span data-stu-id="770b8-104">SYNTAX</span></span>

```
New-AzDedicatedHsm -Name <String> -ResourceGroupName <String> -Location <String> [-SubscriptionId <String>]
 [-NetworkInterface <INetworkInterface[]>] [-Sku <String>] [-StampId <String>] [-SubnetId <String>]
 [-Tag <Hashtable>] [-Zone <String[]>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="770b8-105">描述</span><span class="sxs-lookup"><span data-stu-id="770b8-105">DESCRIPTION</span></span>
<span data-ttu-id="770b8-106">在指定的訂閱中建立或更新專用 HSM。</span><span class="sxs-lookup"><span data-stu-id="770b8-106">Create or Update a dedicated HSM in the specified subscription.</span></span>

## <span data-ttu-id="770b8-107">例子</span><span class="sxs-lookup"><span data-stu-id="770b8-107">EXAMPLES</span></span>

### <span data-ttu-id="770b8-108">範例 1：在現有的虛擬網路中建立專用 HSM</span><span class="sxs-lookup"><span data-stu-id="770b8-108">Example 1: Create a Dedicated HSM into an existing virtual network</span></span>
```powershell
PS C:\> New-AzDedicatedHsm -Name  hsm-n7wfxi -ResourceGroupName dedicatedhsm-rg-n359cz -Location eastus -Sku "SafeNet Luna Network HSM A790" -StampId stamp1 -SubnetId "/subscriptions/xxxx-xxxx-xxx-xxx/resourceGroups/dedicatedhsm-rg-n359cz/providers/Microsoft.Network/virtualNetworks/vnetq30la9/subnets/hsmsubnet" -NetworkInterface @{PrivateIPAddress = '10.2.1.120' }

Name       Provisioning State SKU                           Location
----       ------------------ ---                           --------
hsm-n7wfxi Succeeded          SafeNet Luna Network HSM A790 eastus
```

<span data-ttu-id="770b8-109">此命令會建立專用 HSM 至現有的虛擬網路。</span><span class="sxs-lookup"><span data-stu-id="770b8-109">This command creates a Dedicated HSM into an existing virtual network.</span></span>

<span data-ttu-id="770b8-110">**注意：** HSM 在 Azure 上完整設置之前，目前會 `New-AzDedicatedHsm` 先返回限制。</span><span class="sxs-lookup"><span data-stu-id="770b8-110">**NOTE:** Currently `New-AzDedicatedHsm` has a limitation that it returns before the HSM is fully provisioned on Azure.</span></span>
<span data-ttu-id="770b8-111">因此，建立新 HSM 之後，請先查詢其狀態， `Get-AzDedicatedHsm` 確認其 `Provisioning State` 狀態後 `Succeeded` 再使用它。</span><span class="sxs-lookup"><span data-stu-id="770b8-111">Therefore after creating a new HSM, please query its state by `Get-AzDedicatedHsm` and make sure its `Provisioning State` is `Succeeded` before using it.</span></span>

## <span data-ttu-id="770b8-112">參數</span><span class="sxs-lookup"><span data-stu-id="770b8-112">PARAMETERS</span></span>

### <span data-ttu-id="770b8-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="770b8-113">-AsJob</span></span>
<span data-ttu-id="770b8-114">以工作執行命令</span><span class="sxs-lookup"><span data-stu-id="770b8-114">Run the command as a job</span></span>

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

### <span data-ttu-id="770b8-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="770b8-115">-DefaultProfile</span></span>
<span data-ttu-id="770b8-116">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="770b8-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="770b8-117">-位置</span><span class="sxs-lookup"><span data-stu-id="770b8-117">-Location</span></span>
<span data-ttu-id="770b8-118">應建立專用 HSM 的支援 Azure 位置。</span><span class="sxs-lookup"><span data-stu-id="770b8-118">The supported Azure location where the dedicated HSM should be created.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="770b8-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="770b8-119">-Name</span></span>
<span data-ttu-id="770b8-120">專用 Hsm 的名稱</span><span class="sxs-lookup"><span data-stu-id="770b8-120">Name of the dedicated Hsm</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="770b8-121">-NetworkInterface</span><span class="sxs-lookup"><span data-stu-id="770b8-121">-NetworkInterface</span></span>
<span data-ttu-id="770b8-122">指定與專用 HSM 相關聯的網路介面之資源識別碼清單。</span><span class="sxs-lookup"><span data-stu-id="770b8-122">Specifies the list of resource Ids for the network interfaces associated with the dedicated HSM.</span></span>
<span data-ttu-id="770b8-123">若要建構，請參閱 NETWORKINTERFACE 屬性的附注區段，並建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="770b8-123">To construct, see NOTES section for NETWORKINTERFACE properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DedicatedHsm.Models.Api20181031.INetworkInterface[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="770b8-124">-NoWait</span><span class="sxs-lookup"><span data-stu-id="770b8-124">-NoWait</span></span>
<span data-ttu-id="770b8-125">非同步執行命令</span><span class="sxs-lookup"><span data-stu-id="770b8-125">Run the command asynchronously</span></span>

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

### <span data-ttu-id="770b8-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="770b8-126">-ResourceGroupName</span></span>
<span data-ttu-id="770b8-127">資源所屬的資源組名。</span><span class="sxs-lookup"><span data-stu-id="770b8-127">The name of the Resource Group to which the resource belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="770b8-128">-SKU</span><span class="sxs-lookup"><span data-stu-id="770b8-128">-Sku</span></span>
<span data-ttu-id="770b8-129">專用 HSM 的 SKU</span><span class="sxs-lookup"><span data-stu-id="770b8-129">SKU of the dedicated HSM</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="770b8-130">-StampId</span><span class="sxs-lookup"><span data-stu-id="770b8-130">-StampId</span></span>
<span data-ttu-id="770b8-131">如果 RP 不支援可用性區域，就會使用此欄位。</span><span class="sxs-lookup"><span data-stu-id="770b8-131">This field will be used when RP does not support Availability zones.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="770b8-132">-子網Id</span><span class="sxs-lookup"><span data-stu-id="770b8-132">-SubnetId</span></span>
<span data-ttu-id="770b8-133">/subscriptions/{SubscriptionId}/resourceGroups/{ResourceGroupName}/...</span><span class="sxs-lookup"><span data-stu-id="770b8-133">The ARM resource id in the form of /subscriptions/{SubscriptionId}/resourceGroups/{ResourceGroupName}/...</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="770b8-134">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="770b8-134">-SubscriptionId</span></span>
<span data-ttu-id="770b8-135">可唯一識別 Microsoft Azure 訂閱的訂閱認證。</span><span class="sxs-lookup"><span data-stu-id="770b8-135">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="770b8-136">訂閱識別碼會構成每個服務通話 URI 的一部分。</span><span class="sxs-lookup"><span data-stu-id="770b8-136">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="770b8-137">-標記</span><span class="sxs-lookup"><span data-stu-id="770b8-137">-Tag</span></span>
<span data-ttu-id="770b8-138">資源標記</span><span class="sxs-lookup"><span data-stu-id="770b8-138">Resource tags</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="770b8-139">-區域</span><span class="sxs-lookup"><span data-stu-id="770b8-139">-Zone</span></span>
<span data-ttu-id="770b8-140">專用 Hsm 區域。</span><span class="sxs-lookup"><span data-stu-id="770b8-140">The Dedicated Hsm zones.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="770b8-141">-確認</span><span class="sxs-lookup"><span data-stu-id="770b8-141">-Confirm</span></span>
<span data-ttu-id="770b8-142">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="770b8-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="770b8-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="770b8-143">-WhatIf</span></span>
<span data-ttu-id="770b8-144">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="770b8-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="770b8-145">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="770b8-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="770b8-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="770b8-146">CommonParameters</span></span>
<span data-ttu-id="770b8-147">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="770b8-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="770b8-148">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="770b8-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="770b8-149">輸入</span><span class="sxs-lookup"><span data-stu-id="770b8-149">INPUTS</span></span>

## <span data-ttu-id="770b8-150">輸出</span><span class="sxs-lookup"><span data-stu-id="770b8-150">OUTPUTS</span></span>

### <span data-ttu-id="770b8-151">Microsoft.Azure.PowerShell.Cmdlets.DedicatedVtm.models.Api20181031.IDedicatedSoftm</span><span class="sxs-lookup"><span data-stu-id="770b8-151">Microsoft.Azure.PowerShell.Cmdlets.DedicatedHsm.Models.Api20181031.IDedicatedHsm</span></span>

## <span data-ttu-id="770b8-152">筆記</span><span class="sxs-lookup"><span data-stu-id="770b8-152">NOTES</span></span>

<span data-ttu-id="770b8-153">別名</span><span class="sxs-lookup"><span data-stu-id="770b8-153">ALIASES</span></span>

<span data-ttu-id="770b8-154">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="770b8-154">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="770b8-155">若要建立下列描述的參數，請建構包含適當屬性的雜湊表。</span><span class="sxs-lookup"><span data-stu-id="770b8-155">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="770b8-156">有關雜湊表的資訊，請執行Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="770b8-156">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="770b8-157">NETWORKINTERFACE <INetworkInterface[]>：指定與專用 HSM 相關聯的網路介面資源識別碼清單。</span><span class="sxs-lookup"><span data-stu-id="770b8-157">NETWORKINTERFACE <INetworkInterface[]>: Specifies the list of resource Ids for the network interfaces associated with the dedicated HSM.</span></span>
  - <span data-ttu-id="770b8-158">`[PrivateIPAddress <String>]`：介面的專用 Ip 位址</span><span class="sxs-lookup"><span data-stu-id="770b8-158">`[PrivateIPAddress <String>]`: Private Ip address of the interface</span></span>

## <span data-ttu-id="770b8-159">相關連結</span><span class="sxs-lookup"><span data-stu-id="770b8-159">RELATED LINKS</span></span>

