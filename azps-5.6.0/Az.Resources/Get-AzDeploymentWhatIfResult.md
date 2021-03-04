---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/powershell/module/az.resources/get-azdeploymentwhatifresult
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzDeploymentWhatIfResult.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzDeploymentWhatIfResult.md
ms.openlocfilehash: 725984f8893b7373ded513b0d7242d9ec4bd0c6e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101910385"
---
# <span data-ttu-id="fb9a5-101">Get-AzDeploymentWhatIfResult</span><span class="sxs-lookup"><span data-stu-id="fb9a5-101">Get-AzDeploymentWhatIfResult</span></span>

## <span data-ttu-id="fb9a5-102">簡介</span><span class="sxs-lookup"><span data-stu-id="fb9a5-102">SYNOPSIS</span></span>
<span data-ttu-id="fb9a5-103">在訂閱What-If取得部署結果的範本。</span><span class="sxs-lookup"><span data-stu-id="fb9a5-103">Gets a template What-If result for a deployment at subscription scope.</span></span> 

## <span data-ttu-id="fb9a5-104">語法</span><span class="sxs-lookup"><span data-stu-id="fb9a5-104">SYNTAX</span></span>

### <span data-ttu-id="fb9a5-105">ByTemplateFileWithNoParameters (預設) </span><span class="sxs-lookup"><span data-stu-id="fb9a5-105">ByTemplateFileWithNoParameters (Default)</span></span>
```
Get-AzDeploymentWhatIfResult [-Name <String>] -Location <String> [-ResultFormat <WhatIfResultFormat>]
 [-ExcludeChangeType <String[]>] -TemplateFile <String> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fb9a5-106">ByTemplateObjectAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="fb9a5-106">ByTemplateObjectAndParameterObject</span></span>
```
Get-AzDeploymentWhatIfResult [-Name <String>] -Location <String> [-ResultFormat <WhatIfResultFormat>]
 [-ExcludeChangeType <String[]>] -TemplateParameterObject <Hashtable> -TemplateObject <Hashtable>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fb9a5-107">ByTemplateFileAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="fb9a5-107">ByTemplateFileAndParameterObject</span></span>
```
Get-AzDeploymentWhatIfResult [-Name <String>] -Location <String> [-ResultFormat <WhatIfResultFormat>]
 [-ExcludeChangeType <String[]>] -TemplateParameterObject <Hashtable> -TemplateFile <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fb9a5-108">ByTemplateUriAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="fb9a5-108">ByTemplateUriAndParameterObject</span></span>
```
Get-AzDeploymentWhatIfResult [-Name <String>] -Location <String> [-ResultFormat <WhatIfResultFormat>]
 [-ExcludeChangeType <String[]>] -TemplateParameterObject <Hashtable> -TemplateUri <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fb9a5-109">ByTemplateObjectAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="fb9a5-109">ByTemplateObjectAndParameterFile</span></span>
```
Get-AzDeploymentWhatIfResult [-Name <String>] -Location <String> [-ResultFormat <WhatIfResultFormat>]
 [-ExcludeChangeType <String[]>] -TemplateParameterFile <String> -TemplateObject <Hashtable>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fb9a5-110">ByTemplateFileAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="fb9a5-110">ByTemplateFileAndParameterFile</span></span>
```
Get-AzDeploymentWhatIfResult [-Name <String>] -Location <String> [-ResultFormat <WhatIfResultFormat>]
 [-ExcludeChangeType <String[]>] -TemplateParameterFile <String> -TemplateFile <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fb9a5-111">ByTemplateUriAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="fb9a5-111">ByTemplateUriAndParameterFile</span></span>
```
Get-AzDeploymentWhatIfResult [-Name <String>] -Location <String> [-ResultFormat <WhatIfResultFormat>]
 [-ExcludeChangeType <String[]>] -TemplateParameterFile <String> -TemplateUri <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fb9a5-112">ByTemplateObjectAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="fb9a5-112">ByTemplateObjectAndParameterUri</span></span>
```
Get-AzDeploymentWhatIfResult [-Name <String>] -Location <String> [-ResultFormat <WhatIfResultFormat>]
 [-ExcludeChangeType <String[]>] -TemplateParameterUri <String> -TemplateObject <Hashtable>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fb9a5-113">ByTemplateFileAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="fb9a5-113">ByTemplateFileAndParameterUri</span></span>
```
Get-AzDeploymentWhatIfResult [-Name <String>] -Location <String> [-ResultFormat <WhatIfResultFormat>]
 [-ExcludeChangeType <String[]>] -TemplateParameterUri <String> -TemplateFile <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fb9a5-114">ByTemplateUriAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="fb9a5-114">ByTemplateUriAndParameterUri</span></span>
```
Get-AzDeploymentWhatIfResult [-Name <String>] -Location <String> [-ResultFormat <WhatIfResultFormat>]
 [-ExcludeChangeType <String[]>] -TemplateParameterUri <String> -TemplateUri <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fb9a5-115">ByTemplateObjectWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="fb9a5-115">ByTemplateObjectWithNoParameters</span></span>
```
Get-AzDeploymentWhatIfResult [-Name <String>] -Location <String> [-ResultFormat <WhatIfResultFormat>]
 [-ExcludeChangeType <String[]>] -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fb9a5-116">ByTemplateUriWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="fb9a5-116">ByTemplateUriWithNoParameters</span></span>
```
Get-AzDeploymentWhatIfResult [-Name <String>] -Location <String> [-ResultFormat <WhatIfResultFormat>]
 [-ExcludeChangeType <String[]>] -TemplateUri <String> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fb9a5-117">描述</span><span class="sxs-lookup"><span data-stu-id="fb9a5-117">DESCRIPTION</span></span>
<span data-ttu-id="fb9a5-118">**Get-AzDeploymentWhatIfResult** Cmdlet 會取得 ARM 範本What-If目前訂閱範圍中範本部署的結果。</span><span class="sxs-lookup"><span data-stu-id="fb9a5-118">The **Get-AzDeploymentWhatIfResult** cmdlet gets the ARM template What-If result for a template deployment at the current subscription scope.</span></span> <span data-ttu-id="fb9a5-119">它會回一份變更清單，指出如果部署已執行，且不會對實際資源進行任何變更，將會更新哪些資源。</span><span class="sxs-lookup"><span data-stu-id="fb9a5-119">It returns a list of changes indicating what resources will be updated if the deployment is applied without making any changes to real resources.</span></span> <span data-ttu-id="fb9a5-120">若要指定傳回結果的格式，請使用 *ResultFormat* 參數。</span><span class="sxs-lookup"><span data-stu-id="fb9a5-120">To specify the format for the returning result, use the *ResultFormat* parameter.</span></span>

## <span data-ttu-id="fb9a5-121">例子</span><span class="sxs-lookup"><span data-stu-id="fb9a5-121">EXAMPLES</span></span>

### <span data-ttu-id="fb9a5-122">範例 1：在訂閱What-If取得結果</span><span class="sxs-lookup"><span data-stu-id="fb9a5-122">Example 1: Get a What-If result at subscription scope</span></span>
```powershell
PS C:\> Get-AzDeploymentWhatIfResult `
    -DeploymentName "deploy-01" `
    -Location "West US" `
    -TemplateFile "D:\Azure\Templates\ServiceTemplate.json" `
    -TemplateParameterFile "D:\Azure\Templates\ServiceParameters.json" `
    -ResultFormat "FullResourcePayloads"
```

<span data-ttu-id="fb9a5-123">此命令會使用What-If範本檔案和磁片上的參數檔案，以取得目前訂閱範圍中的結果。</span><span class="sxs-lookup"><span data-stu-id="fb9a5-123">This command gets a What-If result at the current subscription scope by using a custom template file and a parameter file on disk.</span></span>
<span data-ttu-id="fb9a5-124">命令會使用 *Location* 參數指定儲存部署資料的位置。</span><span class="sxs-lookup"><span data-stu-id="fb9a5-124">The command uses the *Location* parameter to specify where to store the deployment data.</span></span>
<span data-ttu-id="fb9a5-125">該命令使用 *TemplateFile* 參數來指定範本檔案。</span><span class="sxs-lookup"><span data-stu-id="fb9a5-125">The command uses the *TemplateFile* parameter to specify a template file.</span></span>
<span data-ttu-id="fb9a5-126">該命令使用 *TemplateParameterFile* 參數來指定範本參數檔案。</span><span class="sxs-lookup"><span data-stu-id="fb9a5-126">The command uses the *TemplateParameterFile* parameter to specify a template parameter file.</span></span>
<span data-ttu-id="fb9a5-127">命令使用 *ResultFormat* 參數來設定What-If，以包含完整的資源負載。</span><span class="sxs-lookup"><span data-stu-id="fb9a5-127">The command uses the *ResultFormat* parameter to set the What-If result to include full resource payloads.</span></span>

### <span data-ttu-id="fb9a5-128">範例 2：使用 ResourceIdOnly 在訂閱What-If取得結果</span><span class="sxs-lookup"><span data-stu-id="fb9a5-128">Example 2: Get a What-If result at subscription scope with ResourceIdOnly</span></span>
```powershell
PS C:\> Get-AzDeploymentWhatIfResult `
    -DeploymentName "deploy-01" `
    -Location "West US" `
    -TemplateFile "D:\Azure\Templates\ServiceTemplate.json" `
    -TemplateParameterFile "D:\Azure\Templates\ServiceParameters.json" `
    -ResultFormat "ResourceIdOnly"
```

<span data-ttu-id="fb9a5-129">此命令會使用What-If範本檔案和磁片上的參數檔案，以取得目前訂閱範圍中的結果。</span><span class="sxs-lookup"><span data-stu-id="fb9a5-129">This command gets a What-If result at the current subscription scope by using a custom template file and a parameter file on disk.</span></span>
<span data-ttu-id="fb9a5-130">命令會使用 *Location* 參數指定儲存部署資料的位置。</span><span class="sxs-lookup"><span data-stu-id="fb9a5-130">The command uses the *Location* parameter to specify where to store the deployment data.</span></span>
<span data-ttu-id="fb9a5-131">該命令使用 *TemplateFile* 參數來指定範本檔案。</span><span class="sxs-lookup"><span data-stu-id="fb9a5-131">The command uses the *TemplateFile* parameter to specify a template file.</span></span>
<span data-ttu-id="fb9a5-132">該命令使用 *TemplateParameterFile* 參數來指定範本參數檔案。</span><span class="sxs-lookup"><span data-stu-id="fb9a5-132">The command uses the *TemplateParameterFile* parameter to specify a template parameter file.</span></span>
<span data-ttu-id="fb9a5-133">命令使用 *ResultFormat* 參數，將結果What-If只包含資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="fb9a5-133">The command uses the *ResultFormat* parameter to set the What-If result to only contain resource IDs.</span></span>

## <span data-ttu-id="fb9a5-134">參數</span><span class="sxs-lookup"><span data-stu-id="fb9a5-134">PARAMETERS</span></span>

### <span data-ttu-id="fb9a5-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fb9a5-135">-DefaultProfile</span></span>
<span data-ttu-id="fb9a5-136">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="fb9a5-136">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fb9a5-137">-ExcludeChangeType</span><span class="sxs-lookup"><span data-stu-id="fb9a5-137">-ExcludeChangeType</span></span>
<span data-ttu-id="fb9a5-138">要排除在結果中之資源變更類型的逗號分隔What-If清單。</span><span class="sxs-lookup"><span data-stu-id="fb9a5-138">Comma-separated list of resource change types to be excluded from What-If results.</span></span>

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

### <span data-ttu-id="fb9a5-139">-位置</span><span class="sxs-lookup"><span data-stu-id="fb9a5-139">-Location</span></span>
<span data-ttu-id="fb9a5-140">儲存部署資料的位置。</span><span class="sxs-lookup"><span data-stu-id="fb9a5-140">The location to store deployment data.</span></span>

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

### <span data-ttu-id="fb9a5-141">-名稱</span><span class="sxs-lookup"><span data-stu-id="fb9a5-141">-Name</span></span>
<span data-ttu-id="fb9a5-142">要建立之部署的名稱。</span><span class="sxs-lookup"><span data-stu-id="fb9a5-142">The name of the deployment it's going to create.</span></span> <span data-ttu-id="fb9a5-143">如果未指定，則提供範本檔案時預設為範本檔案名;預設為提供範本物件的目前時間，例如"20131223140835"。</span><span class="sxs-lookup"><span data-stu-id="fb9a5-143">If not specified, defaults to the template file name when a template file is provided; defaults to the current time when a template object is provided, e.g. "20131223140835".</span></span>

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

### <span data-ttu-id="fb9a5-144">-Pre</span><span class="sxs-lookup"><span data-stu-id="fb9a5-144">-Pre</span></span>
<span data-ttu-id="fb9a5-145">設定之後，表示當系統自動決定要使用哪個版本時，Cmdlet 應該使用測試版 API 版本。</span><span class="sxs-lookup"><span data-stu-id="fb9a5-145">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="fb9a5-146">-ResultFormat</span><span class="sxs-lookup"><span data-stu-id="fb9a5-146">-ResultFormat</span></span>
<span data-ttu-id="fb9a5-147">此What-If格式。</span><span class="sxs-lookup"><span data-stu-id="fb9a5-147">The What-If result format.</span></span>

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

### <span data-ttu-id="fb9a5-148">-SkipTemplateParameterPrompt</span><span class="sxs-lookup"><span data-stu-id="fb9a5-148">-SkipTemplateParameterPrompt</span></span>
<span data-ttu-id="fb9a5-149">跳過 PowerShell 動態參數處理，檢查所提供的範本參數是否包含範本使用的所有必要參數。</span><span class="sxs-lookup"><span data-stu-id="fb9a5-149">Skips the PowerShell dynamic parameter processing that checks if the provided template parameter contains all necessary parameters used by the template.</span></span>
<span data-ttu-id="fb9a5-150">這項檢查會提示使用者提供遺失參數的值，但若發現參數未系在範本中，則提供 -SkipTemplateParameterPrompt 會忽略此提示並立即錯誤。</span><span class="sxs-lookup"><span data-stu-id="fb9a5-150">This check would prompt the user to provide a value for the missing parameters, but providing the -SkipTemplateParameterPrompt will ignore this prompt and error out immediately if a parameter was found not to be bound in the template.</span></span>
<span data-ttu-id="fb9a5-151">針對非互動式腳本，您可以提供 -SkipTemplateParameterPrompt，以在未滿足所有所需參數的情況下提供更佳的錯誤訊息。</span><span class="sxs-lookup"><span data-stu-id="fb9a5-151">For non-interactive scripts, -SkipTemplateParameterPrompt can be provided to provide a better error message in the case where not all required parameters are satisfied.</span></span>

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

### <span data-ttu-id="fb9a5-152">-TemplateFile</span><span class="sxs-lookup"><span data-stu-id="fb9a5-152">-TemplateFile</span></span>
<span data-ttu-id="fb9a5-153">範本檔案的當地路徑。</span><span class="sxs-lookup"><span data-stu-id="fb9a5-153">Local path to the template file.</span></span> <span data-ttu-id="fb9a5-154">支援的範本檔案類型：json 和 bicep。</span><span class="sxs-lookup"><span data-stu-id="fb9a5-154">Supported template file type: json and bicep.</span></span>

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

### <span data-ttu-id="fb9a5-155">-TemplateObject</span><span class="sxs-lookup"><span data-stu-id="fb9a5-155">-TemplateObject</span></span>
<span data-ttu-id="fb9a5-156">代表範本的雜湊表格。</span><span class="sxs-lookup"><span data-stu-id="fb9a5-156">A hash table which represents the template.</span></span>

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

### <span data-ttu-id="fb9a5-157">-TemplateParameterFile</span><span class="sxs-lookup"><span data-stu-id="fb9a5-157">-TemplateParameterFile</span></span>
<span data-ttu-id="fb9a5-158">具有範本參數的檔案。</span><span class="sxs-lookup"><span data-stu-id="fb9a5-158">A file that has the template parameters.</span></span>

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

### <span data-ttu-id="fb9a5-159">-TemplateParameterObject</span><span class="sxs-lookup"><span data-stu-id="fb9a5-159">-TemplateParameterObject</span></span>
<span data-ttu-id="fb9a5-160">代表參數的雜湊表格。</span><span class="sxs-lookup"><span data-stu-id="fb9a5-160">A hash table which represents the parameters.</span></span>

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

### <span data-ttu-id="fb9a5-161">-TemplateParameterUri</span><span class="sxs-lookup"><span data-stu-id="fb9a5-161">-TemplateParameterUri</span></span>
<span data-ttu-id="fb9a5-162">Uri 到範本參數檔案。</span><span class="sxs-lookup"><span data-stu-id="fb9a5-162">Uri to the template parameter file.</span></span>

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

### <span data-ttu-id="fb9a5-163">-TemplateUri</span><span class="sxs-lookup"><span data-stu-id="fb9a5-163">-TemplateUri</span></span>
<span data-ttu-id="fb9a5-164">Uri 到範本檔案。</span><span class="sxs-lookup"><span data-stu-id="fb9a5-164">Uri to the template file.</span></span>

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

### <span data-ttu-id="fb9a5-165">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fb9a5-165">CommonParameters</span></span>
<span data-ttu-id="fb9a5-166">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="fb9a5-166">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fb9a5-167">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="fb9a5-167">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fb9a5-168">輸入</span><span class="sxs-lookup"><span data-stu-id="fb9a5-168">INPUTS</span></span>

### <span data-ttu-id="fb9a5-169">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="fb9a5-169">System.Collections.Hashtable</span></span>

### <span data-ttu-id="fb9a5-170">System.String</span><span class="sxs-lookup"><span data-stu-id="fb9a5-170">System.String</span></span>

## <span data-ttu-id="fb9a5-171">輸出</span><span class="sxs-lookup"><span data-stu-id="fb9a5-171">OUTPUTS</span></span>

### <span data-ttu-id="fb9a5-172">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.Deployments.PSWhatIfOperationResult</span><span class="sxs-lookup"><span data-stu-id="fb9a5-172">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.Deployments.PSWhatIfOperationResult</span></span>

## <span data-ttu-id="fb9a5-173">筆記</span><span class="sxs-lookup"><span data-stu-id="fb9a5-173">NOTES</span></span>

## <span data-ttu-id="fb9a5-174">相關連結</span><span class="sxs-lookup"><span data-stu-id="fb9a5-174">RELATED LINKS</span></span>
