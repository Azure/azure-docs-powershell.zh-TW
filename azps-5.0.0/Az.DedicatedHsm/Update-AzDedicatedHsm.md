---
external help file: ''
Module Name: Az.DedicatedHsm
online version: https://docs.microsoft.com/en-us/powershell/module/az.dedicatedhsm/update-azdedicatedhsm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DedicatedHsm/help/Update-AzDedicatedHsm.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DedicatedHsm/help/Update-AzDedicatedHsm.md
ms.openlocfilehash: 5aa286eeedb08e6f582210d98a1d29bcd0074031
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94284826"
---
# <span data-ttu-id="a61b6-101">Update-AzDedicatedHsm</span><span class="sxs-lookup"><span data-stu-id="a61b6-101">Update-AzDedicatedHsm</span></span>

## <span data-ttu-id="a61b6-102">摘要</span><span class="sxs-lookup"><span data-stu-id="a61b6-102">SYNOPSIS</span></span>
<span data-ttu-id="a61b6-103">在指定的訂閱中更新專用的 HSM。</span><span class="sxs-lookup"><span data-stu-id="a61b6-103">Update a dedicated HSM in the specified subscription.</span></span>

## <span data-ttu-id="a61b6-104">句法</span><span class="sxs-lookup"><span data-stu-id="a61b6-104">SYNTAX</span></span>

### <span data-ttu-id="a61b6-105">UpdateExpanded (預設) </span><span class="sxs-lookup"><span data-stu-id="a61b6-105">UpdateExpanded (Default)</span></span>
```
Update-AzDedicatedHsm -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>] [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="a61b6-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="a61b6-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzDedicatedHsm -InputObject <IDedicatedHsmIdentity> [-Tag <Hashtable>] [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="a61b6-107">說明</span><span class="sxs-lookup"><span data-stu-id="a61b6-107">DESCRIPTION</span></span>
<span data-ttu-id="a61b6-108">在指定的訂閱中更新專用的 HSM。</span><span class="sxs-lookup"><span data-stu-id="a61b6-108">Update a dedicated HSM in the specified subscription.</span></span>

## <span data-ttu-id="a61b6-109">示例</span><span class="sxs-lookup"><span data-stu-id="a61b6-109">EXAMPLES</span></span>

### <span data-ttu-id="a61b6-110">範例1：依名稱更新專用 HSM 的參數標記</span><span class="sxs-lookup"><span data-stu-id="a61b6-110">Example 1: Update the parameter tag of the Dedicated HSM by name</span></span>
```powershell
PS C:\> Update-AzDedicatedHsm -Name  hsm-n7wfxi -ResourceGroupName dedicatedhsm-rg-n359cz -Tag @{'key1' = '1'; 'key2' = 2; 'key3' = 3}

Name       Provisioning State SKU                           Location
----       ------------------ ---                           --------
hsm-n7wfxi Succeeded          SafeNet Luna Network HSM A790 eastus
```

<span data-ttu-id="a61b6-111">這個命令會依名稱更新專用 HSM 的參數標記</span><span class="sxs-lookup"><span data-stu-id="a61b6-111">This command updates the parameter tag of the Dedicated HSM by name</span></span>

### <span data-ttu-id="a61b6-112">範例2：依物件更新專用 HSM 的參數標記</span><span class="sxs-lookup"><span data-stu-id="a61b6-112">Example 2: Update the parameter tag of the Dedicated HSM by object</span></span>
```powershell
PS C:\> $hsm = Get-AzDedicatedHsm -Name  hsm-n7wfxi -ResourceGroupName dedicatedhsm-rg-n359cz 
PS C:\> Update-AzDedicatedHsm -InputObject -Tag @{'key1' = '1'; 'key2' = 2; 'key3' = 3}

Name       Provisioning State SKU                           Location
----       ------------------ ---                           --------
hsm-n7wfxi Succeeded          SafeNet Luna Network HSM A790 eastus
```

<span data-ttu-id="a61b6-113">這個命令會依物件更新專用 HSM 的參數標記</span><span class="sxs-lookup"><span data-stu-id="a61b6-113">This command updates the parameter tag of the Dedicated HSM by object</span></span>

## <span data-ttu-id="a61b6-114">參數</span><span class="sxs-lookup"><span data-stu-id="a61b6-114">PARAMETERS</span></span>

### <span data-ttu-id="a61b6-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a61b6-115">-AsJob</span></span>
<span data-ttu-id="a61b6-116">執行命令做為工作</span><span class="sxs-lookup"><span data-stu-id="a61b6-116">Run the command as a job</span></span>

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

### <span data-ttu-id="a61b6-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a61b6-117">-DefaultProfile</span></span>
<span data-ttu-id="a61b6-118">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="a61b6-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a61b6-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a61b6-119">-InputObject</span></span>
<span data-ttu-id="a61b6-120">要構造的身分識別參數，請參閱 INPUTOBJECT 屬性的 [記事] 區段，然後建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="a61b6-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="a61b6-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="a61b6-121">-Name</span></span>
<span data-ttu-id="a61b6-122">專用 HSM 的名稱</span><span class="sxs-lookup"><span data-stu-id="a61b6-122">Name of the dedicated HSM</span></span>

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

### <span data-ttu-id="a61b6-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="a61b6-123">-NoWait</span></span>
<span data-ttu-id="a61b6-124">以非同步方式執行命令</span><span class="sxs-lookup"><span data-stu-id="a61b6-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="a61b6-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a61b6-125">-ResourceGroupName</span></span>
<span data-ttu-id="a61b6-126">伺服器所屬之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="a61b6-126">The name of the Resource Group to which the server belongs.</span></span>

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

### <span data-ttu-id="a61b6-127">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="a61b6-127">-SubscriptionId</span></span>
<span data-ttu-id="a61b6-128">可唯一識別 Microsoft Azure 訂閱的訂閱認證。</span><span class="sxs-lookup"><span data-stu-id="a61b6-128">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="a61b6-129">[訂閱識別碼] 會在每個服務呼叫的 URI 中形成一部分。</span><span class="sxs-lookup"><span data-stu-id="a61b6-129">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="a61b6-130">-Tag</span><span class="sxs-lookup"><span data-stu-id="a61b6-130">-Tag</span></span>
<span data-ttu-id="a61b6-131">資源標記</span><span class="sxs-lookup"><span data-stu-id="a61b6-131">Resource tags</span></span>

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

### <span data-ttu-id="a61b6-132">-確認</span><span class="sxs-lookup"><span data-stu-id="a61b6-132">-Confirm</span></span>
<span data-ttu-id="a61b6-133">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="a61b6-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a61b6-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a61b6-134">-WhatIf</span></span>
<span data-ttu-id="a61b6-135">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="a61b6-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a61b6-136">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="a61b6-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a61b6-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a61b6-137">CommonParameters</span></span>
<span data-ttu-id="a61b6-138">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="a61b6-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a61b6-139">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="a61b6-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a61b6-140">輸入</span><span class="sxs-lookup"><span data-stu-id="a61b6-140">INPUTS</span></span>

### <span data-ttu-id="a61b6-141">IDedicatedHsmIdentity （DedicatedHsm）的</span><span class="sxs-lookup"><span data-stu-id="a61b6-141">Microsoft.Azure.PowerShell.Cmdlets.DedicatedHsm.Models.IDedicatedHsmIdentity</span></span>

## <span data-ttu-id="a61b6-142">輸出</span><span class="sxs-lookup"><span data-stu-id="a61b6-142">OUTPUTS</span></span>

### <span data-ttu-id="a61b6-143">IDedicatedHsm （DedicatedHsm）。 Api20181031。</span><span class="sxs-lookup"><span data-stu-id="a61b6-143">Microsoft.Azure.PowerShell.Cmdlets.DedicatedHsm.Models.Api20181031.IDedicatedHsm</span></span>

## <span data-ttu-id="a61b6-144">筆記</span><span class="sxs-lookup"><span data-stu-id="a61b6-144">NOTES</span></span>

<span data-ttu-id="a61b6-145">別名</span><span class="sxs-lookup"><span data-stu-id="a61b6-145">ALIASES</span></span>

<span data-ttu-id="a61b6-146">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="a61b6-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="a61b6-147">若要建立如下所述的參數，請構造包含適當屬性的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="a61b6-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="a61b6-148">如需雜湊資料表的詳細資訊，請執行 Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="a61b6-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="a61b6-149">INPUTOBJECT <IDedicatedHsmIdentity> ：身分識別參數</span><span class="sxs-lookup"><span data-stu-id="a61b6-149">INPUTOBJECT <IDedicatedHsmIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="a61b6-150">`[Id <String>]`：資源身分識別路徑</span><span class="sxs-lookup"><span data-stu-id="a61b6-150">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="a61b6-151">`[Name <String>]`：專用 Hsm 的名稱</span><span class="sxs-lookup"><span data-stu-id="a61b6-151">`[Name <String>]`: Name of the dedicated Hsm</span></span>
  - <span data-ttu-id="a61b6-152">`[ResourceGroupName <String>]`：資源所屬之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="a61b6-152">`[ResourceGroupName <String>]`: The name of the Resource Group to which the resource belongs.</span></span>
  - <span data-ttu-id="a61b6-153">`[SubscriptionId <String>]`：可唯一識別 Microsoft Azure 訂閱的訂閱認證。</span><span class="sxs-lookup"><span data-stu-id="a61b6-153">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="a61b6-154">[訂閱識別碼] 會在每個服務呼叫的 URI 中形成一部分。</span><span class="sxs-lookup"><span data-stu-id="a61b6-154">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="a61b6-155">相關連結</span><span class="sxs-lookup"><span data-stu-id="a61b6-155">RELATED LINKS</span></span>

