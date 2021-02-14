---
external help file: ''
Module Name: Az.Portal
online version: https://docs.microsoft.com/en-us/powershell/module/az.portal/new-azportaldashboard
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Portal/help/New-AzPortalDashboard.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Portal/help/New-AzPortalDashboard.md
ms.openlocfilehash: 80b2289b4f481fff126d9cd5dfc98ca94536cfa0
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100134735"
---
# <span data-ttu-id="a076a-101">New-AzPortalDashboard</span><span class="sxs-lookup"><span data-stu-id="a076a-101">New-AzPortalDashboard</span></span>

## <span data-ttu-id="a076a-102">摘要</span><span class="sxs-lookup"><span data-stu-id="a076a-102">SYNOPSIS</span></span>
<span data-ttu-id="a076a-103">建立或更新儀表板。</span><span class="sxs-lookup"><span data-stu-id="a076a-103">Creates or updates a Dashboard.</span></span>

## <span data-ttu-id="a076a-104">句法</span><span class="sxs-lookup"><span data-stu-id="a076a-104">SYNTAX</span></span>

### <span data-ttu-id="a076a-105">CreateExpanded (預設) </span><span class="sxs-lookup"><span data-stu-id="a076a-105">CreateExpanded (Default)</span></span>
```
New-AzPortalDashboard -Name <String> -ResourceGroupName <String> -Location <String> [-SubscriptionId <String>]
 [-Lens <Hashtable>] [-Metadata <Hashtable>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="a076a-106">建立</span><span class="sxs-lookup"><span data-stu-id="a076a-106">Create</span></span>
```
New-AzPortalDashboard -Name <String> -ResourceGroupName <String> -Dashboard <IDashboard>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="a076a-107">CreateByFile</span><span class="sxs-lookup"><span data-stu-id="a076a-107">CreateByFile</span></span>
```
New-AzPortalDashboard -Name <String> -ResourceGroupName <String> -DashboardPath <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="a076a-108">說明</span><span class="sxs-lookup"><span data-stu-id="a076a-108">DESCRIPTION</span></span>
<span data-ttu-id="a076a-109">建立或更新儀表板。</span><span class="sxs-lookup"><span data-stu-id="a076a-109">Creates or updates a Dashboard.</span></span>

## <span data-ttu-id="a076a-110">示例</span><span class="sxs-lookup"><span data-stu-id="a076a-110">EXAMPLES</span></span>

### <span data-ttu-id="a076a-111">範例1：使用儀表板範本檔建立儀表板</span><span class="sxs-lookup"><span data-stu-id="a076a-111">Example 1: Create a dashboard using a dashboard template file</span></span>
```powershell
PS C:\> New-AzPortalDashboard -DashboardPath .\resources\dash1.json -ResourceGroupName mydash-rg -DashboardName my-dashboard03

Location Name           Type
-------- ----           ----
eastasia my-dashboard03 Microsoft.Portal/dashboards
```

<span data-ttu-id="a076a-112">使用提供的儀表板範本檔案建立新的儀表板。</span><span class="sxs-lookup"><span data-stu-id="a076a-112">Create a new dashboard using the provided dashboard template file.</span></span>

## <span data-ttu-id="a076a-113">參數</span><span class="sxs-lookup"><span data-stu-id="a076a-113">PARAMETERS</span></span>

### <span data-ttu-id="a076a-114">-儀表板</span><span class="sxs-lookup"><span data-stu-id="a076a-114">-Dashboard</span></span>
<span data-ttu-id="a076a-115">共用儀表板資源定義。</span><span class="sxs-lookup"><span data-stu-id="a076a-115">The shared dashboard resource definition.</span></span>
<span data-ttu-id="a076a-116">若要建立，請參閱儀表板屬性的 [記事] 區段，然後建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="a076a-116">To construct, see NOTES section for DASHBOARD properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Portal.Models.Api201901Preview.IDashboard
Parameter Sets: Create
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a076a-117">-DashboardPath</span><span class="sxs-lookup"><span data-stu-id="a076a-117">-DashboardPath</span></span>
<span data-ttu-id="a076a-118">現有儀表板範本的路徑。</span><span class="sxs-lookup"><span data-stu-id="a076a-118">The Path to an existing dashboard template.</span></span>
<span data-ttu-id="a076a-119">儀表板範本可能會從入口網站下載。</span><span class="sxs-lookup"><span data-stu-id="a076a-119">Dashboard templates may be downloaded from the portal.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateByFile
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a076a-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a076a-120">-DefaultProfile</span></span>
<span data-ttu-id="a076a-121">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="a076a-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a076a-122">-透鏡</span><span class="sxs-lookup"><span data-stu-id="a076a-122">-Lens</span></span>
<span data-ttu-id="a076a-123">儀表板鏡頭。</span><span class="sxs-lookup"><span data-stu-id="a076a-123">The dashboard lenses.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a076a-124">-位置</span><span class="sxs-lookup"><span data-stu-id="a076a-124">-Location</span></span>
<span data-ttu-id="a076a-125">資源位置</span><span class="sxs-lookup"><span data-stu-id="a076a-125">Resource location</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a076a-126">-中繼資料</span><span class="sxs-lookup"><span data-stu-id="a076a-126">-Metadata</span></span>
<span data-ttu-id="a076a-127">儀表板中繼資料。</span><span class="sxs-lookup"><span data-stu-id="a076a-127">The dashboard metadata.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a076a-128">-名稱</span><span class="sxs-lookup"><span data-stu-id="a076a-128">-Name</span></span>
<span data-ttu-id="a076a-129">儀表板的名稱。</span><span class="sxs-lookup"><span data-stu-id="a076a-129">The name of the dashboard.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: DashboardName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a076a-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a076a-130">-ResourceGroupName</span></span>
<span data-ttu-id="a076a-131">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="a076a-131">The name of the resource group.</span></span>

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

### <span data-ttu-id="a076a-132">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="a076a-132">-SubscriptionId</span></span>
<span data-ttu-id="a076a-133">Azure 訂閱 ID。</span><span class="sxs-lookup"><span data-stu-id="a076a-133">The Azure subscription ID.</span></span>
<span data-ttu-id="a076a-134">這是 GUID 格式的字串 (例如 00000000-0000-0000-0000-000000000000) </span><span class="sxs-lookup"><span data-stu-id="a076a-134">This is a GUID-formatted string (e.g. 00000000-0000-0000-0000-000000000000)</span></span>

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

### <span data-ttu-id="a076a-135">-Tag</span><span class="sxs-lookup"><span data-stu-id="a076a-135">-Tag</span></span>
<span data-ttu-id="a076a-136">資源標記</span><span class="sxs-lookup"><span data-stu-id="a076a-136">Resource tags</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a076a-137">-確認</span><span class="sxs-lookup"><span data-stu-id="a076a-137">-Confirm</span></span>
<span data-ttu-id="a076a-138">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="a076a-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a076a-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a076a-139">-WhatIf</span></span>
<span data-ttu-id="a076a-140">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="a076a-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a076a-141">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="a076a-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a076a-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a076a-142">CommonParameters</span></span>
<span data-ttu-id="a076a-143">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="a076a-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a076a-144">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="a076a-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a076a-145">輸入</span><span class="sxs-lookup"><span data-stu-id="a076a-145">INPUTS</span></span>

### <span data-ttu-id="a076a-146">[Api201901Preview. IDashboard] （）</span><span class="sxs-lookup"><span data-stu-id="a076a-146">Microsoft.Azure.PowerShell.Cmdlets.Portal.Models.Api201901Preview.IDashboard</span></span>

## <span data-ttu-id="a076a-147">輸出</span><span class="sxs-lookup"><span data-stu-id="a076a-147">OUTPUTS</span></span>

### <span data-ttu-id="a076a-148">[Api201901Preview. IDashboard] （）</span><span class="sxs-lookup"><span data-stu-id="a076a-148">Microsoft.Azure.PowerShell.Cmdlets.Portal.Models.Api201901Preview.IDashboard</span></span>

## <span data-ttu-id="a076a-149">筆記</span><span class="sxs-lookup"><span data-stu-id="a076a-149">NOTES</span></span>

<span data-ttu-id="a076a-150">別名</span><span class="sxs-lookup"><span data-stu-id="a076a-150">ALIASES</span></span>

<span data-ttu-id="a076a-151">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="a076a-151">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="a076a-152">若要建立如下所述的參數，請構造包含適當屬性的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="a076a-152">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="a076a-153">如需雜湊資料表的詳細資訊，請執行 Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="a076a-153">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="a076a-154">儀表板 <IDashboard> ：共用的儀表板資源定義。</span><span class="sxs-lookup"><span data-stu-id="a076a-154">DASHBOARD <IDashboard>: The shared dashboard resource definition.</span></span>
  - <span data-ttu-id="a076a-155">`Location <String>`：資源位置</span><span class="sxs-lookup"><span data-stu-id="a076a-155">`Location <String>`: Resource location</span></span>
  - <span data-ttu-id="a076a-156">`[Lens <IDashboardPropertiesLenses>]`：儀表板鏡頭。</span><span class="sxs-lookup"><span data-stu-id="a076a-156">`[Lens <IDashboardPropertiesLenses>]`: The dashboard lenses.</span></span>
    - <span data-ttu-id="a076a-157">`[(Any) <IDashboardLens>]`：這表示您可以將任何屬性新增至此物件。</span><span class="sxs-lookup"><span data-stu-id="a076a-157">`[(Any) <IDashboardLens>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="a076a-158">`[Metadata <IDashboardPropertiesMetadata>]`：儀表板中繼資料。</span><span class="sxs-lookup"><span data-stu-id="a076a-158">`[Metadata <IDashboardPropertiesMetadata>]`: The dashboard metadata.</span></span>
    - <span data-ttu-id="a076a-159">`[(Any) <Object>]`：這表示您可以將任何屬性新增至此物件。</span><span class="sxs-lookup"><span data-stu-id="a076a-159">`[(Any) <Object>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="a076a-160">`[Tag <IDashboardTags>]`：資源標記</span><span class="sxs-lookup"><span data-stu-id="a076a-160">`[Tag <IDashboardTags>]`: Resource tags</span></span>
    - <span data-ttu-id="a076a-161">`[(Any) <String>]`：這表示您可以將任何屬性新增至此物件。</span><span class="sxs-lookup"><span data-stu-id="a076a-161">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>

## <span data-ttu-id="a076a-162">相關連結</span><span class="sxs-lookup"><span data-stu-id="a076a-162">RELATED LINKS</span></span>

