---
external help file: ''
Module Name: Az.DedicatedHsm
online version: https://docs.microsoft.com/en-us/powershell/module/az.dedicatedhsm/new-azdedicatedhsm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DedicatedHsm/help/New-AzDedicatedHsm.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DedicatedHsm/help/New-AzDedicatedHsm.md
ms.openlocfilehash: ff1fc53d7fec9a56564bbf536469ea9f745f9265
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94128216"
---
# <span data-ttu-id="6a446-101">New-AzDedicatedHsm</span><span class="sxs-lookup"><span data-stu-id="6a446-101">New-AzDedicatedHsm</span></span>

## <span data-ttu-id="6a446-102">摘要</span><span class="sxs-lookup"><span data-stu-id="6a446-102">SYNOPSIS</span></span>
<span data-ttu-id="6a446-103">在指定的訂閱中建立或更新專用的 HSM。</span><span class="sxs-lookup"><span data-stu-id="6a446-103">Create or Update a dedicated HSM in the specified subscription.</span></span>

## <span data-ttu-id="6a446-104">句法</span><span class="sxs-lookup"><span data-stu-id="6a446-104">SYNTAX</span></span>

```
New-AzDedicatedHsm -Name <String> -ResourceGroupName <String> -Location <String> [-SubscriptionId <String>]
 [-NetworkInterface <INetworkInterface[]>] [-Sku <String>] [-StampId <String>] [-SubnetId <String>]
 [-Tag <Hashtable>] [-Zone <String[]>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="6a446-105">說明</span><span class="sxs-lookup"><span data-stu-id="6a446-105">DESCRIPTION</span></span>
<span data-ttu-id="6a446-106">在指定的訂閱中建立或更新專用的 HSM。</span><span class="sxs-lookup"><span data-stu-id="6a446-106">Create or Update a dedicated HSM in the specified subscription.</span></span>

## <span data-ttu-id="6a446-107">示例</span><span class="sxs-lookup"><span data-stu-id="6a446-107">EXAMPLES</span></span>

### <span data-ttu-id="6a446-108">範例1：在現有的虛擬網路中建立專用的 HSM</span><span class="sxs-lookup"><span data-stu-id="6a446-108">Example 1: Create a Dedicated HSM into an existing virtual network</span></span>
```powershell
PS C:\> New-AzDedicatedHsm -Name  hsm-n7wfxi -ResourceGroupName dedicatedhsm-rg-n359cz -Location eastus -Sku "SafeNet Luna Network HSM A790" -StampId stamp1 -SubnetId "/subscriptions/xxxx-xxxx-xxx-xxx/resourceGroups/dedicatedhsm-rg-n359cz/providers/Microsoft.Network/virtualNetworks/vnetq30la9/subnets/hsmsubnet" -NetworkInterface @{PrivateIPAddress = '10.2.1.120' }

Name       Provisioning State SKU                           Location
----       ------------------ ---                           --------
hsm-n7wfxi Succeeded          SafeNet Luna Network HSM A790 eastus
```

<span data-ttu-id="6a446-109">這個命令會在現有的虛擬網路中建立一個專用的 HSM。</span><span class="sxs-lookup"><span data-stu-id="6a446-109">This command creates a Dedicated HSM into an existing virtual network.</span></span>

<span data-ttu-id="6a446-110">**注意：** 在 `New-AzDedicatedHsm` Azure 上完全預配 HSM 之前，目前有一個限制會傳回它。</span><span class="sxs-lookup"><span data-stu-id="6a446-110">**NOTE:** Currently `New-AzDedicatedHsm` has a limitation that it returns before the HSM is fully provisioned on Azure.</span></span>
<span data-ttu-id="6a446-111">因此，在建立新的 HSM 之後，請查詢其狀態， `Get-AzDedicatedHsm` 並確認它在 `Provisioning State` `Succeeded` 使用之前。</span><span class="sxs-lookup"><span data-stu-id="6a446-111">Therefore after creating a new HSM, please query its state by `Get-AzDedicatedHsm` and make sure its `Provisioning State` is `Succeeded` before using it.</span></span>

## <span data-ttu-id="6a446-112">參數</span><span class="sxs-lookup"><span data-stu-id="6a446-112">PARAMETERS</span></span>

### <span data-ttu-id="6a446-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6a446-113">-AsJob</span></span>
<span data-ttu-id="6a446-114">執行命令做為工作</span><span class="sxs-lookup"><span data-stu-id="6a446-114">Run the command as a job</span></span>

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

### <span data-ttu-id="6a446-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6a446-115">-DefaultProfile</span></span>
<span data-ttu-id="6a446-116">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="6a446-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6a446-117">-位置</span><span class="sxs-lookup"><span data-stu-id="6a446-117">-Location</span></span>
<span data-ttu-id="6a446-118">您應在其中建立專用 HSM 的支援的 Azure 位置。</span><span class="sxs-lookup"><span data-stu-id="6a446-118">The supported Azure location where the dedicated HSM should be created.</span></span>

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

### <span data-ttu-id="6a446-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="6a446-119">-Name</span></span>
<span data-ttu-id="6a446-120">專用 Hsm 的名稱</span><span class="sxs-lookup"><span data-stu-id="6a446-120">Name of the dedicated Hsm</span></span>

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

### <span data-ttu-id="6a446-121">-NetworkInterface</span><span class="sxs-lookup"><span data-stu-id="6a446-121">-NetworkInterface</span></span>
<span data-ttu-id="6a446-122">指定與專用 HSM 相關聯之網路介面的資源識別碼清單。</span><span class="sxs-lookup"><span data-stu-id="6a446-122">Specifies the list of resource Ids for the network interfaces associated with the dedicated HSM.</span></span>
<span data-ttu-id="6a446-123">若要建立，請參閱 NETWORKINTERFACE 屬性和建立雜湊資料表的備忘稿區段。</span><span class="sxs-lookup"><span data-stu-id="6a446-123">To construct, see NOTES section for NETWORKINTERFACE properties and create a hash table.</span></span>

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

### <span data-ttu-id="6a446-124">-NoWait</span><span class="sxs-lookup"><span data-stu-id="6a446-124">-NoWait</span></span>
<span data-ttu-id="6a446-125">以非同步方式執行命令</span><span class="sxs-lookup"><span data-stu-id="6a446-125">Run the command asynchronously</span></span>

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

### <span data-ttu-id="6a446-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6a446-126">-ResourceGroupName</span></span>
<span data-ttu-id="6a446-127">資源所屬之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="6a446-127">The name of the Resource Group to which the resource belongs.</span></span>

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

### <span data-ttu-id="6a446-128">-Sku</span><span class="sxs-lookup"><span data-stu-id="6a446-128">-Sku</span></span>
<span data-ttu-id="6a446-129">專用 HSM 的 SKU</span><span class="sxs-lookup"><span data-stu-id="6a446-129">SKU of the dedicated HSM</span></span>

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

### <span data-ttu-id="6a446-130">-StampId</span><span class="sxs-lookup"><span data-stu-id="6a446-130">-StampId</span></span>
<span data-ttu-id="6a446-131">當 RP 不支援可用性區域時，將會使用此欄位。</span><span class="sxs-lookup"><span data-stu-id="6a446-131">This field will be used when RP does not support Availability zones.</span></span>

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

### <span data-ttu-id="6a446-132">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="6a446-132">-SubnetId</span></span>
<span data-ttu-id="6a446-133">/Subscriptions/{SubscriptionId}/resourceGroups/{ResourceGroupName}/... 形式的 ARM 資源識別碼</span><span class="sxs-lookup"><span data-stu-id="6a446-133">The ARM resource id in the form of /subscriptions/{SubscriptionId}/resourceGroups/{ResourceGroupName}/...</span></span>

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

### <span data-ttu-id="6a446-134">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="6a446-134">-SubscriptionId</span></span>
<span data-ttu-id="6a446-135">可唯一識別 Microsoft Azure 訂閱的訂閱認證。</span><span class="sxs-lookup"><span data-stu-id="6a446-135">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="6a446-136">[訂閱識別碼] 會在每個服務呼叫的 URI 中形成一部分。</span><span class="sxs-lookup"><span data-stu-id="6a446-136">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="6a446-137">-Tag</span><span class="sxs-lookup"><span data-stu-id="6a446-137">-Tag</span></span>
<span data-ttu-id="6a446-138">資源標記</span><span class="sxs-lookup"><span data-stu-id="6a446-138">Resource tags</span></span>

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

### <span data-ttu-id="6a446-139">-Zone</span><span class="sxs-lookup"><span data-stu-id="6a446-139">-Zone</span></span>
<span data-ttu-id="6a446-140">專用的 Hsm 區域。</span><span class="sxs-lookup"><span data-stu-id="6a446-140">The Dedicated Hsm zones.</span></span>

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

### <span data-ttu-id="6a446-141">-確認</span><span class="sxs-lookup"><span data-stu-id="6a446-141">-Confirm</span></span>
<span data-ttu-id="6a446-142">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="6a446-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6a446-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6a446-143">-WhatIf</span></span>
<span data-ttu-id="6a446-144">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="6a446-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6a446-145">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="6a446-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6a446-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6a446-146">CommonParameters</span></span>
<span data-ttu-id="6a446-147">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="6a446-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6a446-148">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="6a446-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6a446-149">輸入</span><span class="sxs-lookup"><span data-stu-id="6a446-149">INPUTS</span></span>

## <span data-ttu-id="6a446-150">輸出</span><span class="sxs-lookup"><span data-stu-id="6a446-150">OUTPUTS</span></span>

### <span data-ttu-id="6a446-151">IDedicatedHsm （DedicatedHsm）。 Api20181031。</span><span class="sxs-lookup"><span data-stu-id="6a446-151">Microsoft.Azure.PowerShell.Cmdlets.DedicatedHsm.Models.Api20181031.IDedicatedHsm</span></span>

## <span data-ttu-id="6a446-152">筆記</span><span class="sxs-lookup"><span data-stu-id="6a446-152">NOTES</span></span>

<span data-ttu-id="6a446-153">別名</span><span class="sxs-lookup"><span data-stu-id="6a446-153">ALIASES</span></span>

<span data-ttu-id="6a446-154">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="6a446-154">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="6a446-155">若要建立如下所述的參數，請構造包含適當屬性的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="6a446-155">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="6a446-156">如需雜湊資料表的詳細資訊，請執行 Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="6a446-156">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="6a446-157">NETWORKINTERFACE <INetworkInterface [] >：指定與專用 HSM 相關聯之網路介面的資源識別碼清單。</span><span class="sxs-lookup"><span data-stu-id="6a446-157">NETWORKINTERFACE <INetworkInterface[]>: Specifies the list of resource Ids for the network interfaces associated with the dedicated HSM.</span></span>
  - <span data-ttu-id="6a446-158">`[PrivateIPAddress <String>]`：介面的專用 Ip 位址</span><span class="sxs-lookup"><span data-stu-id="6a446-158">`[PrivateIPAddress <String>]`: Private Ip address of the interface</span></span>

## <span data-ttu-id="6a446-159">相關連結</span><span class="sxs-lookup"><span data-stu-id="6a446-159">RELATED LINKS</span></span>

