---
external help file: ''
Module Name: Az.ImportExport
online version: https://docs.microsoft.com/powershell/module/az.importexport/remove-azimportexport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImportExport/help/Remove-AzImportExport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImportExport/help/Remove-AzImportExport.md
ms.openlocfilehash: c4ba805ca2f8f89fcc3ed23747f71c9efff01d47
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101908198"
---
# <span data-ttu-id="e151b-101">Remove-AzImportExport</span><span class="sxs-lookup"><span data-stu-id="e151b-101">Remove-AzImportExport</span></span>

## <span data-ttu-id="e151b-102">簡介</span><span class="sxs-lookup"><span data-stu-id="e151b-102">SYNOPSIS</span></span>
<span data-ttu-id="e151b-103">刪除現有的工作。</span><span class="sxs-lookup"><span data-stu-id="e151b-103">Deletes an existing job.</span></span>
<span data-ttu-id="e151b-104">只有建立或完成狀態中的工作可以刪除。</span><span class="sxs-lookup"><span data-stu-id="e151b-104">Only jobs in the Creating or Completed states can be deleted.</span></span>

## <span data-ttu-id="e151b-105">語法</span><span class="sxs-lookup"><span data-stu-id="e151b-105">SYNTAX</span></span>

### <span data-ttu-id="e151b-106">刪除 (預設) </span><span class="sxs-lookup"><span data-stu-id="e151b-106">Delete (Default)</span></span>
```
Remove-AzImportExport -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-AcceptLanguage <String>] [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="e151b-107">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="e151b-107">DeleteViaIdentity</span></span>
```
Remove-AzImportExport -InputObject <IImportExportIdentity> [-AcceptLanguage <String>]
 [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="e151b-108">描述</span><span class="sxs-lookup"><span data-stu-id="e151b-108">DESCRIPTION</span></span>
<span data-ttu-id="e151b-109">刪除現有的工作。</span><span class="sxs-lookup"><span data-stu-id="e151b-109">Deletes an existing job.</span></span>
<span data-ttu-id="e151b-110">只有建立或完成狀態中的工作可以刪除。</span><span class="sxs-lookup"><span data-stu-id="e151b-110">Only jobs in the Creating or Completed states can be deleted.</span></span>

## <span data-ttu-id="e151b-111">例子</span><span class="sxs-lookup"><span data-stu-id="e151b-111">EXAMPLES</span></span>

### <span data-ttu-id="e151b-112">範例 1：根據 resourceGroup 和伺服器名稱移除 ImportExport 工作</span><span class="sxs-lookup"><span data-stu-id="e151b-112">Example 1: Remove ImportExport job by resourceGroup and server name</span></span>
```powershell
PS C:\> Remove-AzImportExport -Name test-job -ResourceGroupName ImportTestRG
```

<span data-ttu-id="e151b-113">此 Cmdlet 會根據 resourceGroup 和伺服器名稱移除 ImportExport 工作。</span><span class="sxs-lookup"><span data-stu-id="e151b-113">This cmdlet removes ImportExport job by resourceGroup and server name.</span></span>

### <span data-ttu-id="e151b-114">範例 2：根據身分識別移除 ImportExport 工作</span><span class="sxs-lookup"><span data-stu-id="e151b-114">Example 2: Remove ImportExport job by identity</span></span>
```powershell
PS C:\> Get-AzImportExport -Name test-job -ResourceGroupName ImportTestRG | Remove-AzImportExport
 
```

<span data-ttu-id="e151b-115">這些 Cmdlet 會移除根據身分識別的 ImportExport 工作。</span><span class="sxs-lookup"><span data-stu-id="e151b-115">These cmdlet removes ImportExport job by identity.</span></span>

## <span data-ttu-id="e151b-116">參數</span><span class="sxs-lookup"><span data-stu-id="e151b-116">PARAMETERS</span></span>

### <span data-ttu-id="e151b-117">-AcceptLanguage</span><span class="sxs-lookup"><span data-stu-id="e151b-117">-AcceptLanguage</span></span>
<span data-ttu-id="e151b-118">指定回應的偏好語言。</span><span class="sxs-lookup"><span data-stu-id="e151b-118">Specifies the preferred language for the response.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e151b-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e151b-119">-DefaultProfile</span></span>
<span data-ttu-id="e151b-120">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="e151b-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e151b-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e151b-121">-InputObject</span></span>
<span data-ttu-id="e151b-122">身分識別參數若要建構，請參閱 INPUTOBJECT 屬性的 NOTES 區段，並建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="e151b-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ImportExport.Models.IImportExportIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e151b-123">-名稱</span><span class="sxs-lookup"><span data-stu-id="e151b-123">-Name</span></span>
<span data-ttu-id="e151b-124">匯進/匯出工作的名稱。</span><span class="sxs-lookup"><span data-stu-id="e151b-124">The name of the import/export job.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: JobName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e151b-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e151b-125">-PassThru</span></span>
<span data-ttu-id="e151b-126">命令成功時，會返回 True</span><span class="sxs-lookup"><span data-stu-id="e151b-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="e151b-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e151b-127">-ResourceGroupName</span></span>
<span data-ttu-id="e151b-128">資源組名可唯一識別使用者訂閱中的資源群組。</span><span class="sxs-lookup"><span data-stu-id="e151b-128">The resource group name uniquely identifies the resource group within the user subscription.</span></span>

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

### <span data-ttu-id="e151b-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="e151b-129">-SubscriptionId</span></span>
<span data-ttu-id="e151b-130">Azure 使用者的訂閱識別碼。</span><span class="sxs-lookup"><span data-stu-id="e151b-130">The subscription ID for the Azure user.</span></span>

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

### <span data-ttu-id="e151b-131">-確認</span><span class="sxs-lookup"><span data-stu-id="e151b-131">-Confirm</span></span>
<span data-ttu-id="e151b-132">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="e151b-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e151b-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e151b-133">-WhatIf</span></span>
<span data-ttu-id="e151b-134">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="e151b-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e151b-135">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="e151b-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e151b-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e151b-136">CommonParameters</span></span>
<span data-ttu-id="e151b-137">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="e151b-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e151b-138">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e151b-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e151b-139">輸入</span><span class="sxs-lookup"><span data-stu-id="e151b-139">INPUTS</span></span>

### <span data-ttu-id="e151b-140">Microsoft.Azure.PowerShell.Cmdlets.ImportExport.models.IImportExportIdentity</span><span class="sxs-lookup"><span data-stu-id="e151b-140">Microsoft.Azure.PowerShell.Cmdlets.ImportExport.Models.IImportExportIdentity</span></span>

## <span data-ttu-id="e151b-141">輸出</span><span class="sxs-lookup"><span data-stu-id="e151b-141">OUTPUTS</span></span>

### <span data-ttu-id="e151b-142">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="e151b-142">System.Boolean</span></span>

## <span data-ttu-id="e151b-143">筆記</span><span class="sxs-lookup"><span data-stu-id="e151b-143">NOTES</span></span>

<span data-ttu-id="e151b-144">別名</span><span class="sxs-lookup"><span data-stu-id="e151b-144">ALIASES</span></span>

<span data-ttu-id="e151b-145">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="e151b-145">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="e151b-146">若要建立下列描述的參數，請建構包含適當屬性的雜湊表。</span><span class="sxs-lookup"><span data-stu-id="e151b-146">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="e151b-147">有關雜湊表的資訊，請執行Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="e151b-147">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="e151b-148">INPUTOBJECT： <IImportExportIdentity> 身分識別參數</span><span class="sxs-lookup"><span data-stu-id="e151b-148">INPUTOBJECT <IImportExportIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="e151b-149">`[Id <String>]`：資源識別路徑</span><span class="sxs-lookup"><span data-stu-id="e151b-149">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="e151b-150">`[JobName <String>]`：匯進/匯出工作的名稱。</span><span class="sxs-lookup"><span data-stu-id="e151b-150">`[JobName <String>]`: The name of the import/export job.</span></span>
  - <span data-ttu-id="e151b-151">`[LocationName <String>]`：位置的名稱。</span><span class="sxs-lookup"><span data-stu-id="e151b-151">`[LocationName <String>]`: The name of the location.</span></span> <span data-ttu-id="e151b-152">例如，美國西部或西部。</span><span class="sxs-lookup"><span data-stu-id="e151b-152">For example, West US or westus.</span></span>
  - <span data-ttu-id="e151b-153">`[ResourceGroupName <String>]`：資源組名可唯一識別使用者訂閱中的資源群組。</span><span class="sxs-lookup"><span data-stu-id="e151b-153">`[ResourceGroupName <String>]`: The resource group name uniquely identifies the resource group within the user subscription.</span></span>
  - <span data-ttu-id="e151b-154">`[SubscriptionId <String>]`：Azure 使用者的訂閱識別碼。</span><span class="sxs-lookup"><span data-stu-id="e151b-154">`[SubscriptionId <String>]`: The subscription ID for the Azure user.</span></span>

## <span data-ttu-id="e151b-155">相關連結</span><span class="sxs-lookup"><span data-stu-id="e151b-155">RELATED LINKS</span></span>

