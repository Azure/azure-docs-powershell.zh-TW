---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/powershell/module/az.resources/get-azmanagementgroupdeploymentwhatifresult
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzManagementGroupDeploymentWhatIfResult.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzManagementGroupDeploymentWhatIfResult.md
ms.openlocfilehash: 981d9e771a988a4166f542854959b38e140d2061
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101906885"
---
# <span data-ttu-id="17e8e-101">Get-AzManagementGroupDeploymentWhatIfResult</span><span class="sxs-lookup"><span data-stu-id="17e8e-101">Get-AzManagementGroupDeploymentWhatIfResult</span></span>

## <span data-ttu-id="17e8e-102">簡介</span><span class="sxs-lookup"><span data-stu-id="17e8e-102">SYNOPSIS</span></span>
<span data-ttu-id="17e8e-103">在管理What-If取得部署結果的範本。</span><span class="sxs-lookup"><span data-stu-id="17e8e-103">Gets a template What-If result for a deployment at management group scope.</span></span> 

## <span data-ttu-id="17e8e-104">語法</span><span class="sxs-lookup"><span data-stu-id="17e8e-104">SYNTAX</span></span>

### <span data-ttu-id="17e8e-105">ByTemplateFileWithNoParameters (預設) </span><span class="sxs-lookup"><span data-stu-id="17e8e-105">ByTemplateFileWithNoParameters (Default)</span></span>
```
Get-AzManagementGroupDeploymentWhatIfResult [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-ResultFormat <WhatIfResultFormat>] [-ExcludeChangeType <String[]>] -TemplateFile <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="17e8e-106">ByTemplateObjectAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="17e8e-106">ByTemplateObjectAndParameterObject</span></span>
```
Get-AzManagementGroupDeploymentWhatIfResult [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-ResultFormat <WhatIfResultFormat>] [-ExcludeChangeType <String[]>] -TemplateParameterObject <Hashtable>
 -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="17e8e-107">ByTemplateFileAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="17e8e-107">ByTemplateFileAndParameterObject</span></span>
```
Get-AzManagementGroupDeploymentWhatIfResult [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-ResultFormat <WhatIfResultFormat>] [-ExcludeChangeType <String[]>] -TemplateParameterObject <Hashtable>
 -TemplateFile <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="17e8e-108">ByTemplateUriAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="17e8e-108">ByTemplateUriAndParameterObject</span></span>
```
Get-AzManagementGroupDeploymentWhatIfResult [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-ResultFormat <WhatIfResultFormat>] [-ExcludeChangeType <String[]>] -TemplateParameterObject <Hashtable>
 -TemplateUri <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="17e8e-109">ByTemplateObjectAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="17e8e-109">ByTemplateObjectAndParameterFile</span></span>
```
Get-AzManagementGroupDeploymentWhatIfResult [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-ResultFormat <WhatIfResultFormat>] [-ExcludeChangeType <String[]>] -TemplateParameterFile <String>
 -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="17e8e-110">ByTemplateFileAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="17e8e-110">ByTemplateFileAndParameterFile</span></span>
```
Get-AzManagementGroupDeploymentWhatIfResult [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-ResultFormat <WhatIfResultFormat>] [-ExcludeChangeType <String[]>] -TemplateParameterFile <String>
 -TemplateFile <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="17e8e-111">ByTemplateUriAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="17e8e-111">ByTemplateUriAndParameterFile</span></span>
```
Get-AzManagementGroupDeploymentWhatIfResult [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-ResultFormat <WhatIfResultFormat>] [-ExcludeChangeType <String[]>] -TemplateParameterFile <String>
 -TemplateUri <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="17e8e-112">ByTemplateObjectAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="17e8e-112">ByTemplateObjectAndParameterUri</span></span>
```
Get-AzManagementGroupDeploymentWhatIfResult [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-ResultFormat <WhatIfResultFormat>] [-ExcludeChangeType <String[]>] -TemplateParameterUri <String>
 -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="17e8e-113">ByTemplateFileAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="17e8e-113">ByTemplateFileAndParameterUri</span></span>
```
Get-AzManagementGroupDeploymentWhatIfResult [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-ResultFormat <WhatIfResultFormat>] [-ExcludeChangeType <String[]>] -TemplateParameterUri <String>
 -TemplateFile <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="17e8e-114">ByTemplateUriAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="17e8e-114">ByTemplateUriAndParameterUri</span></span>
```
Get-AzManagementGroupDeploymentWhatIfResult [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-ResultFormat <WhatIfResultFormat>] [-ExcludeChangeType <String[]>] -TemplateParameterUri <String>
 -TemplateUri <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="17e8e-115">ByTemplateObjectWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="17e8e-115">ByTemplateObjectWithNoParameters</span></span>
```
Get-AzManagementGroupDeploymentWhatIfResult [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-ResultFormat <WhatIfResultFormat>] [-ExcludeChangeType <String[]>] -TemplateObject <Hashtable>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="17e8e-116">ByTemplateUriWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="17e8e-116">ByTemplateUriWithNoParameters</span></span>
```
Get-AzManagementGroupDeploymentWhatIfResult [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-ResultFormat <WhatIfResultFormat>] [-ExcludeChangeType <String[]>] -TemplateUri <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="17e8e-117">描述</span><span class="sxs-lookup"><span data-stu-id="17e8e-117">DESCRIPTION</span></span>
<span data-ttu-id="17e8e-118">**Get-AzManagementGroupDeploymentWhatIfResult** Cmdlet 會取得指定管理群組What-If範本部署的 ARM 範本 What-If 結果。</span><span class="sxs-lookup"><span data-stu-id="17e8e-118">The **Get-AzManagementGroupDeploymentWhatIfResult** cmdlet gets the ARM template What-If result for a template deployment at the specified management group scope.</span></span> <span data-ttu-id="17e8e-119">它會回一份變更清單，指出如果部署已執行，且不會對實際資源進行任何變更，將會更新哪些資源。</span><span class="sxs-lookup"><span data-stu-id="17e8e-119">It returns a list of changes indicating what resources will be updated if the deployment is applied without making any changes to real resources.</span></span> <span data-ttu-id="17e8e-120">若要指定傳回結果的格式，請使用 *ResultFormat* 參數。</span><span class="sxs-lookup"><span data-stu-id="17e8e-120">To specify the format for the returning result, use the *ResultFormat* parameter.</span></span>

## <span data-ttu-id="17e8e-121">例子</span><span class="sxs-lookup"><span data-stu-id="17e8e-121">EXAMPLES</span></span>

### <span data-ttu-id="17e8e-122">範例 1：在管理What-If範圍中取得結果</span><span class="sxs-lookup"><span data-stu-id="17e8e-122">Example 1: Get a What-If result at management group scope</span></span>
```powershell
PS C:\> Get-AzManagementGroupDeploymentWhatIfResult `
    -DeploymentName "deploy-01" `
    -Location "West US" `
    -ManagementGroupId "myManagementGroup" `
    -TemplateFile "D:\Azure\Templates\ServiceTemplate.json" `
    -TemplateParameterFile "D:\Azure\Templates\ServiceParameters.json" `
    -ResultFormat "FullResourcePayloads"
```

<span data-ttu-id="17e8e-123">此命令會使用What-If範本檔案和磁片上的參數檔案，在管理群組範圍取得一個結果。</span><span class="sxs-lookup"><span data-stu-id="17e8e-123">This command gets a What-If result at management group scope by using a custom template file and a parameter file on disk.</span></span>
<span data-ttu-id="17e8e-124">命令會使用 *Location* 參數指定儲存部署資料的位置。</span><span class="sxs-lookup"><span data-stu-id="17e8e-124">The command uses the *Location* parameter to specify where to store the deployment data.</span></span>
<span data-ttu-id="17e8e-125">該命令使用 *ManagementGroupId* 參數來指定要部署範本的管理群組。</span><span class="sxs-lookup"><span data-stu-id="17e8e-125">The command uses the *ManagementGroupId* parameter to specify the management group where the template will be deployed.</span></span>
<span data-ttu-id="17e8e-126">該命令使用 *TemplateFile* 參數來指定範本檔案。</span><span class="sxs-lookup"><span data-stu-id="17e8e-126">The command uses the *TemplateFile* parameter to specify a template file.</span></span>
<span data-ttu-id="17e8e-127">該命令使用 *TemplateParameterFile* 參數來指定範本參數檔案。</span><span class="sxs-lookup"><span data-stu-id="17e8e-127">The command uses the *TemplateParameterFile* parameter to specify a template parameter file.</span></span>
<span data-ttu-id="17e8e-128">命令使用 *ResultFormat* 參數來設定What-If，以包含完整的資源負載。</span><span class="sxs-lookup"><span data-stu-id="17e8e-128">The command uses the *ResultFormat* parameter to set the What-If result to include full resource payloads.</span></span>

### <span data-ttu-id="17e8e-129">範例 2：使用 ResourceIdOnly What-If管理群組範圍取得結果</span><span class="sxs-lookup"><span data-stu-id="17e8e-129">Example 2: Get a What-If result at management group scope with ResourceIdOnly</span></span>
```powershell
PS C:\> Get-AzManagementGroupDeploymentWhatIfResult `
    -DeploymentName "deploy-01" `
    -Location "West US" `
    -ManagementGroupId "myManagementGroup" `
    -TemplateFile "D:\Azure\Templates\ServiceTemplate.json" `
    -TemplateParameterFile "D:\Azure\Templates\ServiceParameters.json" `
    -ResultFormat "ResourceIdOnly"
```

<span data-ttu-id="17e8e-130">此命令會使用What-If範本檔案和磁片上的參數檔案，在管理群組範圍取得一個結果。</span><span class="sxs-lookup"><span data-stu-id="17e8e-130">This command gets a What-If result at management group scope by using a custom template file and a parameter file on disk.</span></span>
<span data-ttu-id="17e8e-131">命令會使用 *Location* 參數指定儲存部署資料的位置。</span><span class="sxs-lookup"><span data-stu-id="17e8e-131">The command uses the *Location* parameter to specify where to store the deployment data.</span></span>
<span data-ttu-id="17e8e-132">該命令使用 *ManagementGroupId* 參數來指定要部署範本的管理群組。</span><span class="sxs-lookup"><span data-stu-id="17e8e-132">The command uses the *ManagementGroupId* parameter to specify the management group where the template will be deployed.</span></span>
<span data-ttu-id="17e8e-133">該命令使用 *TemplateFile* 參數來指定範本檔案。</span><span class="sxs-lookup"><span data-stu-id="17e8e-133">The command uses the *TemplateFile* parameter to specify a template file.</span></span>
<span data-ttu-id="17e8e-134">該命令使用 *TemplateParameterFile* 參數來指定範本參數檔案。</span><span class="sxs-lookup"><span data-stu-id="17e8e-134">The command uses the *TemplateParameterFile* parameter to specify a template parameter file.</span></span>
<span data-ttu-id="17e8e-135">命令使用 *ResultFormat* 參數，將結果What-If只包含資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="17e8e-135">The command uses the *ResultFormat* parameter to set the What-If result to only contain resource IDs.</span></span>

## <span data-ttu-id="17e8e-136">參數</span><span class="sxs-lookup"><span data-stu-id="17e8e-136">PARAMETERS</span></span>

### <span data-ttu-id="17e8e-137">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="17e8e-137">-DefaultProfile</span></span>
<span data-ttu-id="17e8e-138">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="17e8e-138">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="17e8e-139">-ExcludeChangeType</span><span class="sxs-lookup"><span data-stu-id="17e8e-139">-ExcludeChangeType</span></span>
<span data-ttu-id="17e8e-140">要排除在結果中之資源變更類型的逗號分隔What-If清單。</span><span class="sxs-lookup"><span data-stu-id="17e8e-140">Comma-separated list of resource change types to be excluded from What-If results.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="17e8e-141">-位置</span><span class="sxs-lookup"><span data-stu-id="17e8e-141">-Location</span></span>
<span data-ttu-id="17e8e-142">儲存部署資料的位置。</span><span class="sxs-lookup"><span data-stu-id="17e8e-142">The location to store deployment data.</span></span>

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

### <span data-ttu-id="17e8e-143">-ManagementGroupId</span><span class="sxs-lookup"><span data-stu-id="17e8e-143">-ManagementGroupId</span></span>
<span data-ttu-id="17e8e-144">管理群組識別碼。</span><span class="sxs-lookup"><span data-stu-id="17e8e-144">The management group ID.</span></span>

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

### <span data-ttu-id="17e8e-145">-名稱</span><span class="sxs-lookup"><span data-stu-id="17e8e-145">-Name</span></span>
<span data-ttu-id="17e8e-146">要建立之部署的名稱。</span><span class="sxs-lookup"><span data-stu-id="17e8e-146">The name of the deployment it's going to create.</span></span>
<span data-ttu-id="17e8e-147">如果未指定，則提供範本檔案時預設為範本檔案名;預設為提供範本物件的目前時間，例如"20131223140835"。</span><span class="sxs-lookup"><span data-stu-id="17e8e-147">If not specified, defaults to the template file name when a template file is provided; defaults to the current time when a template object is provided, e.g. "20131223140835".</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: DeploymentName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="17e8e-148">-Pre</span><span class="sxs-lookup"><span data-stu-id="17e8e-148">-Pre</span></span>
<span data-ttu-id="17e8e-149">設定之後，表示當系統自動決定要使用哪個版本時，Cmdlet 應該使用測試版 API 版本。</span><span class="sxs-lookup"><span data-stu-id="17e8e-149">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="17e8e-150">-ResultFormat</span><span class="sxs-lookup"><span data-stu-id="17e8e-150">-ResultFormat</span></span>
<span data-ttu-id="17e8e-151">此What-If格式。</span><span class="sxs-lookup"><span data-stu-id="17e8e-151">The What-If result format.</span></span>

```yaml
Type: Microsoft.Azure.Management.ResourceManager.Models.WhatIfResultFormat
Parameter Sets: (All)
Aliases:
Accepted values: ResourceIdOnly, FullResourcePayloads

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="17e8e-152">-SkipTemplateParameterPrompt</span><span class="sxs-lookup"><span data-stu-id="17e8e-152">-SkipTemplateParameterPrompt</span></span>
<span data-ttu-id="17e8e-153">跳過 PowerShell 動態參數處理，檢查所提供的範本參數是否包含範本使用的所有必要參數。</span><span class="sxs-lookup"><span data-stu-id="17e8e-153">Skips the PowerShell dynamic parameter processing that checks if the provided template parameter contains all necessary parameters used by the template.</span></span>
<span data-ttu-id="17e8e-154">這項檢查會提示使用者提供遺失參數的值，但若發現參數未系在範本中，則提供 -SkipTemplateParameterPrompt 會忽略此提示並立即錯誤。</span><span class="sxs-lookup"><span data-stu-id="17e8e-154">This check would prompt the user to provide a value for the missing parameters, but providing the -SkipTemplateParameterPrompt will ignore this prompt and error out immediately if a parameter was found not to be bound in the template.</span></span>
<span data-ttu-id="17e8e-155">針對非互動式腳本，您可以提供 -SkipTemplateParameterPrompt，以在未滿足所有所需參數的情況下提供更佳的錯誤訊息。</span><span class="sxs-lookup"><span data-stu-id="17e8e-155">For non-interactive scripts, -SkipTemplateParameterPrompt can be provided to provide a better error message in the case where not all required parameters are satisfied.</span></span>

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

### <span data-ttu-id="17e8e-156">-TemplateFile</span><span class="sxs-lookup"><span data-stu-id="17e8e-156">-TemplateFile</span></span>
<span data-ttu-id="17e8e-157">範本檔案的當地路徑。</span><span class="sxs-lookup"><span data-stu-id="17e8e-157">Local path to the template file.</span></span> <span data-ttu-id="17e8e-158">支援的範本檔案類型：json 和 bicep。</span><span class="sxs-lookup"><span data-stu-id="17e8e-158">Supported template file type: json and bicep.</span></span>

```yaml
Type: System.String
Parameter Sets: ByTemplateFileWithNoParameters, ByTemplateFileAndParameterObject, ByTemplateFileAndParameterFile, ByTemplateFileAndParameterUri
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="17e8e-159">-TemplateObject</span><span class="sxs-lookup"><span data-stu-id="17e8e-159">-TemplateObject</span></span>
<span data-ttu-id="17e8e-160">代表範本的雜湊表格。</span><span class="sxs-lookup"><span data-stu-id="17e8e-160">A hash table which represents the template.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: ByTemplateObjectAndParameterObject, ByTemplateObjectAndParameterFile, ByTemplateObjectAndParameterUri, ByTemplateObjectWithNoParameters
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="17e8e-161">-TemplateParameterFile</span><span class="sxs-lookup"><span data-stu-id="17e8e-161">-TemplateParameterFile</span></span>
<span data-ttu-id="17e8e-162">具有範本參數的檔案。</span><span class="sxs-lookup"><span data-stu-id="17e8e-162">A file that has the template parameters.</span></span>

```yaml
Type: System.String
Parameter Sets: ByTemplateObjectAndParameterFile, ByTemplateFileAndParameterFile, ByTemplateUriAndParameterFile
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="17e8e-163">-TemplateParameterObject</span><span class="sxs-lookup"><span data-stu-id="17e8e-163">-TemplateParameterObject</span></span>
<span data-ttu-id="17e8e-164">代表參數的雜湊表格。</span><span class="sxs-lookup"><span data-stu-id="17e8e-164">A hash table which represents the parameters.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: ByTemplateObjectAndParameterObject, ByTemplateFileAndParameterObject, ByTemplateUriAndParameterObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="17e8e-165">-TemplateParameterUri</span><span class="sxs-lookup"><span data-stu-id="17e8e-165">-TemplateParameterUri</span></span>
<span data-ttu-id="17e8e-166">Uri 到範本參數檔案。</span><span class="sxs-lookup"><span data-stu-id="17e8e-166">Uri to the template parameter file.</span></span>

```yaml
Type: System.String
Parameter Sets: ByTemplateObjectAndParameterUri, ByTemplateFileAndParameterUri, ByTemplateUriAndParameterUri
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="17e8e-167">-TemplateUri</span><span class="sxs-lookup"><span data-stu-id="17e8e-167">-TemplateUri</span></span>
<span data-ttu-id="17e8e-168">Uri 到範本檔案。</span><span class="sxs-lookup"><span data-stu-id="17e8e-168">Uri to the template file.</span></span>

```yaml
Type: System.String
Parameter Sets: ByTemplateUriAndParameterObject, ByTemplateUriAndParameterFile, ByTemplateUriAndParameterUri, ByTemplateUriWithNoParameters
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="17e8e-169">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="17e8e-169">CommonParameters</span></span>
<span data-ttu-id="17e8e-170">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="17e8e-170">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="17e8e-171">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="17e8e-171">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="17e8e-172">輸入</span><span class="sxs-lookup"><span data-stu-id="17e8e-172">INPUTS</span></span>

### <span data-ttu-id="17e8e-173">System.String</span><span class="sxs-lookup"><span data-stu-id="17e8e-173">System.String</span></span>

### <span data-ttu-id="17e8e-174">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="17e8e-174">System.Collections.Hashtable</span></span>

## <span data-ttu-id="17e8e-175">輸出</span><span class="sxs-lookup"><span data-stu-id="17e8e-175">OUTPUTS</span></span>

### <span data-ttu-id="17e8e-176">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.Deployments.PSWhatIfOperationResult</span><span class="sxs-lookup"><span data-stu-id="17e8e-176">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.Deployments.PSWhatIfOperationResult</span></span>

## <span data-ttu-id="17e8e-177">筆記</span><span class="sxs-lookup"><span data-stu-id="17e8e-177">NOTES</span></span>

## <span data-ttu-id="17e8e-178">相關連結</span><span class="sxs-lookup"><span data-stu-id="17e8e-178">RELATED LINKS</span></span>
