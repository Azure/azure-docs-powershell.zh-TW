---
external help file: ''
Module Name: Az.Portal
online version: https://docs.microsoft.com/en-us/powershell/module/az.portal/update-azportaldashboard
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Portal/help/Update-AzPortalDashboard.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Portal/help/Update-AzPortalDashboard.md
ms.openlocfilehash: 42c5d90a24e671c47245ace0046c6f5987dbcd94
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98281059"
---
# <span data-ttu-id="58b9f-101">Update-AzPortalDashboard</span><span class="sxs-lookup"><span data-stu-id="58b9f-101">Update-AzPortalDashboard</span></span>

## <span data-ttu-id="58b9f-102">摘要</span><span class="sxs-lookup"><span data-stu-id="58b9f-102">SYNOPSIS</span></span>
<span data-ttu-id="58b9f-103">更新現有的儀表板。</span><span class="sxs-lookup"><span data-stu-id="58b9f-103">Updates an existing Dashboard.</span></span>

## <span data-ttu-id="58b9f-104">句法</span><span class="sxs-lookup"><span data-stu-id="58b9f-104">SYNTAX</span></span>

### <span data-ttu-id="58b9f-105">UpdateExpanded (預設) </span><span class="sxs-lookup"><span data-stu-id="58b9f-105">UpdateExpanded (Default)</span></span>
```
Update-AzPortalDashboard -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-Lens <Hashtable>] [-Metadata <Hashtable>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="58b9f-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="58b9f-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzPortalDashboard -InputObject <IPortalIdentity> [-Lens <Hashtable>] [-Metadata <Hashtable>]
 [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="58b9f-107">說明</span><span class="sxs-lookup"><span data-stu-id="58b9f-107">DESCRIPTION</span></span>
<span data-ttu-id="58b9f-108">更新現有的儀表板。</span><span class="sxs-lookup"><span data-stu-id="58b9f-108">Updates an existing Dashboard.</span></span>

## <span data-ttu-id="58b9f-109">示例</span><span class="sxs-lookup"><span data-stu-id="58b9f-109">EXAMPLES</span></span>

### <span data-ttu-id="58b9f-110">範例1：更新儀表板的標記</span><span class="sxs-lookup"><span data-stu-id="58b9f-110">Example 1: Update the Tags of a Dashboard</span></span>
```powershell
PS C:\> Update-AzPortalDashboard -ResourceGroupName my-rg -Name dashbase03 -Tag @{'hidden-title'="My Dashboard Title"; NewTag="NewValue"}

Location Name       Type
-------- ----       ----
eastasia dashbase03 Microsoft.Portal/dashboards
```

<span data-ttu-id="58b9f-111">更新儀表板中的標記。</span><span class="sxs-lookup"><span data-stu-id="58b9f-111">Update the tags in a dashboard.</span></span>
<span data-ttu-id="58b9f-112">標記會以內聯 hashtable 表示。</span><span class="sxs-lookup"><span data-stu-id="58b9f-112">Tags are represented as an inline hashtable.</span></span>

### <span data-ttu-id="58b9f-113">範例2：使用管線更新儀表板標記</span><span class="sxs-lookup"><span data-stu-id="58b9f-113">Example 2: Update Dashboard tags using the pipeline</span></span>
```powershell
PS C:\> Get-AzPortalDashboard -ResourceGroupName my-rg -Name dashbase03 | Update-AzPortalDashboard -Tag @{'hidden-title'="My Dashboard Title"; NewTag="NewValue"}

Location Name       Type
-------- ----       ----
eastasia dashbase03 Microsoft.Portal/dashboards
```

<span data-ttu-id="58b9f-114">使用 AzPortalDashboard 更新儀表板中的標記。</span><span class="sxs-lookup"><span data-stu-id="58b9f-114">Update the Tags in a Dashboard retried using Get-AzPortalDashboard.</span></span>
<span data-ttu-id="58b9f-115">這可以用來更新單一儀表板或多個 dashboardfs 上的標記。</span><span class="sxs-lookup"><span data-stu-id="58b9f-115">This can be used to update the tags over a single dashboard, or multiple dashboardfs.</span></span>

## <span data-ttu-id="58b9f-116">參數</span><span class="sxs-lookup"><span data-stu-id="58b9f-116">PARAMETERS</span></span>

### <span data-ttu-id="58b9f-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="58b9f-117">-DefaultProfile</span></span>
<span data-ttu-id="58b9f-118">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="58b9f-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="58b9f-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="58b9f-119">-InputObject</span></span>
<span data-ttu-id="58b9f-120">要構造的身分識別參數，請參閱 INPUTOBJECT 屬性的 [記事] 區段，然後建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="58b9f-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Portal.Models.IPortalIdentity
Parameter Sets: UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="58b9f-121">-透鏡</span><span class="sxs-lookup"><span data-stu-id="58b9f-121">-Lens</span></span>
<span data-ttu-id="58b9f-122">儀表板鏡頭。</span><span class="sxs-lookup"><span data-stu-id="58b9f-122">The dashboard lenses.</span></span>

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

### <span data-ttu-id="58b9f-123">-中繼資料</span><span class="sxs-lookup"><span data-stu-id="58b9f-123">-Metadata</span></span>
<span data-ttu-id="58b9f-124">儀表板中繼資料。</span><span class="sxs-lookup"><span data-stu-id="58b9f-124">The dashboard metadata.</span></span>

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

### <span data-ttu-id="58b9f-125">-名稱</span><span class="sxs-lookup"><span data-stu-id="58b9f-125">-Name</span></span>
<span data-ttu-id="58b9f-126">儀表板的名稱。</span><span class="sxs-lookup"><span data-stu-id="58b9f-126">The name of the dashboard.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: DashboardName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="58b9f-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="58b9f-127">-ResourceGroupName</span></span>
<span data-ttu-id="58b9f-128">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="58b9f-128">The name of the resource group.</span></span>

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

### <span data-ttu-id="58b9f-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="58b9f-129">-SubscriptionId</span></span>
<span data-ttu-id="58b9f-130">Azure 訂閱 ID。</span><span class="sxs-lookup"><span data-stu-id="58b9f-130">The Azure subscription ID.</span></span>
<span data-ttu-id="58b9f-131">這是 GUID 格式的字串 (例如 00000000-0000-0000-0000-000000000000) </span><span class="sxs-lookup"><span data-stu-id="58b9f-131">This is a GUID-formatted string (e.g. 00000000-0000-0000-0000-000000000000)</span></span>

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

### <span data-ttu-id="58b9f-132">-Tag</span><span class="sxs-lookup"><span data-stu-id="58b9f-132">-Tag</span></span>
<span data-ttu-id="58b9f-133">資源標記</span><span class="sxs-lookup"><span data-stu-id="58b9f-133">Resource tags</span></span>

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

### <span data-ttu-id="58b9f-134">-確認</span><span class="sxs-lookup"><span data-stu-id="58b9f-134">-Confirm</span></span>
<span data-ttu-id="58b9f-135">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="58b9f-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="58b9f-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="58b9f-136">-WhatIf</span></span>
<span data-ttu-id="58b9f-137">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="58b9f-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="58b9f-138">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="58b9f-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="58b9f-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="58b9f-139">CommonParameters</span></span>
<span data-ttu-id="58b9f-140">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="58b9f-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="58b9f-141">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="58b9f-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="58b9f-142">輸入</span><span class="sxs-lookup"><span data-stu-id="58b9f-142">INPUTS</span></span>

### <span data-ttu-id="58b9f-143">IPortalIdentity 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="58b9f-143">Microsoft.Azure.PowerShell.Cmdlets.Portal.Models.IPortalIdentity</span></span>

## <span data-ttu-id="58b9f-144">輸出</span><span class="sxs-lookup"><span data-stu-id="58b9f-144">OUTPUTS</span></span>

### <span data-ttu-id="58b9f-145">[Api201901Preview. IDashboard] （）</span><span class="sxs-lookup"><span data-stu-id="58b9f-145">Microsoft.Azure.PowerShell.Cmdlets.Portal.Models.Api201901Preview.IDashboard</span></span>

## <span data-ttu-id="58b9f-146">筆記</span><span class="sxs-lookup"><span data-stu-id="58b9f-146">NOTES</span></span>

<span data-ttu-id="58b9f-147">別名</span><span class="sxs-lookup"><span data-stu-id="58b9f-147">ALIASES</span></span>

<span data-ttu-id="58b9f-148">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="58b9f-148">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="58b9f-149">若要建立如下所述的參數，請構造包含適當屬性的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="58b9f-149">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="58b9f-150">如需雜湊資料表的詳細資訊，請執行 Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="58b9f-150">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="58b9f-151">INPUTOBJECT <IPortalIdentity> ：身分識別參數</span><span class="sxs-lookup"><span data-stu-id="58b9f-151">INPUTOBJECT <IPortalIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="58b9f-152">`[DashboardName <String>]`：儀表板的名稱。</span><span class="sxs-lookup"><span data-stu-id="58b9f-152">`[DashboardName <String>]`: The name of the dashboard.</span></span>
  - <span data-ttu-id="58b9f-153">`[Id <String>]`：資源身分識別路徑</span><span class="sxs-lookup"><span data-stu-id="58b9f-153">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="58b9f-154">`[ResourceGroupName <String>]`：資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="58b9f-154">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="58b9f-155">`[SubscriptionId <String>]`： Azure 訂閱 ID。</span><span class="sxs-lookup"><span data-stu-id="58b9f-155">`[SubscriptionId <String>]`: The Azure subscription ID.</span></span> <span data-ttu-id="58b9f-156">這是 GUID 格式的字串 (例如 00000000-0000-0000-0000-000000000000) </span><span class="sxs-lookup"><span data-stu-id="58b9f-156">This is a GUID-formatted string (e.g. 00000000-0000-0000-0000-000000000000)</span></span>

## <span data-ttu-id="58b9f-157">相關連結</span><span class="sxs-lookup"><span data-stu-id="58b9f-157">RELATED LINKS</span></span>

