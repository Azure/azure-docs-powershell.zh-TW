---
external help file: ''
Module Name: Az.DedicatedHsm
online version: https://docs.microsoft.com/powershell/module/az.dedicatedhsm/update-azdedicatedhsm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DedicatedHsm/help/Update-AzDedicatedHsm.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DedicatedHsm/help/Update-AzDedicatedHsm.md
ms.openlocfilehash: ba005802294ef4fa1c890230230cbd44bc783216
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101909109"
---
# <span data-ttu-id="a30dd-101">Update-AzDedicatedHsm</span><span class="sxs-lookup"><span data-stu-id="a30dd-101">Update-AzDedicatedHsm</span></span>

## <span data-ttu-id="a30dd-102">簡介</span><span class="sxs-lookup"><span data-stu-id="a30dd-102">SYNOPSIS</span></span>
<span data-ttu-id="a30dd-103">更新指定訂閱中的專用 HSM。</span><span class="sxs-lookup"><span data-stu-id="a30dd-103">Update a dedicated HSM in the specified subscription.</span></span>

## <span data-ttu-id="a30dd-104">語法</span><span class="sxs-lookup"><span data-stu-id="a30dd-104">SYNTAX</span></span>

### <span data-ttu-id="a30dd-105">UpdateExpanded (預設) </span><span class="sxs-lookup"><span data-stu-id="a30dd-105">UpdateExpanded (Default)</span></span>
```
Update-AzDedicatedHsm -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>] [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="a30dd-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="a30dd-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzDedicatedHsm -InputObject <IDedicatedHsmIdentity> [-Tag <Hashtable>] [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="a30dd-107">描述</span><span class="sxs-lookup"><span data-stu-id="a30dd-107">DESCRIPTION</span></span>
<span data-ttu-id="a30dd-108">更新指定訂閱中的專用 HSM。</span><span class="sxs-lookup"><span data-stu-id="a30dd-108">Update a dedicated HSM in the specified subscription.</span></span>

## <span data-ttu-id="a30dd-109">例子</span><span class="sxs-lookup"><span data-stu-id="a30dd-109">EXAMPLES</span></span>

### <span data-ttu-id="a30dd-110">範例 1：根據名稱更新 Dedicated HSM 的參數標記</span><span class="sxs-lookup"><span data-stu-id="a30dd-110">Example 1: Update the parameter tag of the Dedicated HSM by name</span></span>
```powershell
PS C:\> Update-AzDedicatedHsm -Name  hsm-n7wfxi -ResourceGroupName dedicatedhsm-rg-n359cz -Tag @{'key1' = '1'; 'key2' = 2; 'key3' = 3}

Name       Provisioning State SKU                           Location
----       ------------------ ---                           --------
hsm-n7wfxi Succeeded          SafeNet Luna Network HSM A790 eastus
```

<span data-ttu-id="a30dd-111">此命令會根據名稱更新專用 HSM 的參數標記</span><span class="sxs-lookup"><span data-stu-id="a30dd-111">This command updates the parameter tag of the Dedicated HSM by name</span></span>

### <span data-ttu-id="a30dd-112">範例 2：根據物件更新 Dedicated HSM 的參數標記</span><span class="sxs-lookup"><span data-stu-id="a30dd-112">Example 2: Update the parameter tag of the Dedicated HSM by object</span></span>
```powershell
PS C:\> $hsm = Get-AzDedicatedHsm -Name  hsm-n7wfxi -ResourceGroupName dedicatedhsm-rg-n359cz 
PS C:\> Update-AzDedicatedHsm -InputObject -Tag @{'key1' = '1'; 'key2' = 2; 'key3' = 3}

Name       Provisioning State SKU                           Location
----       ------------------ ---                           --------
hsm-n7wfxi Succeeded          SafeNet Luna Network HSM A790 eastus
```

<span data-ttu-id="a30dd-113">此命令會更新 Dedicated HSM 根據物件的參數標記</span><span class="sxs-lookup"><span data-stu-id="a30dd-113">This command updates the parameter tag of the Dedicated HSM by object</span></span>

## <span data-ttu-id="a30dd-114">參數</span><span class="sxs-lookup"><span data-stu-id="a30dd-114">PARAMETERS</span></span>

### <span data-ttu-id="a30dd-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a30dd-115">-AsJob</span></span>
<span data-ttu-id="a30dd-116">以工作執行命令</span><span class="sxs-lookup"><span data-stu-id="a30dd-116">Run the command as a job</span></span>

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

### <span data-ttu-id="a30dd-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a30dd-117">-DefaultProfile</span></span>
<span data-ttu-id="a30dd-118">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="a30dd-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a30dd-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a30dd-119">-InputObject</span></span>
<span data-ttu-id="a30dd-120">身分識別參數若要建構，請參閱 INPUTOBJECT 屬性的 NOTES 區段，並建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="a30dd-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DedicatedHsm.Models.IDedicatedHsmIdentity
Parameter Sets: UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a30dd-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="a30dd-121">-Name</span></span>
<span data-ttu-id="a30dd-122">專用 HSM 的名稱</span><span class="sxs-lookup"><span data-stu-id="a30dd-122">Name of the dedicated HSM</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a30dd-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="a30dd-123">-NoWait</span></span>
<span data-ttu-id="a30dd-124">非同步執行命令</span><span class="sxs-lookup"><span data-stu-id="a30dd-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="a30dd-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a30dd-125">-ResourceGroupName</span></span>
<span data-ttu-id="a30dd-126">伺服器所屬的資源組名。</span><span class="sxs-lookup"><span data-stu-id="a30dd-126">The name of the Resource Group to which the server belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a30dd-127">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="a30dd-127">-SubscriptionId</span></span>
<span data-ttu-id="a30dd-128">可唯一識別 Microsoft Azure 訂閱的訂閱認證。</span><span class="sxs-lookup"><span data-stu-id="a30dd-128">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="a30dd-129">訂閱識別碼會構成每個服務通話 URI 的一部分。</span><span class="sxs-lookup"><span data-stu-id="a30dd-129">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a30dd-130">-標記</span><span class="sxs-lookup"><span data-stu-id="a30dd-130">-Tag</span></span>
<span data-ttu-id="a30dd-131">資源標記</span><span class="sxs-lookup"><span data-stu-id="a30dd-131">Resource tags</span></span>

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

### <span data-ttu-id="a30dd-132">-確認</span><span class="sxs-lookup"><span data-stu-id="a30dd-132">-Confirm</span></span>
<span data-ttu-id="a30dd-133">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="a30dd-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a30dd-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a30dd-134">-WhatIf</span></span>
<span data-ttu-id="a30dd-135">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="a30dd-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a30dd-136">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="a30dd-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a30dd-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a30dd-137">CommonParameters</span></span>
<span data-ttu-id="a30dd-138">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="a30dd-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a30dd-139">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a30dd-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a30dd-140">輸入</span><span class="sxs-lookup"><span data-stu-id="a30dd-140">INPUTS</span></span>

### <span data-ttu-id="a30dd-141">Microsoft.Azure.PowerShell.Cmdlets.DedicatedVtm.models.IDedicatedSoftmIdentity</span><span class="sxs-lookup"><span data-stu-id="a30dd-141">Microsoft.Azure.PowerShell.Cmdlets.DedicatedHsm.Models.IDedicatedHsmIdentity</span></span>

## <span data-ttu-id="a30dd-142">輸出</span><span class="sxs-lookup"><span data-stu-id="a30dd-142">OUTPUTS</span></span>

### <span data-ttu-id="a30dd-143">Microsoft.Azure.PowerShell.Cmdlets.DedicatedVtm.models.Api20181031.IDedicatedSoftm</span><span class="sxs-lookup"><span data-stu-id="a30dd-143">Microsoft.Azure.PowerShell.Cmdlets.DedicatedHsm.Models.Api20181031.IDedicatedHsm</span></span>

## <span data-ttu-id="a30dd-144">筆記</span><span class="sxs-lookup"><span data-stu-id="a30dd-144">NOTES</span></span>

<span data-ttu-id="a30dd-145">別名</span><span class="sxs-lookup"><span data-stu-id="a30dd-145">ALIASES</span></span>

<span data-ttu-id="a30dd-146">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="a30dd-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="a30dd-147">若要建立下列描述的參數，請建構包含適當屬性的雜湊表。</span><span class="sxs-lookup"><span data-stu-id="a30dd-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="a30dd-148">有關雜湊表的資訊，請執行Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="a30dd-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="a30dd-149">INPUTOBJECT： <IDedicatedHsmIdentity> 身分識別參數</span><span class="sxs-lookup"><span data-stu-id="a30dd-149">INPUTOBJECT <IDedicatedHsmIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="a30dd-150">`[Id <String>]`：資源識別路徑</span><span class="sxs-lookup"><span data-stu-id="a30dd-150">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="a30dd-151">`[Name <String>]`：專用 Hsm 的名稱</span><span class="sxs-lookup"><span data-stu-id="a30dd-151">`[Name <String>]`: Name of the dedicated Hsm</span></span>
  - <span data-ttu-id="a30dd-152">`[ResourceGroupName <String>]`：資源所屬的資源組名。</span><span class="sxs-lookup"><span data-stu-id="a30dd-152">`[ResourceGroupName <String>]`: The name of the Resource Group to which the resource belongs.</span></span>
  - <span data-ttu-id="a30dd-153">`[SubscriptionId <String>]`：可唯一識別 Microsoft Azure 訂閱的訂閱認證。</span><span class="sxs-lookup"><span data-stu-id="a30dd-153">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="a30dd-154">訂閱識別碼會構成每個服務通話 URI 的一部分。</span><span class="sxs-lookup"><span data-stu-id="a30dd-154">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="a30dd-155">相關連結</span><span class="sxs-lookup"><span data-stu-id="a30dd-155">RELATED LINKS</span></span>

