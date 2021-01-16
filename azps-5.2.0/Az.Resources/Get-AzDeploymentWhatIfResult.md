---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azdeploymentwhatifresult
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzDeploymentWhatIfResult.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzDeploymentWhatIfResult.md
ms.openlocfilehash: 0ad3df8e010beec777bd059bbef708774570792d
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98273879"
---
# <span data-ttu-id="5676f-101">Get-AzDeploymentWhatIfResult</span><span class="sxs-lookup"><span data-stu-id="5676f-101">Get-AzDeploymentWhatIfResult</span></span>

## <span data-ttu-id="5676f-102">摘要</span><span class="sxs-lookup"><span data-stu-id="5676f-102">SYNOPSIS</span></span>
<span data-ttu-id="5676f-103">取得在訂閱範圍中部署的 ARM 範本 What-If 結果。</span><span class="sxs-lookup"><span data-stu-id="5676f-103">Gets an ARM template What-If result for a deployment at subscription scope.</span></span> 

## <span data-ttu-id="5676f-104">句法</span><span class="sxs-lookup"><span data-stu-id="5676f-104">SYNTAX</span></span>

### <span data-ttu-id="5676f-105">ByTemplateFileWithNoParameters (預設) </span><span class="sxs-lookup"><span data-stu-id="5676f-105">ByTemplateFileWithNoParameters (Default)</span></span>
```
Get-AzDeploymentWhatIfResult [-Name <String>] -Location <String> [-ResultFormat <WhatIfResultFormat>]
 [-ExcludeChangeType <String[]>] -TemplateFile <String> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5676f-106">ByTemplateObjectAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="5676f-106">ByTemplateObjectAndParameterObject</span></span>
```
Get-AzDeploymentWhatIfResult [-Name <String>] -Location <String> [-ResultFormat <WhatIfResultFormat>]
 [-ExcludeChangeType <String[]>] -TemplateParameterObject <Hashtable> -TemplateObject <Hashtable>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5676f-107">ByTemplateFileAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="5676f-107">ByTemplateFileAndParameterObject</span></span>
```
Get-AzDeploymentWhatIfResult [-Name <String>] -Location <String> [-ResultFormat <WhatIfResultFormat>]
 [-ExcludeChangeType <String[]>] -TemplateParameterObject <Hashtable> -TemplateFile <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5676f-108">ByTemplateUriAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="5676f-108">ByTemplateUriAndParameterObject</span></span>
```
Get-AzDeploymentWhatIfResult [-Name <String>] -Location <String> [-ResultFormat <WhatIfResultFormat>]
 [-ExcludeChangeType <String[]>] -TemplateParameterObject <Hashtable> -TemplateUri <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5676f-109">ByTemplateObjectAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="5676f-109">ByTemplateObjectAndParameterFile</span></span>
```
Get-AzDeploymentWhatIfResult [-Name <String>] -Location <String> [-ResultFormat <WhatIfResultFormat>]
 [-ExcludeChangeType <String[]>] -TemplateParameterFile <String> -TemplateObject <Hashtable>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5676f-110">ByTemplateFileAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="5676f-110">ByTemplateFileAndParameterFile</span></span>
```
Get-AzDeploymentWhatIfResult [-Name <String>] -Location <String> [-ResultFormat <WhatIfResultFormat>]
 [-ExcludeChangeType <String[]>] -TemplateParameterFile <String> -TemplateFile <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5676f-111">ByTemplateUriAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="5676f-111">ByTemplateUriAndParameterFile</span></span>
```
Get-AzDeploymentWhatIfResult [-Name <String>] -Location <String> [-ResultFormat <WhatIfResultFormat>]
 [-ExcludeChangeType <String[]>] -TemplateParameterFile <String> -TemplateUri <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5676f-112">ByTemplateObjectAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="5676f-112">ByTemplateObjectAndParameterUri</span></span>
```
Get-AzDeploymentWhatIfResult [-Name <String>] -Location <String> [-ResultFormat <WhatIfResultFormat>]
 [-ExcludeChangeType <String[]>] -TemplateParameterUri <String> -TemplateObject <Hashtable>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5676f-113">ByTemplateFileAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="5676f-113">ByTemplateFileAndParameterUri</span></span>
```
Get-AzDeploymentWhatIfResult [-Name <String>] -Location <String> [-ResultFormat <WhatIfResultFormat>]
 [-ExcludeChangeType <String[]>] -TemplateParameterUri <String> -TemplateFile <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5676f-114">ByTemplateUriAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="5676f-114">ByTemplateUriAndParameterUri</span></span>
```
Get-AzDeploymentWhatIfResult [-Name <String>] -Location <String> [-ResultFormat <WhatIfResultFormat>]
 [-ExcludeChangeType <String[]>] -TemplateParameterUri <String> -TemplateUri <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5676f-115">ByTemplateObjectWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="5676f-115">ByTemplateObjectWithNoParameters</span></span>
```
Get-AzDeploymentWhatIfResult [-Name <String>] -Location <String> [-ResultFormat <WhatIfResultFormat>]
 [-ExcludeChangeType <String[]>] -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5676f-116">ByTemplateUriWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="5676f-116">ByTemplateUriWithNoParameters</span></span>
```
Get-AzDeploymentWhatIfResult [-Name <String>] -Location <String> [-ResultFormat <WhatIfResultFormat>]
 [-ExcludeChangeType <String[]>] -TemplateUri <String> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5676f-117">說明</span><span class="sxs-lookup"><span data-stu-id="5676f-117">DESCRIPTION</span></span>
<span data-ttu-id="5676f-118">**AzDeploymentWhatIfResult** Cmdlet 會取得 ARM 範本，What-If 在目前訂閱範圍中部署範本的結果。</span><span class="sxs-lookup"><span data-stu-id="5676f-118">The **Get-AzDeploymentWhatIfResult** cmdlet gets the ARM template What-If result for a template deployment at the current subscription scope.</span></span> <span data-ttu-id="5676f-119">它會傳回一份變更清單，指出如果應用部署但不會對真實資源進行任何變更，就會更新哪些資源。</span><span class="sxs-lookup"><span data-stu-id="5676f-119">It returns a list of changes indicating what resources will be updated if the deployment is applied without making any changes to real resources.</span></span> <span data-ttu-id="5676f-120">若要指定傳回結果的格式，請使用 *ResultFormat* 參數。</span><span class="sxs-lookup"><span data-stu-id="5676f-120">To specify the format for the returning result, use the *ResultFormat* parameter.</span></span>

## <span data-ttu-id="5676f-121">示例</span><span class="sxs-lookup"><span data-stu-id="5676f-121">EXAMPLES</span></span>

### <span data-ttu-id="5676f-122">範例1：在訂閱範圍中取得 What-If 結果</span><span class="sxs-lookup"><span data-stu-id="5676f-122">Example 1: Get a What-If result at subscription scope</span></span>
```powershell
PS C:\> Get-AzDeploymentWhatIfResult `
    -DeploymentName "deploy-01" `
    -Location "West US" `
    -TemplateFile "D:\Azure\Templates\ServiceTemplate.json" `
    -TemplateParameterFile "D:\Azure\Templates\ServiceParameters.json" `
    -ResultFormat "FullResourcePayloads"
```

<span data-ttu-id="5676f-123">這個命令會使用自訂範本檔案和磁片上的參數檔案，在目前訂閱範圍中取得 What-If 結果。</span><span class="sxs-lookup"><span data-stu-id="5676f-123">This command gets a What-If result at the current subscription scope by using a custom template file and a parameter file on disk.</span></span>
<span data-ttu-id="5676f-124">此命令會使用 *Location* 參數指定要儲存部署資料的位置。</span><span class="sxs-lookup"><span data-stu-id="5676f-124">The command uses the *Location* parameter to specify where to store the deployment data.</span></span>
<span data-ttu-id="5676f-125">此命令使用 *TemplateFile* 參數來指定範本檔案。</span><span class="sxs-lookup"><span data-stu-id="5676f-125">The command uses the *TemplateFile* parameter to specify a template file.</span></span>
<span data-ttu-id="5676f-126">此命令會使用 *TemplateParameterFile* 參數來指定範本參數檔。</span><span class="sxs-lookup"><span data-stu-id="5676f-126">The command uses the *TemplateParameterFile* parameter to specify a template parameter file.</span></span>
<span data-ttu-id="5676f-127">此命令會使用 *ResultFormat* 參數來設定 What-If 結果，以包含完整的資源載荷。</span><span class="sxs-lookup"><span data-stu-id="5676f-127">The command uses the *ResultFormat* parameter to set the What-If result to include full resource payloads.</span></span>

### <span data-ttu-id="5676f-128">範例2：使用 ResourceIdOnly 在訂閱範圍中取得 What-If 結果</span><span class="sxs-lookup"><span data-stu-id="5676f-128">Example 2: Get a What-If result at subscription scope with ResourceIdOnly</span></span>
```powershell
PS C:\> Get-AzDeploymentWhatIfResult `
    -DeploymentName "deploy-01" `
    -Location "West US" `
    -TemplateFile "D:\Azure\Templates\ServiceTemplate.json" `
    -TemplateParameterFile "D:\Azure\Templates\ServiceParameters.json" `
    -ResultFormat "ResourceIdOnly"
```

<span data-ttu-id="5676f-129">這個命令會使用自訂範本檔案和磁片上的參數檔案，在目前訂閱範圍中取得 What-If 結果。</span><span class="sxs-lookup"><span data-stu-id="5676f-129">This command gets a What-If result at the current subscription scope by using a custom template file and a parameter file on disk.</span></span>
<span data-ttu-id="5676f-130">此命令會使用 *Location* 參數指定要儲存部署資料的位置。</span><span class="sxs-lookup"><span data-stu-id="5676f-130">The command uses the *Location* parameter to specify where to store the deployment data.</span></span>
<span data-ttu-id="5676f-131">此命令使用 *TemplateFile* 參數來指定範本檔案。</span><span class="sxs-lookup"><span data-stu-id="5676f-131">The command uses the *TemplateFile* parameter to specify a template file.</span></span>
<span data-ttu-id="5676f-132">此命令會使用 *TemplateParameterFile* 參數來指定範本參數檔。</span><span class="sxs-lookup"><span data-stu-id="5676f-132">The command uses the *TemplateParameterFile* parameter to specify a template parameter file.</span></span>
<span data-ttu-id="5676f-133">此命令會使用 *ResultFormat* 參數，將 What-If 結果設定為僅包含資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="5676f-133">The command uses the *ResultFormat* parameter to set the What-If result to only contain resource IDs.</span></span>

## <span data-ttu-id="5676f-134">參數</span><span class="sxs-lookup"><span data-stu-id="5676f-134">PARAMETERS</span></span>

### <span data-ttu-id="5676f-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5676f-135">-DefaultProfile</span></span>
<span data-ttu-id="5676f-136">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="5676f-136">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5676f-137">-ExcludeChangeType</span><span class="sxs-lookup"><span data-stu-id="5676f-137">-ExcludeChangeType</span></span>
<span data-ttu-id="5676f-138">要從 What-If 結果中排除的資源變更類型清單（以逗號分隔）。</span><span class="sxs-lookup"><span data-stu-id="5676f-138">Comma-separated list of resource change types to be excluded from What-If results.</span></span>

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

### <span data-ttu-id="5676f-139">-位置</span><span class="sxs-lookup"><span data-stu-id="5676f-139">-Location</span></span>
<span data-ttu-id="5676f-140">儲存部署資料的位置。</span><span class="sxs-lookup"><span data-stu-id="5676f-140">The location to store deployment data.</span></span>

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

### <span data-ttu-id="5676f-141">-名稱</span><span class="sxs-lookup"><span data-stu-id="5676f-141">-Name</span></span>
<span data-ttu-id="5676f-142">將要建立之部署的名稱。</span><span class="sxs-lookup"><span data-stu-id="5676f-142">The name of the deployment it's going to create.</span></span> <span data-ttu-id="5676f-143">如果未指定，則預設為提供範本檔時的範本檔案名;預設為提供範本物件的目前時間（例如 "20131223140835"）。</span><span class="sxs-lookup"><span data-stu-id="5676f-143">If not specified, defaults to the template file name when a template file is provided; defaults to the current time when a template object is provided, e.g. "20131223140835".</span></span>

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

### <span data-ttu-id="5676f-144">-預先</span><span class="sxs-lookup"><span data-stu-id="5676f-144">-Pre</span></span>
<span data-ttu-id="5676f-145">設定時，表示 Cmdlet 應該使用預發行 API 版本，以便自動判斷要使用的版本。</span><span class="sxs-lookup"><span data-stu-id="5676f-145">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="5676f-146">-ResultFormat</span><span class="sxs-lookup"><span data-stu-id="5676f-146">-ResultFormat</span></span>
<span data-ttu-id="5676f-147">What-If 的結果格式。</span><span class="sxs-lookup"><span data-stu-id="5676f-147">The What-If result format.</span></span>

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

### <span data-ttu-id="5676f-148">-SkipTemplateParameterPrompt</span><span class="sxs-lookup"><span data-stu-id="5676f-148">-SkipTemplateParameterPrompt</span></span>
<span data-ttu-id="5676f-149">會跳過 PowerShell 動態參數處理，檢查提供的範本參數是否包含範本所使用的所有必要參數。</span><span class="sxs-lookup"><span data-stu-id="5676f-149">Skips the PowerShell dynamic parameter processing that checks if the provided template parameter contains all necessary parameters used by the template.</span></span>
<span data-ttu-id="5676f-150">這項檢查會提示使用者提供缺少參數的值，但提供-SkipTemplateParameterPrompt 將會在範本中發現未系結的參數時，立即忽略此提示和錯誤。</span><span class="sxs-lookup"><span data-stu-id="5676f-150">This check would prompt the user to provide a value for the missing parameters, but providing the -SkipTemplateParameterPrompt will ignore this prompt and error out immediately if a parameter was found not to be bound in the template.</span></span>
<span data-ttu-id="5676f-151">在非互動式腳本中，您可以提供 SkipTemplateParameterPrompt，以在不符合所有必要參數的情況下，提供較佳的錯誤訊息。</span><span class="sxs-lookup"><span data-stu-id="5676f-151">For non-interactive scripts, -SkipTemplateParameterPrompt can be provided to provide a better error message in the case where not all required parameters are satisfied.</span></span>

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

### <span data-ttu-id="5676f-152">-TemplateFile</span><span class="sxs-lookup"><span data-stu-id="5676f-152">-TemplateFile</span></span>
<span data-ttu-id="5676f-153">範本檔案的本機路徑。</span><span class="sxs-lookup"><span data-stu-id="5676f-153">Local path to the template file.</span></span>

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

### <span data-ttu-id="5676f-154">-TemplateObject</span><span class="sxs-lookup"><span data-stu-id="5676f-154">-TemplateObject</span></span>
<span data-ttu-id="5676f-155">代表範本的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="5676f-155">A hash table which represents the template.</span></span>

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

### <span data-ttu-id="5676f-156">-TemplateParameterFile</span><span class="sxs-lookup"><span data-stu-id="5676f-156">-TemplateParameterFile</span></span>
<span data-ttu-id="5676f-157">具有範本參數的檔案。</span><span class="sxs-lookup"><span data-stu-id="5676f-157">A file that has the template parameters.</span></span>

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

### <span data-ttu-id="5676f-158">-TemplateParameterObject</span><span class="sxs-lookup"><span data-stu-id="5676f-158">-TemplateParameterObject</span></span>
<span data-ttu-id="5676f-159">代表參數的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="5676f-159">A hash table which represents the parameters.</span></span>

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

### <span data-ttu-id="5676f-160">-TemplateParameterUri</span><span class="sxs-lookup"><span data-stu-id="5676f-160">-TemplateParameterUri</span></span>
<span data-ttu-id="5676f-161">範本參數檔的 Uri。</span><span class="sxs-lookup"><span data-stu-id="5676f-161">Uri to the template parameter file.</span></span>

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

### <span data-ttu-id="5676f-162">-TemplateUri</span><span class="sxs-lookup"><span data-stu-id="5676f-162">-TemplateUri</span></span>
<span data-ttu-id="5676f-163">範本檔案的 Uri。</span><span class="sxs-lookup"><span data-stu-id="5676f-163">Uri to the template file.</span></span>

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

### <span data-ttu-id="5676f-164">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5676f-164">CommonParameters</span></span>
<span data-ttu-id="5676f-165">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="5676f-165">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5676f-166">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="5676f-166">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5676f-167">輸入</span><span class="sxs-lookup"><span data-stu-id="5676f-167">INPUTS</span></span>

### <span data-ttu-id="5676f-168">[System.object] 集合. Hashtable</span><span class="sxs-lookup"><span data-stu-id="5676f-168">System.Collections.Hashtable</span></span>

### <span data-ttu-id="5676f-169">System.object</span><span class="sxs-lookup"><span data-stu-id="5676f-169">System.String</span></span>

## <span data-ttu-id="5676f-170">輸出</span><span class="sxs-lookup"><span data-stu-id="5676f-170">OUTPUTS</span></span>

### <span data-ttu-id="5676f-171">PSWhatIfOperationResult 中的 SdkModels，然後再</span><span class="sxs-lookup"><span data-stu-id="5676f-171">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.Deployments.PSWhatIfOperationResult</span></span>

## <span data-ttu-id="5676f-172">筆記</span><span class="sxs-lookup"><span data-stu-id="5676f-172">NOTES</span></span>

## <span data-ttu-id="5676f-173">相關連結</span><span class="sxs-lookup"><span data-stu-id="5676f-173">RELATED LINKS</span></span>
