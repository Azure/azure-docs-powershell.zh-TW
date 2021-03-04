---
external help file: ''
Module Name: Az.DedicatedHsm
online version: https://docs.microsoft.com/powershell/module/az.dedicatedhsm/remove-azdedicatedhsm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DedicatedHsm/help/Remove-AzDedicatedHsm.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DedicatedHsm/help/Remove-AzDedicatedHsm.md
ms.openlocfilehash: 0f9369e3ad2427fc633239b9775f485db01e87b1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101904466"
---
# <span data-ttu-id="a393c-101">Remove-AzDedicatedHsm</span><span class="sxs-lookup"><span data-stu-id="a393c-101">Remove-AzDedicatedHsm</span></span>

## <span data-ttu-id="a393c-102">簡介</span><span class="sxs-lookup"><span data-stu-id="a393c-102">SYNOPSIS</span></span>
<span data-ttu-id="a393c-103">刪除指定的 Azure Dedicated HSM。</span><span class="sxs-lookup"><span data-stu-id="a393c-103">Deletes the specified Azure Dedicated HSM.</span></span>

## <span data-ttu-id="a393c-104">語法</span><span class="sxs-lookup"><span data-stu-id="a393c-104">SYNTAX</span></span>

### <span data-ttu-id="a393c-105">刪除 (預設) </span><span class="sxs-lookup"><span data-stu-id="a393c-105">Delete (Default)</span></span>
```
Remove-AzDedicatedHsm -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="a393c-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="a393c-106">DeleteViaIdentity</span></span>
```
Remove-AzDedicatedHsm -InputObject <IDedicatedHsmIdentity> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="a393c-107">描述</span><span class="sxs-lookup"><span data-stu-id="a393c-107">DESCRIPTION</span></span>
<span data-ttu-id="a393c-108">刪除指定的 Azure Dedicated HSM。</span><span class="sxs-lookup"><span data-stu-id="a393c-108">Deletes the specified Azure Dedicated HSM.</span></span>

## <span data-ttu-id="a393c-109">例子</span><span class="sxs-lookup"><span data-stu-id="a393c-109">EXAMPLES</span></span>

### <span data-ttu-id="a393c-110">範例 1：根據名稱移除專用 HSM</span><span class="sxs-lookup"><span data-stu-id="a393c-110">Example 1: Remove a Dedicated HSM by name</span></span>
```powershell
PS C:\> Remove-AzDedicatedHsm -Name hsm-7t2xaf -ResourceGroupName lucas-manual-test

```

<span data-ttu-id="a393c-111">此元件會移除 HSM (硬體) 模組。</span><span class="sxs-lookup"><span data-stu-id="a393c-111">This commnad removes a hardware security module(HSM) by name.</span></span>

### <span data-ttu-id="a393c-112">範例 2：移除物件專用 HSM</span><span class="sxs-lookup"><span data-stu-id="a393c-112">Example 2: Remove a Dedicated HSM  by object</span></span>
```powershell
PS C:\> $hsm = Get-AzDedicatedHsm -Name hsm-7t2xaf -ResourceGroupName dedicatedhsm-rg-n359cz
PS C:\> Remove-AzDedicatedHsm -InputObject  $hsm

```

<span data-ttu-id="a393c-113">此通訊會根據物件移除專用 HSM。</span><span class="sxs-lookup"><span data-stu-id="a393c-113">This commnad removes a Dedicated HSM by object.</span></span>

## <span data-ttu-id="a393c-114">參數</span><span class="sxs-lookup"><span data-stu-id="a393c-114">PARAMETERS</span></span>

### <span data-ttu-id="a393c-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a393c-115">-AsJob</span></span>
<span data-ttu-id="a393c-116">以工作執行命令</span><span class="sxs-lookup"><span data-stu-id="a393c-116">Run the command as a job</span></span>

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

### <span data-ttu-id="a393c-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a393c-117">-DefaultProfile</span></span>
<span data-ttu-id="a393c-118">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="a393c-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a393c-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a393c-119">-InputObject</span></span>
<span data-ttu-id="a393c-120">身分識別參數若要建構，請參閱 INPUTOBJECT 屬性的 NOTES 區段，並建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="a393c-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DedicatedHsm.Models.IDedicatedHsmIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a393c-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="a393c-121">-Name</span></span>
<span data-ttu-id="a393c-122">要刪除的專用 HSM 名稱</span><span class="sxs-lookup"><span data-stu-id="a393c-122">The name of the dedicated HSM to delete</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a393c-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="a393c-123">-NoWait</span></span>
<span data-ttu-id="a393c-124">非同步執行命令</span><span class="sxs-lookup"><span data-stu-id="a393c-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="a393c-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a393c-125">-PassThru</span></span>
<span data-ttu-id="a393c-126">命令成功時，會返回 True</span><span class="sxs-lookup"><span data-stu-id="a393c-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="a393c-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a393c-127">-ResourceGroupName</span></span>
<span data-ttu-id="a393c-128">專用 HSM 所屬的資源組名。</span><span class="sxs-lookup"><span data-stu-id="a393c-128">The name of the Resource Group to which the dedicated HSM belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a393c-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="a393c-129">-SubscriptionId</span></span>
<span data-ttu-id="a393c-130">可唯一識別 Microsoft Azure 訂閱的訂閱認證。</span><span class="sxs-lookup"><span data-stu-id="a393c-130">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="a393c-131">訂閱識別碼會構成每個服務通話 URI 的一部分。</span><span class="sxs-lookup"><span data-stu-id="a393c-131">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a393c-132">-確認</span><span class="sxs-lookup"><span data-stu-id="a393c-132">-Confirm</span></span>
<span data-ttu-id="a393c-133">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="a393c-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a393c-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a393c-134">-WhatIf</span></span>
<span data-ttu-id="a393c-135">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="a393c-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a393c-136">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="a393c-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a393c-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a393c-137">CommonParameters</span></span>
<span data-ttu-id="a393c-138">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="a393c-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a393c-139">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a393c-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a393c-140">輸入</span><span class="sxs-lookup"><span data-stu-id="a393c-140">INPUTS</span></span>

### <span data-ttu-id="a393c-141">Microsoft.Azure.PowerShell.Cmdlets.DedicatedVtm.models.IDedicatedSoftmIdentity</span><span class="sxs-lookup"><span data-stu-id="a393c-141">Microsoft.Azure.PowerShell.Cmdlets.DedicatedHsm.Models.IDedicatedHsmIdentity</span></span>

## <span data-ttu-id="a393c-142">輸出</span><span class="sxs-lookup"><span data-stu-id="a393c-142">OUTPUTS</span></span>

### <span data-ttu-id="a393c-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="a393c-143">System.Boolean</span></span>

## <span data-ttu-id="a393c-144">筆記</span><span class="sxs-lookup"><span data-stu-id="a393c-144">NOTES</span></span>

<span data-ttu-id="a393c-145">別名</span><span class="sxs-lookup"><span data-stu-id="a393c-145">ALIASES</span></span>

<span data-ttu-id="a393c-146">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="a393c-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="a393c-147">若要建立下列描述的參數，請建構包含適當屬性的雜湊表。</span><span class="sxs-lookup"><span data-stu-id="a393c-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="a393c-148">有關雜湊表的資訊，請執行Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="a393c-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="a393c-149">INPUTOBJECT： <IDedicatedHsmIdentity> 身分識別參數</span><span class="sxs-lookup"><span data-stu-id="a393c-149">INPUTOBJECT <IDedicatedHsmIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="a393c-150">`[Id <String>]`：資源識別路徑</span><span class="sxs-lookup"><span data-stu-id="a393c-150">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="a393c-151">`[Name <String>]`：專用 Hsm 的名稱</span><span class="sxs-lookup"><span data-stu-id="a393c-151">`[Name <String>]`: Name of the dedicated Hsm</span></span>
  - <span data-ttu-id="a393c-152">`[ResourceGroupName <String>]`：資源所屬的資源組名。</span><span class="sxs-lookup"><span data-stu-id="a393c-152">`[ResourceGroupName <String>]`: The name of the Resource Group to which the resource belongs.</span></span>
  - <span data-ttu-id="a393c-153">`[SubscriptionId <String>]`：可唯一識別 Microsoft Azure 訂閱的訂閱認證。</span><span class="sxs-lookup"><span data-stu-id="a393c-153">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="a393c-154">訂閱識別碼會構成每個服務通話 URI 的一部分。</span><span class="sxs-lookup"><span data-stu-id="a393c-154">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="a393c-155">相關連結</span><span class="sxs-lookup"><span data-stu-id="a393c-155">RELATED LINKS</span></span>

