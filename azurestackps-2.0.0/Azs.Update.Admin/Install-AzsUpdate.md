---
external help file: ''
Module Name: Azs.Update.Admin
online version: https://docs.microsoft.com/powershell/module/azs.update.admin/install-azsupdate
schema: 2.0.0
ms.openlocfilehash: e6fc8ee19443f0861fb867a5e60d0f637642ff62
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/16/2020
ms.locfileid: "93794081"
---
# <span data-ttu-id="11652-101">Install-AzsUpdate</span><span class="sxs-lookup"><span data-stu-id="11652-101">Install-AzsUpdate</span></span>

## <span data-ttu-id="11652-102">摘要</span><span class="sxs-lookup"><span data-stu-id="11652-102">SYNOPSIS</span></span>
<span data-ttu-id="11652-103">在更新位置套用特定更新。</span><span class="sxs-lookup"><span data-stu-id="11652-103">Apply a specific update at an update location.</span></span>

## <span data-ttu-id="11652-104">句法</span><span class="sxs-lookup"><span data-stu-id="11652-104">SYNTAX</span></span>

### <span data-ttu-id="11652-105">套用 (預設) </span><span class="sxs-lookup"><span data-stu-id="11652-105">Apply (Default)</span></span>
```
Install-AzsUpdate -Name <String> [-Location <String>] [-ResourceGroupName <String>] [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="11652-106">ApplyViaIdentity</span><span class="sxs-lookup"><span data-stu-id="11652-106">ApplyViaIdentity</span></span>
```
Install-AzsUpdate -InputObject <IUpdateAdminIdentity> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="11652-107">說明</span><span class="sxs-lookup"><span data-stu-id="11652-107">DESCRIPTION</span></span>
<span data-ttu-id="11652-108">在更新位置套用特定更新。</span><span class="sxs-lookup"><span data-stu-id="11652-108">Apply a specific update at an update location.</span></span>

## <span data-ttu-id="11652-109">示例</span><span class="sxs-lookup"><span data-stu-id="11652-109">EXAMPLES</span></span>

### <span data-ttu-id="11652-110">範例1：依名稱 Install-AzsUpdate</span><span class="sxs-lookup"><span data-stu-id="11652-110">Example 1: Install-AzsUpdate By Name</span></span>
```powershell
PS C:\> Install-AzsUpdate -Name Microsoft1.1907.0.10
```

<span data-ttu-id="11652-111">Commandlet 可讓您依名稱安裝特定更新。</span><span class="sxs-lookup"><span data-stu-id="11652-111">Commandlet allows you to install specific updates by name.</span></span>
<span data-ttu-id="11652-112">請注意，更新版本完全大於目前版本。</span><span class="sxs-lookup"><span data-stu-id="11652-112">Note that there is a requirement that the update version is strictly greater than the current version.</span></span>

## <span data-ttu-id="11652-113">參數</span><span class="sxs-lookup"><span data-stu-id="11652-113">PARAMETERS</span></span>

### <span data-ttu-id="11652-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="11652-114">-AsJob</span></span>
<span data-ttu-id="11652-115">執行命令做為工作</span><span class="sxs-lookup"><span data-stu-id="11652-115">Run the command as a job</span></span>

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

### <span data-ttu-id="11652-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="11652-116">-DefaultProfile</span></span>
<span data-ttu-id="11652-117">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="11652-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="11652-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="11652-118">-InputObject</span></span>
<span data-ttu-id="11652-119">要構造的身分識別參數，請參閱 INPUTOBJECT 屬性的 [記事] 區段，然後建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="11652-119">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.UpdateAdmin.Models.IUpdateAdminIdentity
Parameter Sets: ApplyViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="11652-120">-位置</span><span class="sxs-lookup"><span data-stu-id="11652-120">-Location</span></span>
<span data-ttu-id="11652-121">更新位置的名稱。</span><span class="sxs-lookup"><span data-stu-id="11652-121">The name of the update location.</span></span>

```yaml
Type: System.String
Parameter Sets: Apply
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Location
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="11652-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="11652-122">-Name</span></span>
<span data-ttu-id="11652-123">更新的名稱。</span><span class="sxs-lookup"><span data-stu-id="11652-123">Name of the update.</span></span>

```yaml
Type: System.String
Parameter Sets: Apply
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="11652-124">-NoWait</span><span class="sxs-lookup"><span data-stu-id="11652-124">-NoWait</span></span>
<span data-ttu-id="11652-125">以非同步方式執行命令</span><span class="sxs-lookup"><span data-stu-id="11652-125">Run the command asynchronously</span></span>

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

### <span data-ttu-id="11652-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="11652-126">-ResourceGroupName</span></span>
<span data-ttu-id="11652-127">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="11652-127">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: Apply
Aliases:

Required: False
Position: Named
Default value: -join("System.",(Get-AzLocation)[0].Location)
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="11652-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="11652-128">-SubscriptionId</span></span>
<span data-ttu-id="11652-129">可唯一識別 Microsoft Azure 訂閱的訂閱認證。</span><span class="sxs-lookup"><span data-stu-id="11652-129">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="11652-130">[訂閱識別碼] 會在每個服務呼叫的 URI 中形成一部分。</span><span class="sxs-lookup"><span data-stu-id="11652-130">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: Apply
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="11652-131">-確認</span><span class="sxs-lookup"><span data-stu-id="11652-131">-Confirm</span></span>
<span data-ttu-id="11652-132">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="11652-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="11652-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="11652-133">-WhatIf</span></span>
<span data-ttu-id="11652-134">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="11652-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="11652-135">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="11652-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="11652-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="11652-136">CommonParameters</span></span>
<span data-ttu-id="11652-137">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="11652-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="11652-138">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="11652-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="11652-139">輸入</span><span class="sxs-lookup"><span data-stu-id="11652-139">INPUTS</span></span>

### <span data-ttu-id="11652-140">IUpdateAdminIdentity （UpdateAdmin）的</span><span class="sxs-lookup"><span data-stu-id="11652-140">Microsoft.Azure.PowerShell.Cmdlets.UpdateAdmin.Models.IUpdateAdminIdentity</span></span>

## <span data-ttu-id="11652-141">輸出</span><span class="sxs-lookup"><span data-stu-id="11652-141">OUTPUTS</span></span>

### <span data-ttu-id="11652-142">IUpdateRun （UpdateAdmin）。 Api20160501。</span><span class="sxs-lookup"><span data-stu-id="11652-142">Microsoft.Azure.PowerShell.Cmdlets.UpdateAdmin.Models.Api20160501.IUpdateRun</span></span>



## <span data-ttu-id="11652-143">筆記</span><span class="sxs-lookup"><span data-stu-id="11652-143">NOTES</span></span>

<span data-ttu-id="11652-144">複雜參數屬性若要建立如下所述的參數，請構造包含適當屬性的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="11652-144">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="11652-145">如需雜湊資料表的詳細資訊，請執行 Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="11652-145">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="11652-146">INPUTOBJECT <IUpdateAdminIdentity> ：身分識別參數</span><span class="sxs-lookup"><span data-stu-id="11652-146">INPUTOBJECT <IUpdateAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="11652-147">`[Id <String>]`：資源身分識別路徑</span><span class="sxs-lookup"><span data-stu-id="11652-147">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="11652-148">`[ResourceGroupName <String>]`：資源組名。</span><span class="sxs-lookup"><span data-stu-id="11652-148">`[ResourceGroupName <String>]`: Resource group name.</span></span>
  - <span data-ttu-id="11652-149">`[RunName <String>]`：更新執行識別碼。</span><span class="sxs-lookup"><span data-stu-id="11652-149">`[RunName <String>]`: Update run identifier.</span></span>
  - <span data-ttu-id="11652-150">`[SubscriptionId <String>]`：可唯一識別 Microsoft Azure 訂閱的訂閱認證。</span><span class="sxs-lookup"><span data-stu-id="11652-150">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>  <span data-ttu-id="11652-151">[訂閱識別碼] 會在每個服務呼叫的 URI 中形成一部分。</span><span class="sxs-lookup"><span data-stu-id="11652-151">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="11652-152">`[UpdateLocation <String>]`：更新位置的名稱。</span><span class="sxs-lookup"><span data-stu-id="11652-152">`[UpdateLocation <String>]`: The name of the update location.</span></span>
  - <span data-ttu-id="11652-153">`[UpdateName <String>]`：更新的名稱。</span><span class="sxs-lookup"><span data-stu-id="11652-153">`[UpdateName <String>]`: Name of the update.</span></span>

## <span data-ttu-id="11652-154">相關連結</span><span class="sxs-lookup"><span data-stu-id="11652-154">RELATED LINKS</span></span>

