---
external help file: ''
Module Name: Az.Portal
online version: https://docs.microsoft.com/powershell/module/az.portal/update-azportaldashboard
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Portal/help/Update-AzPortalDashboard.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Portal/help/Update-AzPortalDashboard.md
ms.openlocfilehash: 97d5519d1b643a04fb1f6375030f178f9ccfbfe1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101911322"
---
# <span data-ttu-id="05895-101">Update-AzPortalDashboard</span><span class="sxs-lookup"><span data-stu-id="05895-101">Update-AzPortalDashboard</span></span>

## <span data-ttu-id="05895-102">簡介</span><span class="sxs-lookup"><span data-stu-id="05895-102">SYNOPSIS</span></span>
<span data-ttu-id="05895-103">更新現有的儀表板。</span><span class="sxs-lookup"><span data-stu-id="05895-103">Updates an existing Dashboard.</span></span>

## <span data-ttu-id="05895-104">語法</span><span class="sxs-lookup"><span data-stu-id="05895-104">SYNTAX</span></span>

### <span data-ttu-id="05895-105">UpdateExpanded (預設) </span><span class="sxs-lookup"><span data-stu-id="05895-105">UpdateExpanded (Default)</span></span>
```
Update-AzPortalDashboard -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-Lens <Hashtable>] [-Metadata <Hashtable>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="05895-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="05895-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzPortalDashboard -InputObject <IPortalIdentity> [-Lens <Hashtable>] [-Metadata <Hashtable>]
 [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="05895-107">描述</span><span class="sxs-lookup"><span data-stu-id="05895-107">DESCRIPTION</span></span>
<span data-ttu-id="05895-108">更新現有的儀表板。</span><span class="sxs-lookup"><span data-stu-id="05895-108">Updates an existing Dashboard.</span></span>

## <span data-ttu-id="05895-109">例子</span><span class="sxs-lookup"><span data-stu-id="05895-109">EXAMPLES</span></span>

### <span data-ttu-id="05895-110">範例 1：更新儀表板的標記</span><span class="sxs-lookup"><span data-stu-id="05895-110">Example 1: Update the Tags of a Dashboard</span></span>
```powershell
PS C:\> Update-AzPortalDashboard -ResourceGroupName my-rg -Name dashbase03 -Tag @{'hidden-title'="My Dashboard Title"; NewTag="NewValue"}

Location Name       Type
-------- ----       ----
eastasia dashbase03 Microsoft.Portal/dashboards
```

<span data-ttu-id="05895-111">更新儀表板中的標記。</span><span class="sxs-lookup"><span data-stu-id="05895-111">Update the tags in a dashboard.</span></span>
<span data-ttu-id="05895-112">標記會以內嵌雜湊表表示。</span><span class="sxs-lookup"><span data-stu-id="05895-112">Tags are represented as an inline hashtable.</span></span>

### <span data-ttu-id="05895-113">範例 2：使用管線更新儀表板標記</span><span class="sxs-lookup"><span data-stu-id="05895-113">Example 2: Update Dashboard tags using the pipeline</span></span>
```powershell
PS C:\> Get-AzPortalDashboard -ResourceGroupName my-rg -Name dashbase03 | Update-AzPortalDashboard -Tag @{'hidden-title'="My Dashboard Title"; NewTag="NewValue"}

Location Name       Type
-------- ----       ----
eastasia dashbase03 Microsoft.Portal/dashboards
```

<span data-ttu-id="05895-114">使用 Get-AzPortalDashboard 重新重試的儀表板中的標記。</span><span class="sxs-lookup"><span data-stu-id="05895-114">Update the Tags in a Dashboard retried using Get-AzPortalDashboard.</span></span>
<span data-ttu-id="05895-115">這可以用來更新單一儀表板或多個儀表板上的標記。</span><span class="sxs-lookup"><span data-stu-id="05895-115">This can be used to update the tags over a single dashboard, or multiple dashboardfs.</span></span>

## <span data-ttu-id="05895-116">參數</span><span class="sxs-lookup"><span data-stu-id="05895-116">PARAMETERS</span></span>

### <span data-ttu-id="05895-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="05895-117">-DefaultProfile</span></span>
<span data-ttu-id="05895-118">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="05895-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="05895-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="05895-119">-InputObject</span></span>
<span data-ttu-id="05895-120">身分識別參數若要建構，請參閱 INPUTOBJECT 屬性的 NOTES 區段，並建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="05895-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="05895-121">-Lens</span><span class="sxs-lookup"><span data-stu-id="05895-121">-Lens</span></span>
<span data-ttu-id="05895-122">儀表板儀表板。</span><span class="sxs-lookup"><span data-stu-id="05895-122">The dashboard lenses.</span></span>

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

### <span data-ttu-id="05895-123">-中繼資料</span><span class="sxs-lookup"><span data-stu-id="05895-123">-Metadata</span></span>
<span data-ttu-id="05895-124">儀表板中繼資料。</span><span class="sxs-lookup"><span data-stu-id="05895-124">The dashboard metadata.</span></span>

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

### <span data-ttu-id="05895-125">-名稱</span><span class="sxs-lookup"><span data-stu-id="05895-125">-Name</span></span>
<span data-ttu-id="05895-126">儀表板的名稱。</span><span class="sxs-lookup"><span data-stu-id="05895-126">The name of the dashboard.</span></span>

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

### <span data-ttu-id="05895-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="05895-127">-ResourceGroupName</span></span>
<span data-ttu-id="05895-128">資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="05895-128">The name of the resource group.</span></span>

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

### <span data-ttu-id="05895-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="05895-129">-SubscriptionId</span></span>
<span data-ttu-id="05895-130">Azure 訂閱識別碼。</span><span class="sxs-lookup"><span data-stu-id="05895-130">The Azure subscription ID.</span></span>
<span data-ttu-id="05895-131">這是 GUID 格式的字串 (例如 00000000-0000-0000-0000-00000000000000000000000000000000000000000000000000000) </span><span class="sxs-lookup"><span data-stu-id="05895-131">This is a GUID-formatted string (e.g. 00000000-0000-0000-0000-000000000000)</span></span>

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

### <span data-ttu-id="05895-132">-標記</span><span class="sxs-lookup"><span data-stu-id="05895-132">-Tag</span></span>
<span data-ttu-id="05895-133">資源標記</span><span class="sxs-lookup"><span data-stu-id="05895-133">Resource tags</span></span>

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

### <span data-ttu-id="05895-134">-確認</span><span class="sxs-lookup"><span data-stu-id="05895-134">-Confirm</span></span>
<span data-ttu-id="05895-135">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="05895-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="05895-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="05895-136">-WhatIf</span></span>
<span data-ttu-id="05895-137">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="05895-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="05895-138">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="05895-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="05895-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="05895-139">CommonParameters</span></span>
<span data-ttu-id="05895-140">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="05895-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="05895-141">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="05895-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="05895-142">輸入</span><span class="sxs-lookup"><span data-stu-id="05895-142">INPUTS</span></span>

### <span data-ttu-id="05895-143">Microsoft.Azure.PowerShell.Cmdlets.Portal.models.IPortalIdentity</span><span class="sxs-lookup"><span data-stu-id="05895-143">Microsoft.Azure.PowerShell.Cmdlets.Portal.Models.IPortalIdentity</span></span>

## <span data-ttu-id="05895-144">輸出</span><span class="sxs-lookup"><span data-stu-id="05895-144">OUTPUTS</span></span>

### <span data-ttu-id="05895-145">Microsoft.Azure.PowerShell.Cmdlets.Portal.Models.Api201901Preview.IDashboard</span><span class="sxs-lookup"><span data-stu-id="05895-145">Microsoft.Azure.PowerShell.Cmdlets.Portal.Models.Api201901Preview.IDashboard</span></span>

## <span data-ttu-id="05895-146">筆記</span><span class="sxs-lookup"><span data-stu-id="05895-146">NOTES</span></span>

<span data-ttu-id="05895-147">別名</span><span class="sxs-lookup"><span data-stu-id="05895-147">ALIASES</span></span>

<span data-ttu-id="05895-148">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="05895-148">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="05895-149">若要建立下列描述的參數，請建構包含適當屬性的雜湊表。</span><span class="sxs-lookup"><span data-stu-id="05895-149">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="05895-150">有關雜湊表的資訊，請執行Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="05895-150">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="05895-151">INPUTOBJECT： <IPortalIdentity> 身分識別參數</span><span class="sxs-lookup"><span data-stu-id="05895-151">INPUTOBJECT <IPortalIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="05895-152">`[DashboardName <String>]`：儀表板的名稱。</span><span class="sxs-lookup"><span data-stu-id="05895-152">`[DashboardName <String>]`: The name of the dashboard.</span></span>
  - <span data-ttu-id="05895-153">`[Id <String>]`：資源識別路徑</span><span class="sxs-lookup"><span data-stu-id="05895-153">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="05895-154">`[ResourceGroupName <String>]`：資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="05895-154">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="05895-155">`[SubscriptionId <String>]`：Azure 訂閱識別碼。</span><span class="sxs-lookup"><span data-stu-id="05895-155">`[SubscriptionId <String>]`: The Azure subscription ID.</span></span> <span data-ttu-id="05895-156">這是 GUID 格式的字串 (例如 00000000-0000-0000-0000-00000000000000000000000000000000000000000000000000000) </span><span class="sxs-lookup"><span data-stu-id="05895-156">This is a GUID-formatted string (e.g. 00000000-0000-0000-0000-000000000000)</span></span>

## <span data-ttu-id="05895-157">相關連結</span><span class="sxs-lookup"><span data-stu-id="05895-157">RELATED LINKS</span></span>

