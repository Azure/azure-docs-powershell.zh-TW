---
external help file: ''
Module Name: Az.ImportExport
online version: https://docs.microsoft.com/en-us/powershell/module/az.importexport/get-azimportexport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImportExport/help/Get-AzImportExport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImportExport/help/Get-AzImportExport.md
ms.openlocfilehash: 13c5a7104c0b9d2d4e11e4fe0a2da772ee271c4c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94139248"
---
# <span data-ttu-id="3d05c-101">Get-AzImportExport</span><span class="sxs-lookup"><span data-stu-id="3d05c-101">Get-AzImportExport</span></span>

## <span data-ttu-id="3d05c-102">摘要</span><span class="sxs-lookup"><span data-stu-id="3d05c-102">SYNOPSIS</span></span>
<span data-ttu-id="3d05c-103">取得現有作業的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="3d05c-103">Gets information about an existing job.</span></span>

## <span data-ttu-id="3d05c-104">句法</span><span class="sxs-lookup"><span data-stu-id="3d05c-104">SYNTAX</span></span>

### <span data-ttu-id="3d05c-105"> (預設) 清單</span><span class="sxs-lookup"><span data-stu-id="3d05c-105">List (Default)</span></span>
```
Get-AzImportExport [-SubscriptionId <String[]>] [-Filter <String>] [-Top <Int32>] [-AcceptLanguage <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="3d05c-106">獲取</span><span class="sxs-lookup"><span data-stu-id="3d05c-106">Get</span></span>
```
Get-AzImportExport -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-AcceptLanguage <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="3d05c-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="3d05c-107">GetViaIdentity</span></span>
```
Get-AzImportExport -InputObject <IImportExportIdentity> [-AcceptLanguage <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="3d05c-108">List1</span><span class="sxs-lookup"><span data-stu-id="3d05c-108">List1</span></span>
```
Get-AzImportExport -ResourceGroupName <String> [-SubscriptionId <String[]>] [-Filter <String>] [-Top <Int32>]
 [-AcceptLanguage <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="3d05c-109">說明</span><span class="sxs-lookup"><span data-stu-id="3d05c-109">DESCRIPTION</span></span>
<span data-ttu-id="3d05c-110">取得現有作業的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="3d05c-110">Gets information about an existing job.</span></span>

## <span data-ttu-id="3d05c-111">示例</span><span class="sxs-lookup"><span data-stu-id="3d05c-111">EXAMPLES</span></span>

### <span data-ttu-id="3d05c-112">範例1：使用預設內容取得 ImportExport 工作</span><span class="sxs-lookup"><span data-stu-id="3d05c-112">Example 1: Get ImportExport job with default context</span></span>
```powershell
PS C:\> Get-AzImportExport
Location Name     Type
-------- ----     ----
East US  test-job Microsoft.ImportExport/jobs
```

<span data-ttu-id="3d05c-113">這個 Cmdlet 會取得 ImportExport 作業及預設的內容。</span><span class="sxs-lookup"><span data-stu-id="3d05c-113">This cmdlet gets ImportExport job with default context.</span></span>

### <span data-ttu-id="3d05c-114">範例2：依資源群組和作業名稱取得 ImportExport 工作</span><span class="sxs-lookup"><span data-stu-id="3d05c-114">Example 2: Get ImportExport job by resource group and job name</span></span>
```powershell
PS C:\> Get-AzImportExport -Name test-job -ResourceGroupName ImportTestRG
Location Name     Type
-------- ----     ----
East US  test-job Microsoft.ImportExport/jobs
```

<span data-ttu-id="3d05c-115">這個 Cmdlet 會透過資源群組和作業名稱來取得 ImportExport 工作。</span><span class="sxs-lookup"><span data-stu-id="3d05c-115">This cmdlet gets ImportExport job by resource group and job name.</span></span>

### <span data-ttu-id="3d05c-116">範例3：列出指定資源群組中的所有 ImportExport 工作</span><span class="sxs-lookup"><span data-stu-id="3d05c-116">Example 3: Lists all the ImportExport jobs in specified resource group</span></span>
```powershell
PS C:\> Get-AzImportExport -ResourceGroupName ImportTestRG
Location Name     Type
-------- ----     ----
East US  test-job Microsoft.ImportExport/jobs
```

<span data-ttu-id="3d05c-117">這個 Cmdlet 會列出指定資源群組中的所有 ImportExport 工作。</span><span class="sxs-lookup"><span data-stu-id="3d05c-117">This cmdlet lists all the ImportExport jobs in specified resource group.</span></span>

### <span data-ttu-id="3d05c-118">範例4：依身分識別取得 ImportExport 工作</span><span class="sxs-lookup"><span data-stu-id="3d05c-118">Example 4: Get ImportExport job by identity</span></span>
```powershell
PS C:\> $Id = "/subscriptions/<SubscriptionId>/resourceGroups/ImportTestRG/providers/Microsoft.ImportExport/jobs/test-job"
PS C:\> Get-AzImportExport -InputObject $Id
Location Name     Type
-------- ----     ----
East US  test-job Microsoft.ImportExport/jobs
```

<span data-ttu-id="3d05c-119">這個 Cmdlet 清單會透過身分識別來取得 ImportExport 工作。</span><span class="sxs-lookup"><span data-stu-id="3d05c-119">This cmdlet lists gets ImportExport job by identity.</span></span>

## <span data-ttu-id="3d05c-120">參數</span><span class="sxs-lookup"><span data-stu-id="3d05c-120">PARAMETERS</span></span>

### <span data-ttu-id="3d05c-121">-AcceptLanguage</span><span class="sxs-lookup"><span data-stu-id="3d05c-121">-AcceptLanguage</span></span>
<span data-ttu-id="3d05c-122">指定回應的喜好語言。</span><span class="sxs-lookup"><span data-stu-id="3d05c-122">Specifies the preferred language for the response.</span></span>

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

### <span data-ttu-id="3d05c-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3d05c-123">-DefaultProfile</span></span>
<span data-ttu-id="3d05c-124">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="3d05c-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3d05c-125">-篩選</span><span class="sxs-lookup"><span data-stu-id="3d05c-125">-Filter</span></span>
<span data-ttu-id="3d05c-126">可用於將結果限制為特定條件。</span><span class="sxs-lookup"><span data-stu-id="3d05c-126">Can be used to restrict the results to certain conditions.</span></span>

```yaml
Type: System.String
Parameter Sets: List, List1
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d05c-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3d05c-127">-InputObject</span></span>
<span data-ttu-id="3d05c-128">要構造的身分識別參數，請參閱 INPUTOBJECT 屬性的 [記事] 區段，然後建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="3d05c-128">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ImportExport.Models.IImportExportIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3d05c-129">-名稱</span><span class="sxs-lookup"><span data-stu-id="3d05c-129">-Name</span></span>
<span data-ttu-id="3d05c-130">匯入/匯出作業的名稱。</span><span class="sxs-lookup"><span data-stu-id="3d05c-130">The name of the import/export job.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: JobName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d05c-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3d05c-131">-ResourceGroupName</span></span>
<span data-ttu-id="3d05c-132">資源群組名稱會唯一識別使用者訂閱中的資源群組。</span><span class="sxs-lookup"><span data-stu-id="3d05c-132">The resource group name uniquely identifies the resource group within the user subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List1
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d05c-133">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="3d05c-133">-SubscriptionId</span></span>
<span data-ttu-id="3d05c-134">Azure 使用者的訂閱 ID。</span><span class="sxs-lookup"><span data-stu-id="3d05c-134">The subscription ID for the Azure user.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Get, List, List1
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d05c-135">-上方</span><span class="sxs-lookup"><span data-stu-id="3d05c-135">-Top</span></span>
<span data-ttu-id="3d05c-136">指定最多應傳回多少作業的整數值。</span><span class="sxs-lookup"><span data-stu-id="3d05c-136">An integer value that specifies how many jobs at most should be returned.</span></span>
<span data-ttu-id="3d05c-137">此值不能超過100。</span><span class="sxs-lookup"><span data-stu-id="3d05c-137">The value cannot exceed 100.</span></span>

```yaml
Type: System.Int32
Parameter Sets: List, List1
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d05c-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3d05c-138">CommonParameters</span></span>
<span data-ttu-id="3d05c-139">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="3d05c-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3d05c-140">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="3d05c-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3d05c-141">輸入</span><span class="sxs-lookup"><span data-stu-id="3d05c-141">INPUTS</span></span>

### <span data-ttu-id="3d05c-142">IImportExportIdentity （ImportExport）的</span><span class="sxs-lookup"><span data-stu-id="3d05c-142">Microsoft.Azure.PowerShell.Cmdlets.ImportExport.Models.IImportExportIdentity</span></span>

## <span data-ttu-id="3d05c-143">輸出</span><span class="sxs-lookup"><span data-stu-id="3d05c-143">OUTPUTS</span></span>

### <span data-ttu-id="3d05c-144">IJobResponse （ImportExport）。 Api20161101。</span><span class="sxs-lookup"><span data-stu-id="3d05c-144">Microsoft.Azure.PowerShell.Cmdlets.ImportExport.Models.Api20161101.IJobResponse</span></span>

## <span data-ttu-id="3d05c-145">筆記</span><span class="sxs-lookup"><span data-stu-id="3d05c-145">NOTES</span></span>

<span data-ttu-id="3d05c-146">別名</span><span class="sxs-lookup"><span data-stu-id="3d05c-146">ALIASES</span></span>

<span data-ttu-id="3d05c-147">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="3d05c-147">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="3d05c-148">若要建立如下所述的參數，請構造包含適當屬性的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="3d05c-148">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="3d05c-149">如需雜湊資料表的詳細資訊，請執行 Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="3d05c-149">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="3d05c-150">INPUTOBJECT <IImportExportIdentity> ：身分識別參數</span><span class="sxs-lookup"><span data-stu-id="3d05c-150">INPUTOBJECT <IImportExportIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="3d05c-151">`[Id <String>]`：資源身分識別路徑</span><span class="sxs-lookup"><span data-stu-id="3d05c-151">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="3d05c-152">`[JobName <String>]`：匯入/匯出作業的名稱。</span><span class="sxs-lookup"><span data-stu-id="3d05c-152">`[JobName <String>]`: The name of the import/export job.</span></span>
  - <span data-ttu-id="3d05c-153">`[LocationName <String>]`：位置的名稱。</span><span class="sxs-lookup"><span data-stu-id="3d05c-153">`[LocationName <String>]`: The name of the location.</span></span> <span data-ttu-id="3d05c-154">例如，美國西部或 westus。</span><span class="sxs-lookup"><span data-stu-id="3d05c-154">For example, West US or westus.</span></span>
  - <span data-ttu-id="3d05c-155">`[ResourceGroupName <String>]`：資源群組名稱會唯一識別使用者訂閱中的資源群組。</span><span class="sxs-lookup"><span data-stu-id="3d05c-155">`[ResourceGroupName <String>]`: The resource group name uniquely identifies the resource group within the user subscription.</span></span>
  - <span data-ttu-id="3d05c-156">`[SubscriptionId <String>]`： Azure 使用者的訂閱 ID。</span><span class="sxs-lookup"><span data-stu-id="3d05c-156">`[SubscriptionId <String>]`: The subscription ID for the Azure user.</span></span>

## <span data-ttu-id="3d05c-157">相關連結</span><span class="sxs-lookup"><span data-stu-id="3d05c-157">RELATED LINKS</span></span>

