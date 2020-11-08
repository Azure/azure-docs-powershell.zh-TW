---
external help file: ''
Module Name: Az.Portal
online version: https://docs.microsoft.com/en-us/powershell/module/az.portal/remove-azportaldashboard
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Portal/help/Remove-AzPortalDashboard.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Portal/help/Remove-AzPortalDashboard.md
ms.openlocfilehash: f0ef681f09caf43ac2f2100d1a30af19b1b3c364
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94135725"
---
# <span data-ttu-id="fa6b8-101">Remove-AzPortalDashboard</span><span class="sxs-lookup"><span data-stu-id="fa6b8-101">Remove-AzPortalDashboard</span></span>

## <span data-ttu-id="fa6b8-102">摘要</span><span class="sxs-lookup"><span data-stu-id="fa6b8-102">SYNOPSIS</span></span>
<span data-ttu-id="fa6b8-103">刪除儀表板。</span><span class="sxs-lookup"><span data-stu-id="fa6b8-103">Deletes the Dashboard.</span></span>

## <span data-ttu-id="fa6b8-104">句法</span><span class="sxs-lookup"><span data-stu-id="fa6b8-104">SYNTAX</span></span>

### <span data-ttu-id="fa6b8-105">刪除 (預設) </span><span class="sxs-lookup"><span data-stu-id="fa6b8-105">Delete (Default)</span></span>
```
Remove-AzPortalDashboard -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="fa6b8-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="fa6b8-106">DeleteViaIdentity</span></span>
```
Remove-AzPortalDashboard -InputObject <IPortalIdentity> [-DefaultProfile <PSObject>] [-PassThru] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="fa6b8-107">說明</span><span class="sxs-lookup"><span data-stu-id="fa6b8-107">DESCRIPTION</span></span>
<span data-ttu-id="fa6b8-108">刪除儀表板。</span><span class="sxs-lookup"><span data-stu-id="fa6b8-108">Deletes the Dashboard.</span></span>

## <span data-ttu-id="fa6b8-109">示例</span><span class="sxs-lookup"><span data-stu-id="fa6b8-109">EXAMPLES</span></span>

### <span data-ttu-id="fa6b8-110">範例1：移除儀表板</span><span class="sxs-lookup"><span data-stu-id="fa6b8-110">Example 1: Remove a Dashboard</span></span>
```powershell
PS C:\td\> Remove-AzPortalDashboard -ResourceGroupName my-rg -DashboardName dashbase02
```

<span data-ttu-id="fa6b8-111">使用資源組名稱和儀表板名稱來移除 Dashbaord。</span><span class="sxs-lookup"><span data-stu-id="fa6b8-111">Remove a Dashbaord using resource group name and dashboard name.</span></span>

### <span data-ttu-id="fa6b8-112">範例2：使用管線移除儀表板</span><span class="sxs-lookup"><span data-stu-id="fa6b8-112">Example 2: Remove a Dashboard using the pipeline</span></span>
```powershell
PS C:\> Get-AzPortalDashboard -ResourceGroupName my-rg -DashboardName dashbase02 | Remove-AzPortalDashboard
```

<span data-ttu-id="fa6b8-113">移除從 Get-AzDashboard 通話中傳回的儀表板。</span><span class="sxs-lookup"><span data-stu-id="fa6b8-113">Remove the dashboard returned from a Get-AzDashboard call.</span></span>

## <span data-ttu-id="fa6b8-114">參數</span><span class="sxs-lookup"><span data-stu-id="fa6b8-114">PARAMETERS</span></span>

### <span data-ttu-id="fa6b8-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fa6b8-115">-DefaultProfile</span></span>
<span data-ttu-id="fa6b8-116">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="fa6b8-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fa6b8-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fa6b8-117">-InputObject</span></span>
<span data-ttu-id="fa6b8-118">要構造的身分識別參數，請參閱 INPUTOBJECT 屬性的 [記事] 區段，然後建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="fa6b8-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Portal.Models.IPortalIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fa6b8-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="fa6b8-119">-Name</span></span>
<span data-ttu-id="fa6b8-120">儀表板的名稱。</span><span class="sxs-lookup"><span data-stu-id="fa6b8-120">The name of the dashboard.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: DashboardName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fa6b8-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="fa6b8-121">-PassThru</span></span>
<span data-ttu-id="fa6b8-122">在命令成功時傳回 true</span><span class="sxs-lookup"><span data-stu-id="fa6b8-122">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="fa6b8-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fa6b8-123">-ResourceGroupName</span></span>
<span data-ttu-id="fa6b8-124">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="fa6b8-124">The name of the resource group.</span></span>

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

### <span data-ttu-id="fa6b8-125">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="fa6b8-125">-SubscriptionId</span></span>
<span data-ttu-id="fa6b8-126">Azure 訂閱 ID。</span><span class="sxs-lookup"><span data-stu-id="fa6b8-126">The Azure subscription ID.</span></span>
<span data-ttu-id="fa6b8-127">這是 GUID 格式的字串 (例如 00000000-0000-0000-0000-000000000000) </span><span class="sxs-lookup"><span data-stu-id="fa6b8-127">This is a GUID-formatted string (e.g. 00000000-0000-0000-0000-000000000000)</span></span>

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

### <span data-ttu-id="fa6b8-128">-確認</span><span class="sxs-lookup"><span data-stu-id="fa6b8-128">-Confirm</span></span>
<span data-ttu-id="fa6b8-129">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="fa6b8-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fa6b8-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fa6b8-130">-WhatIf</span></span>
<span data-ttu-id="fa6b8-131">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="fa6b8-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fa6b8-132">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="fa6b8-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fa6b8-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fa6b8-133">CommonParameters</span></span>
<span data-ttu-id="fa6b8-134">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="fa6b8-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fa6b8-135">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="fa6b8-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fa6b8-136">輸入</span><span class="sxs-lookup"><span data-stu-id="fa6b8-136">INPUTS</span></span>

### <span data-ttu-id="fa6b8-137">IPortalIdentity 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="fa6b8-137">Microsoft.Azure.PowerShell.Cmdlets.Portal.Models.IPortalIdentity</span></span>

## <span data-ttu-id="fa6b8-138">輸出</span><span class="sxs-lookup"><span data-stu-id="fa6b8-138">OUTPUTS</span></span>

### <span data-ttu-id="fa6b8-139">System.object</span><span class="sxs-lookup"><span data-stu-id="fa6b8-139">System.Boolean</span></span>

## <span data-ttu-id="fa6b8-140">筆記</span><span class="sxs-lookup"><span data-stu-id="fa6b8-140">NOTES</span></span>

<span data-ttu-id="fa6b8-141">別名</span><span class="sxs-lookup"><span data-stu-id="fa6b8-141">ALIASES</span></span>

<span data-ttu-id="fa6b8-142">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="fa6b8-142">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="fa6b8-143">若要建立如下所述的參數，請構造包含適當屬性的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="fa6b8-143">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="fa6b8-144">如需雜湊資料表的詳細資訊，請執行 Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="fa6b8-144">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="fa6b8-145">INPUTOBJECT <IPortalIdentity> ：身分識別參數</span><span class="sxs-lookup"><span data-stu-id="fa6b8-145">INPUTOBJECT <IPortalIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="fa6b8-146">`[DashboardName <String>]`：儀表板的名稱。</span><span class="sxs-lookup"><span data-stu-id="fa6b8-146">`[DashboardName <String>]`: The name of the dashboard.</span></span>
  - <span data-ttu-id="fa6b8-147">`[Id <String>]`：資源身分識別路徑</span><span class="sxs-lookup"><span data-stu-id="fa6b8-147">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="fa6b8-148">`[ResourceGroupName <String>]`：資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="fa6b8-148">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="fa6b8-149">`[SubscriptionId <String>]`： Azure 訂閱 ID。</span><span class="sxs-lookup"><span data-stu-id="fa6b8-149">`[SubscriptionId <String>]`: The Azure subscription ID.</span></span> <span data-ttu-id="fa6b8-150">這是 GUID 格式的字串 (例如 00000000-0000-0000-0000-000000000000) </span><span class="sxs-lookup"><span data-stu-id="fa6b8-150">This is a GUID-formatted string (e.g. 00000000-0000-0000-0000-000000000000)</span></span>

## <span data-ttu-id="fa6b8-151">相關連結</span><span class="sxs-lookup"><span data-stu-id="fa6b8-151">RELATED LINKS</span></span>

