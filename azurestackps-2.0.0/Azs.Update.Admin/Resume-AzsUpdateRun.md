---
external help file: ''
Module Name: Azs.Update.Admin
online version: https://docs.microsoft.com/powershell/module/azs.update.admin/resume-azsupdaterun
schema: 2.0.0
ms.openlocfilehash: 65d2b3a045d38435cdd709d47c0be88f7fc98af0
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/16/2020
ms.locfileid: "93794076"
---
# <span data-ttu-id="4f021-101">Resume-AzsUpdateRun</span><span class="sxs-lookup"><span data-stu-id="4f021-101">Resume-AzsUpdateRun</span></span>

## <span data-ttu-id="4f021-102">摘要</span><span class="sxs-lookup"><span data-stu-id="4f021-102">SYNOPSIS</span></span>
<span data-ttu-id="4f021-103">繼續失敗的更新。</span><span class="sxs-lookup"><span data-stu-id="4f021-103">Resume a failed update.</span></span>

## <span data-ttu-id="4f021-104">句法</span><span class="sxs-lookup"><span data-stu-id="4f021-104">SYNTAX</span></span>

### <span data-ttu-id="4f021-105">重新執行 (預設) </span><span class="sxs-lookup"><span data-stu-id="4f021-105">Rerun (Default)</span></span>
```
Resume-AzsUpdateRun -Name <String> -UpdateName <String> [-Location <String>] [-ResourceGroupName <String>]
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="4f021-106">RerunViaIdentity</span><span class="sxs-lookup"><span data-stu-id="4f021-106">RerunViaIdentity</span></span>
```
Resume-AzsUpdateRun -InputObject <IUpdateAdminIdentity> [-DefaultProfile <PSObject>] [-PassThru] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="4f021-107">說明</span><span class="sxs-lookup"><span data-stu-id="4f021-107">DESCRIPTION</span></span>
<span data-ttu-id="4f021-108">繼續失敗的更新。</span><span class="sxs-lookup"><span data-stu-id="4f021-108">Resume a failed update.</span></span>

## <span data-ttu-id="4f021-109">示例</span><span class="sxs-lookup"><span data-stu-id="4f021-109">EXAMPLES</span></span>

### <span data-ttu-id="4f021-110">範例1：依名稱和 UpdateName Resume-AzsUpdateRun</span><span class="sxs-lookup"><span data-stu-id="4f021-110">Example 1: Resume-AzsUpdateRun By Name and UpdateName</span></span>
```powershell
PS C:\> Resume-AzsUpdateRun -UpdateName northwest/Microsoft1.1907.0.10 -Name 45aaeb26-805b-495b-9c8c-d5da5542dbf4

```

<span data-ttu-id="4f021-111">Commandlet 可讓您重新執行特定的失敗更新運行。</span><span class="sxs-lookup"><span data-stu-id="4f021-111">Commandlet allows you to rerun a specific failed update run.</span></span>
<span data-ttu-id="4f021-112">請注意，更新版本完全大於目前版本。</span><span class="sxs-lookup"><span data-stu-id="4f021-112">Note that there is a requirement that the update version is strictly greater than the current version.</span></span>

## <span data-ttu-id="4f021-113">參數</span><span class="sxs-lookup"><span data-stu-id="4f021-113">PARAMETERS</span></span>

### <span data-ttu-id="4f021-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4f021-114">-DefaultProfile</span></span>
<span data-ttu-id="4f021-115">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="4f021-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4f021-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4f021-116">-InputObject</span></span>
<span data-ttu-id="4f021-117">要構造的身分識別參數，請參閱 INPUTOBJECT 屬性的 [記事] 區段，然後建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="4f021-117">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.UpdateAdmin.Models.IUpdateAdminIdentity
Parameter Sets: RerunViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="4f021-118">-位置</span><span class="sxs-lookup"><span data-stu-id="4f021-118">-Location</span></span>
<span data-ttu-id="4f021-119">更新位置的名稱。</span><span class="sxs-lookup"><span data-stu-id="4f021-119">The name of the update location.</span></span>

```yaml
Type: System.String
Parameter Sets: Rerun
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Location
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="4f021-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="4f021-120">-Name</span></span>
<span data-ttu-id="4f021-121">更新執行識別碼。</span><span class="sxs-lookup"><span data-stu-id="4f021-121">Update run identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: Rerun
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="4f021-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4f021-122">-PassThru</span></span>
<span data-ttu-id="4f021-123">在命令成功時傳回 true</span><span class="sxs-lookup"><span data-stu-id="4f021-123">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="4f021-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4f021-124">-ResourceGroupName</span></span>
<span data-ttu-id="4f021-125">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="4f021-125">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: Rerun
Aliases:

Required: False
Position: Named
Default value: -join("System.",(Get-AzLocation)[0].Location)
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="4f021-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="4f021-126">-SubscriptionId</span></span>
<span data-ttu-id="4f021-127">可唯一識別 Microsoft Azure 訂閱的訂閱認證。</span><span class="sxs-lookup"><span data-stu-id="4f021-127">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="4f021-128">[訂閱識別碼] 會在每個服務呼叫的 URI 中形成一部分。</span><span class="sxs-lookup"><span data-stu-id="4f021-128">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: Rerun
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="4f021-129">-UpdateName</span><span class="sxs-lookup"><span data-stu-id="4f021-129">-UpdateName</span></span>
<span data-ttu-id="4f021-130">更新的名稱。</span><span class="sxs-lookup"><span data-stu-id="4f021-130">Name of the update.</span></span>

```yaml
Type: System.String
Parameter Sets: Rerun
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="4f021-131">-確認</span><span class="sxs-lookup"><span data-stu-id="4f021-131">-Confirm</span></span>
<span data-ttu-id="4f021-132">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="4f021-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4f021-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4f021-133">-WhatIf</span></span>
<span data-ttu-id="4f021-134">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="4f021-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4f021-135">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="4f021-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4f021-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4f021-136">CommonParameters</span></span>
<span data-ttu-id="4f021-137">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="4f021-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4f021-138">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="4f021-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4f021-139">輸入</span><span class="sxs-lookup"><span data-stu-id="4f021-139">INPUTS</span></span>

### <span data-ttu-id="4f021-140">IUpdateAdminIdentity （UpdateAdmin）的</span><span class="sxs-lookup"><span data-stu-id="4f021-140">Microsoft.Azure.PowerShell.Cmdlets.UpdateAdmin.Models.IUpdateAdminIdentity</span></span>

## <span data-ttu-id="4f021-141">輸出</span><span class="sxs-lookup"><span data-stu-id="4f021-141">OUTPUTS</span></span>

### <span data-ttu-id="4f021-142">System.object</span><span class="sxs-lookup"><span data-stu-id="4f021-142">System.Boolean</span></span>



## <span data-ttu-id="4f021-143">筆記</span><span class="sxs-lookup"><span data-stu-id="4f021-143">NOTES</span></span>

<span data-ttu-id="4f021-144">複雜參數屬性若要建立如下所述的參數，請構造包含適當屬性的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="4f021-144">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="4f021-145">如需雜湊資料表的詳細資訊，請執行 Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="4f021-145">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="4f021-146">INPUTOBJECT <IUpdateAdminIdentity> ：身分識別參數</span><span class="sxs-lookup"><span data-stu-id="4f021-146">INPUTOBJECT <IUpdateAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="4f021-147">`[Id <String>]`：資源身分識別路徑</span><span class="sxs-lookup"><span data-stu-id="4f021-147">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="4f021-148">`[ResourceGroupName <String>]`：資源組名。</span><span class="sxs-lookup"><span data-stu-id="4f021-148">`[ResourceGroupName <String>]`: Resource group name.</span></span>
  - <span data-ttu-id="4f021-149">`[RunName <String>]`：更新執行識別碼。</span><span class="sxs-lookup"><span data-stu-id="4f021-149">`[RunName <String>]`: Update run identifier.</span></span>
  - <span data-ttu-id="4f021-150">`[SubscriptionId <String>]`：可唯一識別 Microsoft Azure 訂閱的訂閱認證。</span><span class="sxs-lookup"><span data-stu-id="4f021-150">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>  <span data-ttu-id="4f021-151">[訂閱識別碼] 會在每個服務呼叫的 URI 中形成一部分。</span><span class="sxs-lookup"><span data-stu-id="4f021-151">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="4f021-152">`[UpdateLocation <String>]`：更新位置的名稱。</span><span class="sxs-lookup"><span data-stu-id="4f021-152">`[UpdateLocation <String>]`: The name of the update location.</span></span>
  - <span data-ttu-id="4f021-153">`[UpdateName <String>]`：更新的名稱。</span><span class="sxs-lookup"><span data-stu-id="4f021-153">`[UpdateName <String>]`: Name of the update.</span></span>

## <span data-ttu-id="4f021-154">相關連結</span><span class="sxs-lookup"><span data-stu-id="4f021-154">RELATED LINKS</span></span>

