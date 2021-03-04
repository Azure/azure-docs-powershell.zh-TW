---
external help file: ''
Module Name: Az.Portal
online version: https://docs.microsoft.com/powershell/module/az.portal/remove-azportaldashboard
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Portal/help/Remove-AzPortalDashboard.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Portal/help/Remove-AzPortalDashboard.md
ms.openlocfilehash: 5422b416d7fc6bf16625625a991e17d65061339e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101911330"
---
# <span data-ttu-id="c8600-101">Remove-AzPortalDashboard</span><span class="sxs-lookup"><span data-stu-id="c8600-101">Remove-AzPortalDashboard</span></span>

## <span data-ttu-id="c8600-102">簡介</span><span class="sxs-lookup"><span data-stu-id="c8600-102">SYNOPSIS</span></span>
<span data-ttu-id="c8600-103">刪除儀表板。</span><span class="sxs-lookup"><span data-stu-id="c8600-103">Deletes the Dashboard.</span></span>

## <span data-ttu-id="c8600-104">語法</span><span class="sxs-lookup"><span data-stu-id="c8600-104">SYNTAX</span></span>

### <span data-ttu-id="c8600-105">刪除 (預設) </span><span class="sxs-lookup"><span data-stu-id="c8600-105">Delete (Default)</span></span>
```
Remove-AzPortalDashboard -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="c8600-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="c8600-106">DeleteViaIdentity</span></span>
```
Remove-AzPortalDashboard -InputObject <IPortalIdentity> [-DefaultProfile <PSObject>] [-PassThru] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="c8600-107">描述</span><span class="sxs-lookup"><span data-stu-id="c8600-107">DESCRIPTION</span></span>
<span data-ttu-id="c8600-108">刪除儀表板。</span><span class="sxs-lookup"><span data-stu-id="c8600-108">Deletes the Dashboard.</span></span>

## <span data-ttu-id="c8600-109">例子</span><span class="sxs-lookup"><span data-stu-id="c8600-109">EXAMPLES</span></span>

### <span data-ttu-id="c8600-110">範例 1：移除儀表板</span><span class="sxs-lookup"><span data-stu-id="c8600-110">Example 1: Remove a Dashboard</span></span>
```powershell
PS C:\td\> Remove-AzPortalDashboard -ResourceGroupName my-rg -DashboardName dashbase02
```

<span data-ttu-id="c8600-111">使用資源組名和儀表板名稱移除虛線。</span><span class="sxs-lookup"><span data-stu-id="c8600-111">Remove a Dashbaord using resource group name and dashboard name.</span></span>

### <span data-ttu-id="c8600-112">範例 2：使用管線移除儀表板</span><span class="sxs-lookup"><span data-stu-id="c8600-112">Example 2: Remove a Dashboard using the pipeline</span></span>
```powershell
PS C:\> Get-AzPortalDashboard -ResourceGroupName my-rg -DashboardName dashbase02 | Remove-AzPortalDashboard
```

<span data-ttu-id="c8600-113">移除從通話中Get-AzDashboard儀表板。</span><span class="sxs-lookup"><span data-stu-id="c8600-113">Remove the dashboard returned from a Get-AzDashboard call.</span></span>

## <span data-ttu-id="c8600-114">參數</span><span class="sxs-lookup"><span data-stu-id="c8600-114">PARAMETERS</span></span>

### <span data-ttu-id="c8600-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c8600-115">-DefaultProfile</span></span>
<span data-ttu-id="c8600-116">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="c8600-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c8600-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c8600-117">-InputObject</span></span>
<span data-ttu-id="c8600-118">身分識別參數若要建構，請參閱 INPUTOBJECT 屬性的 NOTES 區段，並建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="c8600-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="c8600-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="c8600-119">-Name</span></span>
<span data-ttu-id="c8600-120">儀表板的名稱。</span><span class="sxs-lookup"><span data-stu-id="c8600-120">The name of the dashboard.</span></span>

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

### <span data-ttu-id="c8600-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c8600-121">-PassThru</span></span>
<span data-ttu-id="c8600-122">命令成功時，會返回 True</span><span class="sxs-lookup"><span data-stu-id="c8600-122">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="c8600-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c8600-123">-ResourceGroupName</span></span>
<span data-ttu-id="c8600-124">資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="c8600-124">The name of the resource group.</span></span>

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

### <span data-ttu-id="c8600-125">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="c8600-125">-SubscriptionId</span></span>
<span data-ttu-id="c8600-126">Azure 訂閱識別碼。</span><span class="sxs-lookup"><span data-stu-id="c8600-126">The Azure subscription ID.</span></span>
<span data-ttu-id="c8600-127">這是 GUID 格式的字串 (例如 00000000-0000-0000-0000-00000000000000000000000000000000000000000000000000000) </span><span class="sxs-lookup"><span data-stu-id="c8600-127">This is a GUID-formatted string (e.g. 00000000-0000-0000-0000-000000000000)</span></span>

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

### <span data-ttu-id="c8600-128">-確認</span><span class="sxs-lookup"><span data-stu-id="c8600-128">-Confirm</span></span>
<span data-ttu-id="c8600-129">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="c8600-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c8600-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c8600-130">-WhatIf</span></span>
<span data-ttu-id="c8600-131">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="c8600-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c8600-132">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="c8600-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c8600-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c8600-133">CommonParameters</span></span>
<span data-ttu-id="c8600-134">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="c8600-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c8600-135">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c8600-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c8600-136">輸入</span><span class="sxs-lookup"><span data-stu-id="c8600-136">INPUTS</span></span>

### <span data-ttu-id="c8600-137">Microsoft.Azure.PowerShell.Cmdlets.Portal.models.IPortalIdentity</span><span class="sxs-lookup"><span data-stu-id="c8600-137">Microsoft.Azure.PowerShell.Cmdlets.Portal.Models.IPortalIdentity</span></span>

## <span data-ttu-id="c8600-138">輸出</span><span class="sxs-lookup"><span data-stu-id="c8600-138">OUTPUTS</span></span>

### <span data-ttu-id="c8600-139">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="c8600-139">System.Boolean</span></span>

## <span data-ttu-id="c8600-140">筆記</span><span class="sxs-lookup"><span data-stu-id="c8600-140">NOTES</span></span>

<span data-ttu-id="c8600-141">別名</span><span class="sxs-lookup"><span data-stu-id="c8600-141">ALIASES</span></span>

<span data-ttu-id="c8600-142">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="c8600-142">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="c8600-143">若要建立下列描述的參數，請建構包含適當屬性的雜湊表。</span><span class="sxs-lookup"><span data-stu-id="c8600-143">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="c8600-144">有關雜湊表的資訊，請執行Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="c8600-144">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="c8600-145">INPUTOBJECT： <IPortalIdentity> 身分識別參數</span><span class="sxs-lookup"><span data-stu-id="c8600-145">INPUTOBJECT <IPortalIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="c8600-146">`[DashboardName <String>]`：儀表板的名稱。</span><span class="sxs-lookup"><span data-stu-id="c8600-146">`[DashboardName <String>]`: The name of the dashboard.</span></span>
  - <span data-ttu-id="c8600-147">`[Id <String>]`：資源識別路徑</span><span class="sxs-lookup"><span data-stu-id="c8600-147">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="c8600-148">`[ResourceGroupName <String>]`：資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="c8600-148">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="c8600-149">`[SubscriptionId <String>]`：Azure 訂閱識別碼。</span><span class="sxs-lookup"><span data-stu-id="c8600-149">`[SubscriptionId <String>]`: The Azure subscription ID.</span></span> <span data-ttu-id="c8600-150">這是 GUID 格式的字串 (例如 00000000-0000-0000-0000-00000000000000000000000000000000000000000000000000000) </span><span class="sxs-lookup"><span data-stu-id="c8600-150">This is a GUID-formatted string (e.g. 00000000-0000-0000-0000-000000000000)</span></span>

## <span data-ttu-id="c8600-151">相關連結</span><span class="sxs-lookup"><span data-stu-id="c8600-151">RELATED LINKS</span></span>

