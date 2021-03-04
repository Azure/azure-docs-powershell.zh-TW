---
external help file: ''
Module Name: Az.ImportExport
online version: https://docs.microsoft.com/powershell/module/az.importexport/get-azimportexport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImportExport/help/Get-AzImportExport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImportExport/help/Get-AzImportExport.md
ms.openlocfilehash: 8825cb9b3d4a2efcd6a326244139950e431d71f1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101905081"
---
# <span data-ttu-id="a1f6f-101">Get-AzImportExport</span><span class="sxs-lookup"><span data-stu-id="a1f6f-101">Get-AzImportExport</span></span>

## <span data-ttu-id="a1f6f-102">簡介</span><span class="sxs-lookup"><span data-stu-id="a1f6f-102">SYNOPSIS</span></span>
<span data-ttu-id="a1f6f-103">獲得現有工作的資訊。</span><span class="sxs-lookup"><span data-stu-id="a1f6f-103">Gets information about an existing job.</span></span>

## <span data-ttu-id="a1f6f-104">語法</span><span class="sxs-lookup"><span data-stu-id="a1f6f-104">SYNTAX</span></span>

### <span data-ttu-id="a1f6f-105">清單 (預設) </span><span class="sxs-lookup"><span data-stu-id="a1f6f-105">List (Default)</span></span>
```
Get-AzImportExport [-SubscriptionId <String[]>] [-Filter <String>] [-Top <Int32>] [-AcceptLanguage <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="a1f6f-106">獲取</span><span class="sxs-lookup"><span data-stu-id="a1f6f-106">Get</span></span>
```
Get-AzImportExport -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-AcceptLanguage <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="a1f6f-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="a1f6f-107">GetViaIdentity</span></span>
```
Get-AzImportExport -InputObject <IImportExportIdentity> [-AcceptLanguage <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="a1f6f-108">清單1</span><span class="sxs-lookup"><span data-stu-id="a1f6f-108">List1</span></span>
```
Get-AzImportExport -ResourceGroupName <String> [-SubscriptionId <String[]>] [-Filter <String>] [-Top <Int32>]
 [-AcceptLanguage <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="a1f6f-109">描述</span><span class="sxs-lookup"><span data-stu-id="a1f6f-109">DESCRIPTION</span></span>
<span data-ttu-id="a1f6f-110">獲得現有工作的資訊。</span><span class="sxs-lookup"><span data-stu-id="a1f6f-110">Gets information about an existing job.</span></span>

## <span data-ttu-id="a1f6f-111">例子</span><span class="sxs-lookup"><span data-stu-id="a1f6f-111">EXAMPLES</span></span>

### <span data-ttu-id="a1f6f-112">範例 1：取得具有預設上下文的 ImportExport 工作</span><span class="sxs-lookup"><span data-stu-id="a1f6f-112">Example 1: Get ImportExport job with default context</span></span>
```powershell
PS C:\> Get-AzImportExport
Location Name     Type
-------- ----     ----
East US  test-job Microsoft.ImportExport/jobs
```

<span data-ttu-id="a1f6f-113">此 Cmdlet 會獲得具有預設上下文的 ImportExport 工作。</span><span class="sxs-lookup"><span data-stu-id="a1f6f-113">This cmdlet gets ImportExport job with default context.</span></span>

### <span data-ttu-id="a1f6f-114">範例 2：根據資源群組和工作名稱取得 ImportExport 工作</span><span class="sxs-lookup"><span data-stu-id="a1f6f-114">Example 2: Get ImportExport job by resource group and job name</span></span>
```powershell
PS C:\> Get-AzImportExport -Name test-job -ResourceGroupName ImportTestRG
Location Name     Type
-------- ----     ----
East US  test-job Microsoft.ImportExport/jobs
```

<span data-ttu-id="a1f6f-115">此 Cmdlet 會按資源群組和工作名稱獲得 ImportExport 工作。</span><span class="sxs-lookup"><span data-stu-id="a1f6f-115">This cmdlet gets ImportExport job by resource group and job name.</span></span>

### <span data-ttu-id="a1f6f-116">範例 3：列出指定資源群組中所有 ImportExport 工作</span><span class="sxs-lookup"><span data-stu-id="a1f6f-116">Example 3: Lists all the ImportExport jobs in specified resource group</span></span>
```powershell
PS C:\> Get-AzImportExport -ResourceGroupName ImportTestRG
Location Name     Type
-------- ----     ----
East US  test-job Microsoft.ImportExport/jobs
```

<span data-ttu-id="a1f6f-117">此 Cmdlet 會列出指定資源群組中所有 ImportExport 工作。</span><span class="sxs-lookup"><span data-stu-id="a1f6f-117">This cmdlet lists all the ImportExport jobs in specified resource group.</span></span>

### <span data-ttu-id="a1f6f-118">範例 4：根據身分識別取得 ImportExport 工作</span><span class="sxs-lookup"><span data-stu-id="a1f6f-118">Example 4: Get ImportExport job by identity</span></span>
```powershell
PS C:\> $Id = "/subscriptions/<SubscriptionId>/resourceGroups/ImportTestRG/providers/Microsoft.ImportExport/jobs/test-job"
PS C:\> Get-AzImportExport -InputObject $Id
Location Name     Type
-------- ----     ----
East US  test-job Microsoft.ImportExport/jobs
```

<span data-ttu-id="a1f6f-119">此 Cmdlet 清單會以身分識別獲得 ImportExport 工作。</span><span class="sxs-lookup"><span data-stu-id="a1f6f-119">This cmdlet lists gets ImportExport job by identity.</span></span>

## <span data-ttu-id="a1f6f-120">參數</span><span class="sxs-lookup"><span data-stu-id="a1f6f-120">PARAMETERS</span></span>

### <span data-ttu-id="a1f6f-121">-AcceptLanguage</span><span class="sxs-lookup"><span data-stu-id="a1f6f-121">-AcceptLanguage</span></span>
<span data-ttu-id="a1f6f-122">指定回應的偏好語言。</span><span class="sxs-lookup"><span data-stu-id="a1f6f-122">Specifies the preferred language for the response.</span></span>

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

### <span data-ttu-id="a1f6f-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a1f6f-123">-DefaultProfile</span></span>
<span data-ttu-id="a1f6f-124">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="a1f6f-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a1f6f-125">-篩選</span><span class="sxs-lookup"><span data-stu-id="a1f6f-125">-Filter</span></span>
<span data-ttu-id="a1f6f-126">可用來將結果限制為特定條件。</span><span class="sxs-lookup"><span data-stu-id="a1f6f-126">Can be used to restrict the results to certain conditions.</span></span>

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

### <span data-ttu-id="a1f6f-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a1f6f-127">-InputObject</span></span>
<span data-ttu-id="a1f6f-128">身分識別參數若要建構，請參閱 INPUTOBJECT 屬性的 NOTES 區段，並建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="a1f6f-128">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="a1f6f-129">-名稱</span><span class="sxs-lookup"><span data-stu-id="a1f6f-129">-Name</span></span>
<span data-ttu-id="a1f6f-130">匯進/匯出工作的名稱。</span><span class="sxs-lookup"><span data-stu-id="a1f6f-130">The name of the import/export job.</span></span>

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

### <span data-ttu-id="a1f6f-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a1f6f-131">-ResourceGroupName</span></span>
<span data-ttu-id="a1f6f-132">資源組名可唯一識別使用者訂閱中的資源群組。</span><span class="sxs-lookup"><span data-stu-id="a1f6f-132">The resource group name uniquely identifies the resource group within the user subscription.</span></span>

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

### <span data-ttu-id="a1f6f-133">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="a1f6f-133">-SubscriptionId</span></span>
<span data-ttu-id="a1f6f-134">Azure 使用者的訂閱識別碼。</span><span class="sxs-lookup"><span data-stu-id="a1f6f-134">The subscription ID for the Azure user.</span></span>

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

### <span data-ttu-id="a1f6f-135">-頂端</span><span class="sxs-lookup"><span data-stu-id="a1f6f-135">-Top</span></span>
<span data-ttu-id="a1f6f-136">指定最多應退回多少個工作的整數值。</span><span class="sxs-lookup"><span data-stu-id="a1f6f-136">An integer value that specifies how many jobs at most should be returned.</span></span>
<span data-ttu-id="a1f6f-137">值不能超過 100。</span><span class="sxs-lookup"><span data-stu-id="a1f6f-137">The value cannot exceed 100.</span></span>

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

### <span data-ttu-id="a1f6f-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a1f6f-138">CommonParameters</span></span>
<span data-ttu-id="a1f6f-139">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="a1f6f-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a1f6f-140">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a1f6f-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a1f6f-141">輸入</span><span class="sxs-lookup"><span data-stu-id="a1f6f-141">INPUTS</span></span>

### <span data-ttu-id="a1f6f-142">Microsoft.Azure.PowerShell.Cmdlets.ImportExport.models.IImportExportIdentity</span><span class="sxs-lookup"><span data-stu-id="a1f6f-142">Microsoft.Azure.PowerShell.Cmdlets.ImportExport.Models.IImportExportIdentity</span></span>

## <span data-ttu-id="a1f6f-143">輸出</span><span class="sxs-lookup"><span data-stu-id="a1f6f-143">OUTPUTS</span></span>

### <span data-ttu-id="a1f6f-144">Microsoft.Azure.PowerShell.Cmdlets.ImportExport.models.Api20161101.IJobResponse</span><span class="sxs-lookup"><span data-stu-id="a1f6f-144">Microsoft.Azure.PowerShell.Cmdlets.ImportExport.Models.Api20161101.IJobResponse</span></span>

## <span data-ttu-id="a1f6f-145">筆記</span><span class="sxs-lookup"><span data-stu-id="a1f6f-145">NOTES</span></span>

<span data-ttu-id="a1f6f-146">別名</span><span class="sxs-lookup"><span data-stu-id="a1f6f-146">ALIASES</span></span>

<span data-ttu-id="a1f6f-147">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="a1f6f-147">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="a1f6f-148">若要建立下列描述的參數，請建構包含適當屬性的雜湊表。</span><span class="sxs-lookup"><span data-stu-id="a1f6f-148">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="a1f6f-149">有關雜湊表的資訊，請執行Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="a1f6f-149">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="a1f6f-150">INPUTOBJECT： <IImportExportIdentity> 身分識別參數</span><span class="sxs-lookup"><span data-stu-id="a1f6f-150">INPUTOBJECT <IImportExportIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="a1f6f-151">`[Id <String>]`：資源識別路徑</span><span class="sxs-lookup"><span data-stu-id="a1f6f-151">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="a1f6f-152">`[JobName <String>]`：匯進/匯出工作的名稱。</span><span class="sxs-lookup"><span data-stu-id="a1f6f-152">`[JobName <String>]`: The name of the import/export job.</span></span>
  - <span data-ttu-id="a1f6f-153">`[LocationName <String>]`：位置的名稱。</span><span class="sxs-lookup"><span data-stu-id="a1f6f-153">`[LocationName <String>]`: The name of the location.</span></span> <span data-ttu-id="a1f6f-154">例如，美國西部或西部。</span><span class="sxs-lookup"><span data-stu-id="a1f6f-154">For example, West US or westus.</span></span>
  - <span data-ttu-id="a1f6f-155">`[ResourceGroupName <String>]`：資源組名可唯一識別使用者訂閱中的資源群組。</span><span class="sxs-lookup"><span data-stu-id="a1f6f-155">`[ResourceGroupName <String>]`: The resource group name uniquely identifies the resource group within the user subscription.</span></span>
  - <span data-ttu-id="a1f6f-156">`[SubscriptionId <String>]`：Azure 使用者的訂閱識別碼。</span><span class="sxs-lookup"><span data-stu-id="a1f6f-156">`[SubscriptionId <String>]`: The subscription ID for the Azure user.</span></span>

## <span data-ttu-id="a1f6f-157">相關連結</span><span class="sxs-lookup"><span data-stu-id="a1f6f-157">RELATED LINKS</span></span>

