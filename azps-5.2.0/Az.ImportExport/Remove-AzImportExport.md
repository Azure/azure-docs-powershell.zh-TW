---
external help file: ''
Module Name: Az.ImportExport
online version: https://docs.microsoft.com/en-us/powershell/module/az.importexport/remove-azimportexport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImportExport/help/Remove-AzImportExport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImportExport/help/Remove-AzImportExport.md
ms.openlocfilehash: 0f78f68c9d5557b97366185b354823400eada97c
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98282727"
---
# <span data-ttu-id="3ca8d-101">Remove-AzImportExport</span><span class="sxs-lookup"><span data-stu-id="3ca8d-101">Remove-AzImportExport</span></span>

## <span data-ttu-id="3ca8d-102">摘要</span><span class="sxs-lookup"><span data-stu-id="3ca8d-102">SYNOPSIS</span></span>
<span data-ttu-id="3ca8d-103">刪除現有的工作。</span><span class="sxs-lookup"><span data-stu-id="3ca8d-103">Deletes an existing job.</span></span>
<span data-ttu-id="3ca8d-104">只有 [建立] 或 [已完成] 狀態中的工作可以刪除。</span><span class="sxs-lookup"><span data-stu-id="3ca8d-104">Only jobs in the Creating or Completed states can be deleted.</span></span>

## <span data-ttu-id="3ca8d-105">句法</span><span class="sxs-lookup"><span data-stu-id="3ca8d-105">SYNTAX</span></span>

### <span data-ttu-id="3ca8d-106">刪除 (預設) </span><span class="sxs-lookup"><span data-stu-id="3ca8d-106">Delete (Default)</span></span>
```
Remove-AzImportExport -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-AcceptLanguage <String>] [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="3ca8d-107">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="3ca8d-107">DeleteViaIdentity</span></span>
```
Remove-AzImportExport -InputObject <IImportExportIdentity> [-AcceptLanguage <String>]
 [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="3ca8d-108">說明</span><span class="sxs-lookup"><span data-stu-id="3ca8d-108">DESCRIPTION</span></span>
<span data-ttu-id="3ca8d-109">刪除現有的工作。</span><span class="sxs-lookup"><span data-stu-id="3ca8d-109">Deletes an existing job.</span></span>
<span data-ttu-id="3ca8d-110">只有 [建立] 或 [已完成] 狀態中的工作可以刪除。</span><span class="sxs-lookup"><span data-stu-id="3ca8d-110">Only jobs in the Creating or Completed states can be deleted.</span></span>

## <span data-ttu-id="3ca8d-111">示例</span><span class="sxs-lookup"><span data-stu-id="3ca8d-111">EXAMPLES</span></span>

### <span data-ttu-id="3ca8d-112">範例1：依 resourceGroup 和伺服器名稱移除 ImportExport 工作</span><span class="sxs-lookup"><span data-stu-id="3ca8d-112">Example 1: Remove ImportExport job by resourceGroup and server name</span></span>
```powershell
PS C:\> Remove-AzImportExport -Name test-job -ResourceGroupName ImportTestRG
```

<span data-ttu-id="3ca8d-113">這個 Cmdlet 會依 resourceGroup 和伺服器名稱來移除 ImportExport 工作。</span><span class="sxs-lookup"><span data-stu-id="3ca8d-113">This cmdlet removes ImportExport job by resourceGroup and server name.</span></span>

### <span data-ttu-id="3ca8d-114">範例2：依身分識別移除 ImportExport 工作</span><span class="sxs-lookup"><span data-stu-id="3ca8d-114">Example 2: Remove ImportExport job by identity</span></span>
```powershell
PS C:\> Get-AzImportExport -Name test-job -ResourceGroupName ImportTestRG | Remove-AzImportExport
 
```

<span data-ttu-id="3ca8d-115">這些 Cmdlet 會依身分識別來移除 ImportExport 工作。</span><span class="sxs-lookup"><span data-stu-id="3ca8d-115">These cmdlet removes ImportExport job by identity.</span></span>

## <span data-ttu-id="3ca8d-116">參數</span><span class="sxs-lookup"><span data-stu-id="3ca8d-116">PARAMETERS</span></span>

### <span data-ttu-id="3ca8d-117">-AcceptLanguage</span><span class="sxs-lookup"><span data-stu-id="3ca8d-117">-AcceptLanguage</span></span>
<span data-ttu-id="3ca8d-118">指定回應的喜好語言。</span><span class="sxs-lookup"><span data-stu-id="3ca8d-118">Specifies the preferred language for the response.</span></span>

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

### <span data-ttu-id="3ca8d-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3ca8d-119">-DefaultProfile</span></span>
<span data-ttu-id="3ca8d-120">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="3ca8d-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3ca8d-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3ca8d-121">-InputObject</span></span>
<span data-ttu-id="3ca8d-122">要構造的身分識別參數，請參閱 INPUTOBJECT 屬性的 [記事] 區段，然後建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="3ca8d-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="3ca8d-123">-名稱</span><span class="sxs-lookup"><span data-stu-id="3ca8d-123">-Name</span></span>
<span data-ttu-id="3ca8d-124">匯入/匯出作業的名稱。</span><span class="sxs-lookup"><span data-stu-id="3ca8d-124">The name of the import/export job.</span></span>

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

### <span data-ttu-id="3ca8d-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3ca8d-125">-PassThru</span></span>
<span data-ttu-id="3ca8d-126">在命令成功時傳回 true</span><span class="sxs-lookup"><span data-stu-id="3ca8d-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="3ca8d-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3ca8d-127">-ResourceGroupName</span></span>
<span data-ttu-id="3ca8d-128">資源群組名稱會唯一識別使用者訂閱中的資源群組。</span><span class="sxs-lookup"><span data-stu-id="3ca8d-128">The resource group name uniquely identifies the resource group within the user subscription.</span></span>

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

### <span data-ttu-id="3ca8d-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="3ca8d-129">-SubscriptionId</span></span>
<span data-ttu-id="3ca8d-130">Azure 使用者的訂閱 ID。</span><span class="sxs-lookup"><span data-stu-id="3ca8d-130">The subscription ID for the Azure user.</span></span>

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

### <span data-ttu-id="3ca8d-131">-確認</span><span class="sxs-lookup"><span data-stu-id="3ca8d-131">-Confirm</span></span>
<span data-ttu-id="3ca8d-132">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="3ca8d-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3ca8d-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3ca8d-133">-WhatIf</span></span>
<span data-ttu-id="3ca8d-134">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="3ca8d-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3ca8d-135">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="3ca8d-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3ca8d-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3ca8d-136">CommonParameters</span></span>
<span data-ttu-id="3ca8d-137">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="3ca8d-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3ca8d-138">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="3ca8d-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3ca8d-139">輸入</span><span class="sxs-lookup"><span data-stu-id="3ca8d-139">INPUTS</span></span>

### <span data-ttu-id="3ca8d-140">IImportExportIdentity （ImportExport）的</span><span class="sxs-lookup"><span data-stu-id="3ca8d-140">Microsoft.Azure.PowerShell.Cmdlets.ImportExport.Models.IImportExportIdentity</span></span>

## <span data-ttu-id="3ca8d-141">輸出</span><span class="sxs-lookup"><span data-stu-id="3ca8d-141">OUTPUTS</span></span>

### <span data-ttu-id="3ca8d-142">System.object</span><span class="sxs-lookup"><span data-stu-id="3ca8d-142">System.Boolean</span></span>

## <span data-ttu-id="3ca8d-143">筆記</span><span class="sxs-lookup"><span data-stu-id="3ca8d-143">NOTES</span></span>

<span data-ttu-id="3ca8d-144">別名</span><span class="sxs-lookup"><span data-stu-id="3ca8d-144">ALIASES</span></span>

<span data-ttu-id="3ca8d-145">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="3ca8d-145">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="3ca8d-146">若要建立如下所述的參數，請構造包含適當屬性的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="3ca8d-146">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="3ca8d-147">如需雜湊資料表的詳細資訊，請執行 Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="3ca8d-147">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="3ca8d-148">INPUTOBJECT <IImportExportIdentity> ：身分識別參數</span><span class="sxs-lookup"><span data-stu-id="3ca8d-148">INPUTOBJECT <IImportExportIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="3ca8d-149">`[Id <String>]`：資源身分識別路徑</span><span class="sxs-lookup"><span data-stu-id="3ca8d-149">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="3ca8d-150">`[JobName <String>]`：匯入/匯出作業的名稱。</span><span class="sxs-lookup"><span data-stu-id="3ca8d-150">`[JobName <String>]`: The name of the import/export job.</span></span>
  - <span data-ttu-id="3ca8d-151">`[LocationName <String>]`：位置的名稱。</span><span class="sxs-lookup"><span data-stu-id="3ca8d-151">`[LocationName <String>]`: The name of the location.</span></span> <span data-ttu-id="3ca8d-152">例如，美國西部或 westus。</span><span class="sxs-lookup"><span data-stu-id="3ca8d-152">For example, West US or westus.</span></span>
  - <span data-ttu-id="3ca8d-153">`[ResourceGroupName <String>]`：資源群組名稱會唯一識別使用者訂閱中的資源群組。</span><span class="sxs-lookup"><span data-stu-id="3ca8d-153">`[ResourceGroupName <String>]`: The resource group name uniquely identifies the resource group within the user subscription.</span></span>
  - <span data-ttu-id="3ca8d-154">`[SubscriptionId <String>]`： Azure 使用者的訂閱 ID。</span><span class="sxs-lookup"><span data-stu-id="3ca8d-154">`[SubscriptionId <String>]`: The subscription ID for the Azure user.</span></span>

## <span data-ttu-id="3ca8d-155">相關連結</span><span class="sxs-lookup"><span data-stu-id="3ca8d-155">RELATED LINKS</span></span>

