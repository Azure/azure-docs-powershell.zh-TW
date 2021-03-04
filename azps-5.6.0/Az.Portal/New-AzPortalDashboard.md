---
external help file: ''
Module Name: Az.Portal
online version: https://docs.microsoft.com/powershell/module/az.portal/new-azportaldashboard
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Portal/help/New-AzPortalDashboard.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Portal/help/New-AzPortalDashboard.md
ms.openlocfilehash: 05627146c0b9984ea5222f70f85f801b374e1321
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101911337"
---
# <span data-ttu-id="358a3-101">New-AzPortalDashboard</span><span class="sxs-lookup"><span data-stu-id="358a3-101">New-AzPortalDashboard</span></span>

## <span data-ttu-id="358a3-102">簡介</span><span class="sxs-lookup"><span data-stu-id="358a3-102">SYNOPSIS</span></span>
<span data-ttu-id="358a3-103">建立或更新儀表板。</span><span class="sxs-lookup"><span data-stu-id="358a3-103">Creates or updates a Dashboard.</span></span>

## <span data-ttu-id="358a3-104">語法</span><span class="sxs-lookup"><span data-stu-id="358a3-104">SYNTAX</span></span>

### <span data-ttu-id="358a3-105">CreateExpanded (預設) </span><span class="sxs-lookup"><span data-stu-id="358a3-105">CreateExpanded (Default)</span></span>
```
New-AzPortalDashboard -Name <String> -ResourceGroupName <String> -Location <String> [-SubscriptionId <String>]
 [-Lens <Hashtable>] [-Metadata <Hashtable>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="358a3-106">創建</span><span class="sxs-lookup"><span data-stu-id="358a3-106">Create</span></span>
```
New-AzPortalDashboard -Name <String> -ResourceGroupName <String> -Dashboard <IDashboard>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="358a3-107">CreateByFile</span><span class="sxs-lookup"><span data-stu-id="358a3-107">CreateByFile</span></span>
```
New-AzPortalDashboard -Name <String> -ResourceGroupName <String> -DashboardPath <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="358a3-108">描述</span><span class="sxs-lookup"><span data-stu-id="358a3-108">DESCRIPTION</span></span>
<span data-ttu-id="358a3-109">建立或更新儀表板。</span><span class="sxs-lookup"><span data-stu-id="358a3-109">Creates or updates a Dashboard.</span></span>

## <span data-ttu-id="358a3-110">例子</span><span class="sxs-lookup"><span data-stu-id="358a3-110">EXAMPLES</span></span>

### <span data-ttu-id="358a3-111">範例 1：使用儀表板範本檔案建立儀表板</span><span class="sxs-lookup"><span data-stu-id="358a3-111">Example 1: Create a dashboard using a dashboard template file</span></span>
```powershell
PS C:\> New-AzPortalDashboard -DashboardPath .\resources\dash1.json -ResourceGroupName mydash-rg -DashboardName my-dashboard03

Location Name           Type
-------- ----           ----
eastasia my-dashboard03 Microsoft.Portal/dashboards
```

<span data-ttu-id="358a3-112">使用提供的儀表板範本檔案建立新儀表板。</span><span class="sxs-lookup"><span data-stu-id="358a3-112">Create a new dashboard using the provided dashboard template file.</span></span>

## <span data-ttu-id="358a3-113">參數</span><span class="sxs-lookup"><span data-stu-id="358a3-113">PARAMETERS</span></span>

### <span data-ttu-id="358a3-114">-儀表板</span><span class="sxs-lookup"><span data-stu-id="358a3-114">-Dashboard</span></span>
<span data-ttu-id="358a3-115">共用儀表板資源定義。</span><span class="sxs-lookup"><span data-stu-id="358a3-115">The shared dashboard resource definition.</span></span>
<span data-ttu-id="358a3-116">若要建構，請參閱儀表板屬性的附注區段，並建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="358a3-116">To construct, see NOTES section for DASHBOARD properties and create a hash table.</span></span>

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

### <span data-ttu-id="358a3-117">-DashboardPath</span><span class="sxs-lookup"><span data-stu-id="358a3-117">-DashboardPath</span></span>
<span data-ttu-id="358a3-118">現有儀表板範本的路徑。</span><span class="sxs-lookup"><span data-stu-id="358a3-118">The Path to an existing dashboard template.</span></span>
<span data-ttu-id="358a3-119">儀表板範本可以從入口網站下載。</span><span class="sxs-lookup"><span data-stu-id="358a3-119">Dashboard templates may be downloaded from the portal.</span></span>

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

### <span data-ttu-id="358a3-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="358a3-120">-DefaultProfile</span></span>
<span data-ttu-id="358a3-121">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="358a3-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="358a3-122">-Lens</span><span class="sxs-lookup"><span data-stu-id="358a3-122">-Lens</span></span>
<span data-ttu-id="358a3-123">儀表板儀表板。</span><span class="sxs-lookup"><span data-stu-id="358a3-123">The dashboard lenses.</span></span>

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

### <span data-ttu-id="358a3-124">-位置</span><span class="sxs-lookup"><span data-stu-id="358a3-124">-Location</span></span>
<span data-ttu-id="358a3-125">資源位置</span><span class="sxs-lookup"><span data-stu-id="358a3-125">Resource location</span></span>

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

### <span data-ttu-id="358a3-126">-中繼資料</span><span class="sxs-lookup"><span data-stu-id="358a3-126">-Metadata</span></span>
<span data-ttu-id="358a3-127">儀表板中繼資料。</span><span class="sxs-lookup"><span data-stu-id="358a3-127">The dashboard metadata.</span></span>

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

### <span data-ttu-id="358a3-128">-名稱</span><span class="sxs-lookup"><span data-stu-id="358a3-128">-Name</span></span>
<span data-ttu-id="358a3-129">儀表板的名稱。</span><span class="sxs-lookup"><span data-stu-id="358a3-129">The name of the dashboard.</span></span>

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

### <span data-ttu-id="358a3-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="358a3-130">-ResourceGroupName</span></span>
<span data-ttu-id="358a3-131">資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="358a3-131">The name of the resource group.</span></span>

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

### <span data-ttu-id="358a3-132">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="358a3-132">-SubscriptionId</span></span>
<span data-ttu-id="358a3-133">Azure 訂閱識別碼。</span><span class="sxs-lookup"><span data-stu-id="358a3-133">The Azure subscription ID.</span></span>
<span data-ttu-id="358a3-134">這是 GUID 格式的字串 (例如 00000000-0000-0000-0000-00000000000000000000000000000000000000000000000000000) </span><span class="sxs-lookup"><span data-stu-id="358a3-134">This is a GUID-formatted string (e.g. 00000000-0000-0000-0000-000000000000)</span></span>

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

### <span data-ttu-id="358a3-135">-標記</span><span class="sxs-lookup"><span data-stu-id="358a3-135">-Tag</span></span>
<span data-ttu-id="358a3-136">資源標記</span><span class="sxs-lookup"><span data-stu-id="358a3-136">Resource tags</span></span>

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

### <span data-ttu-id="358a3-137">-確認</span><span class="sxs-lookup"><span data-stu-id="358a3-137">-Confirm</span></span>
<span data-ttu-id="358a3-138">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="358a3-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="358a3-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="358a3-139">-WhatIf</span></span>
<span data-ttu-id="358a3-140">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="358a3-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="358a3-141">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="358a3-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="358a3-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="358a3-142">CommonParameters</span></span>
<span data-ttu-id="358a3-143">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="358a3-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="358a3-144">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="358a3-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="358a3-145">輸入</span><span class="sxs-lookup"><span data-stu-id="358a3-145">INPUTS</span></span>

### <span data-ttu-id="358a3-146">Microsoft.Azure.PowerShell.Cmdlets.Portal.Models.Api201901Preview.IDashboard</span><span class="sxs-lookup"><span data-stu-id="358a3-146">Microsoft.Azure.PowerShell.Cmdlets.Portal.Models.Api201901Preview.IDashboard</span></span>

## <span data-ttu-id="358a3-147">輸出</span><span class="sxs-lookup"><span data-stu-id="358a3-147">OUTPUTS</span></span>

### <span data-ttu-id="358a3-148">Microsoft.Azure.PowerShell.Cmdlets.Portal.Models.Api201901Preview.IDashboard</span><span class="sxs-lookup"><span data-stu-id="358a3-148">Microsoft.Azure.PowerShell.Cmdlets.Portal.Models.Api201901Preview.IDashboard</span></span>

## <span data-ttu-id="358a3-149">筆記</span><span class="sxs-lookup"><span data-stu-id="358a3-149">NOTES</span></span>

<span data-ttu-id="358a3-150">別名</span><span class="sxs-lookup"><span data-stu-id="358a3-150">ALIASES</span></span>

<span data-ttu-id="358a3-151">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="358a3-151">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="358a3-152">若要建立下列描述的參數，請建構包含適當屬性的雜湊表。</span><span class="sxs-lookup"><span data-stu-id="358a3-152">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="358a3-153">有關雜湊表的資訊，請執行Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="358a3-153">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="358a3-154">儀表板 <IDashboard> ：共用儀表板資源定義。</span><span class="sxs-lookup"><span data-stu-id="358a3-154">DASHBOARD <IDashboard>: The shared dashboard resource definition.</span></span>
  - <span data-ttu-id="358a3-155">`Location <String>`：資源位置</span><span class="sxs-lookup"><span data-stu-id="358a3-155">`Location <String>`: Resource location</span></span>
  - <span data-ttu-id="358a3-156">`[Lens <IDashboardPropertiesLenses>]`：儀表板儀表板。</span><span class="sxs-lookup"><span data-stu-id="358a3-156">`[Lens <IDashboardPropertiesLenses>]`: The dashboard lenses.</span></span>
    - <span data-ttu-id="358a3-157">`[(Any) <IDashboardLens>]`：這表示任何屬性都可以新增到這個物件。</span><span class="sxs-lookup"><span data-stu-id="358a3-157">`[(Any) <IDashboardLens>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="358a3-158">`[Metadata <IDashboardPropertiesMetadata>]`：儀表板中繼資料。</span><span class="sxs-lookup"><span data-stu-id="358a3-158">`[Metadata <IDashboardPropertiesMetadata>]`: The dashboard metadata.</span></span>
    - <span data-ttu-id="358a3-159">`[(Any) <Object>]`：這表示任何屬性都可以新增到這個物件。</span><span class="sxs-lookup"><span data-stu-id="358a3-159">`[(Any) <Object>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="358a3-160">`[Tag <IDashboardTags>]`：資源標記</span><span class="sxs-lookup"><span data-stu-id="358a3-160">`[Tag <IDashboardTags>]`: Resource tags</span></span>
    - <span data-ttu-id="358a3-161">`[(Any) <String>]`：這表示任何屬性都可以新增到這個物件。</span><span class="sxs-lookup"><span data-stu-id="358a3-161">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>

## <span data-ttu-id="358a3-162">相關連結</span><span class="sxs-lookup"><span data-stu-id="358a3-162">RELATED LINKS</span></span>

