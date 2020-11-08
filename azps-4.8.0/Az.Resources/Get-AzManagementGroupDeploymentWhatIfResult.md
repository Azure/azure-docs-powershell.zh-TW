---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azmanagementgroupdeploymentwhatifresult
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzManagementGroupDeploymentWhatIfResult.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzManagementGroupDeploymentWhatIfResult.md
ms.openlocfilehash: 39b652f1e6096f74da8d23baee10cd5b2ce54b6d
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94135670"
---
# <span data-ttu-id="d2c7a-101">Get-AzManagementGroupDeploymentWhatIfResult</span><span class="sxs-lookup"><span data-stu-id="d2c7a-101">Get-AzManagementGroupDeploymentWhatIfResult</span></span>

## <span data-ttu-id="d2c7a-102">摘要</span><span class="sxs-lookup"><span data-stu-id="d2c7a-102">SYNOPSIS</span></span>
<span data-ttu-id="d2c7a-103">取得在管理群組範圍中部署的 ARM 範本 What-If 結果。</span><span class="sxs-lookup"><span data-stu-id="d2c7a-103">Gets an ARM template What-If result for a deployment at management group scope.</span></span> 

## <span data-ttu-id="d2c7a-104">句法</span><span class="sxs-lookup"><span data-stu-id="d2c7a-104">SYNTAX</span></span>

### <span data-ttu-id="d2c7a-105">ByTemplateFileWithNoParameters (預設) </span><span class="sxs-lookup"><span data-stu-id="d2c7a-105">ByTemplateFileWithNoParameters (Default)</span></span>
```
Get-AzManagementGroupDeploymentWhatIfResult [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-ResultFormat <WhatIfResultFormat>] [-ExcludeChangeType <String[]>] -TemplateFile <String>
 [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="d2c7a-106">ByTemplateObjectAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="d2c7a-106">ByTemplateObjectAndParameterObject</span></span>
```
Get-AzManagementGroupDeploymentWhatIfResult [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-ResultFormat <WhatIfResultFormat>] [-ExcludeChangeType <String[]>] -TemplateParameterObject <Hashtable>
 -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d2c7a-107">ByTemplateFileAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="d2c7a-107">ByTemplateFileAndParameterObject</span></span>
```
Get-AzManagementGroupDeploymentWhatIfResult [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-ResultFormat <WhatIfResultFormat>] [-ExcludeChangeType <String[]>] -TemplateParameterObject <Hashtable>
 -TemplateFile <String> [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d2c7a-108">ByTemplateUriAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="d2c7a-108">ByTemplateUriAndParameterObject</span></span>
```
Get-AzManagementGroupDeploymentWhatIfResult [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-ResultFormat <WhatIfResultFormat>] [-ExcludeChangeType <String[]>] -TemplateParameterObject <Hashtable>
 -TemplateUri <String> [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d2c7a-109">ByTemplateObjectAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="d2c7a-109">ByTemplateObjectAndParameterFile</span></span>
```
Get-AzManagementGroupDeploymentWhatIfResult [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-ResultFormat <WhatIfResultFormat>] [-ExcludeChangeType <String[]>] -TemplateParameterFile <String>
 -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d2c7a-110">ByTemplateFileAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="d2c7a-110">ByTemplateFileAndParameterFile</span></span>
```
Get-AzManagementGroupDeploymentWhatIfResult [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-ResultFormat <WhatIfResultFormat>] [-ExcludeChangeType <String[]>] -TemplateParameterFile <String>
 -TemplateFile <String> [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d2c7a-111">ByTemplateUriAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="d2c7a-111">ByTemplateUriAndParameterFile</span></span>
```
Get-AzManagementGroupDeploymentWhatIfResult [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-ResultFormat <WhatIfResultFormat>] [-ExcludeChangeType <String[]>] -TemplateParameterFile <String>
 -TemplateUri <String> [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d2c7a-112">ByTemplateObjectAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="d2c7a-112">ByTemplateObjectAndParameterUri</span></span>
```
Get-AzManagementGroupDeploymentWhatIfResult [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-ResultFormat <WhatIfResultFormat>] [-ExcludeChangeType <String[]>] -TemplateParameterUri <String>
 -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d2c7a-113">ByTemplateFileAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="d2c7a-113">ByTemplateFileAndParameterUri</span></span>
```
Get-AzManagementGroupDeploymentWhatIfResult [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-ResultFormat <WhatIfResultFormat>] [-ExcludeChangeType <String[]>] -TemplateParameterUri <String>
 -TemplateFile <String> [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d2c7a-114">ByTemplateUriAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="d2c7a-114">ByTemplateUriAndParameterUri</span></span>
```
Get-AzManagementGroupDeploymentWhatIfResult [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-ResultFormat <WhatIfResultFormat>] [-ExcludeChangeType <String[]>] -TemplateParameterUri <String>
 -TemplateUri <String> [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d2c7a-115">ByTemplateObjectWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="d2c7a-115">ByTemplateObjectWithNoParameters</span></span>
```
Get-AzManagementGroupDeploymentWhatIfResult [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-ResultFormat <WhatIfResultFormat>] [-ExcludeChangeType <String[]>] -TemplateObject <Hashtable>
 [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="d2c7a-116">ByTemplateUriWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="d2c7a-116">ByTemplateUriWithNoParameters</span></span>
```
Get-AzManagementGroupDeploymentWhatIfResult [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-ResultFormat <WhatIfResultFormat>] [-ExcludeChangeType <String[]>] -TemplateUri <String>
 [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d2c7a-117">說明</span><span class="sxs-lookup"><span data-stu-id="d2c7a-117">DESCRIPTION</span></span>
<span data-ttu-id="d2c7a-118">**AzManagementGroupDeploymentWhatIfResult** Cmdlet 會取得 ARM 範本，What-If 在指定管理群組範圍中部署範本的結果。</span><span class="sxs-lookup"><span data-stu-id="d2c7a-118">The **Get-AzManagementGroupDeploymentWhatIfResult** cmdlet gets the ARM template What-If result for a template deployment at the specified management group scope.</span></span> <span data-ttu-id="d2c7a-119">它會傳回一份變更清單，指出如果應用部署但不會對真實資源進行任何變更，就會更新哪些資源。</span><span class="sxs-lookup"><span data-stu-id="d2c7a-119">It returns a list of changes indicating what resources will be updated if the deployment is applied without making any changes to real resources.</span></span> <span data-ttu-id="d2c7a-120">若要指定傳回結果的格式，請使用 *ResultFormat* 參數。</span><span class="sxs-lookup"><span data-stu-id="d2c7a-120">To specify the format for the returning result, use the *ResultFormat* parameter.</span></span>

## <span data-ttu-id="d2c7a-121">示例</span><span class="sxs-lookup"><span data-stu-id="d2c7a-121">EXAMPLES</span></span>

### <span data-ttu-id="d2c7a-122">範例1：在管理群組範圍中取得 What-If 結果</span><span class="sxs-lookup"><span data-stu-id="d2c7a-122">Example 1: Get a What-If result at management group scope</span></span>
```powershell
PS C:\> Get-AzManagementGroupDeploymentWhatIfResult `
    -DeploymentName "deploy-01" `
    -Location "West US" `
    -ManagementGroupId "myManagementGroup" `
    -TemplateFile "D:\Azure\Templates\ServiceTemplate.json" `
    -TemplateParameterFile "D:\Azure\Templates\ServiceParameters.json" `
    -ResultFormat "FullResourcePayloads"
```

<span data-ttu-id="d2c7a-123">這個命令會使用自訂範本檔案和磁片上的參數檔案，在管理群組範圍中取得 What-If 的結果。</span><span class="sxs-lookup"><span data-stu-id="d2c7a-123">This command gets a What-If result at management group scope by using a custom template file and a parameter file on disk.</span></span>
<span data-ttu-id="d2c7a-124">此命令會使用 *Location* 參數指定要儲存部署資料的位置。</span><span class="sxs-lookup"><span data-stu-id="d2c7a-124">The command uses the *Location* parameter to specify where to store the deployment data.</span></span>
<span data-ttu-id="d2c7a-125">此命令會使用 *ManagementGroupId* 參數來指定要部署範本的管理群組。</span><span class="sxs-lookup"><span data-stu-id="d2c7a-125">The command uses the *ManagementGroupId* parameter to specify the management group where the template will be deployed.</span></span>
<span data-ttu-id="d2c7a-126">此命令使用 *TemplateFile* 參數來指定範本檔案。</span><span class="sxs-lookup"><span data-stu-id="d2c7a-126">The command uses the *TemplateFile* parameter to specify a template file.</span></span>
<span data-ttu-id="d2c7a-127">此命令會使用 *TemplateParameterFile* 參數來指定範本參數檔。</span><span class="sxs-lookup"><span data-stu-id="d2c7a-127">The command uses the *TemplateParameterFile* parameter to specify a template parameter file.</span></span>
<span data-ttu-id="d2c7a-128">此命令會使用 *ResultFormat* 參數來設定 What-If 結果，以包含完整的資源載荷。</span><span class="sxs-lookup"><span data-stu-id="d2c7a-128">The command uses the *ResultFormat* parameter to set the What-If result to include full resource payloads.</span></span>

### <span data-ttu-id="d2c7a-129">範例2：使用 ResourceIdOnly 在管理群組範圍中取得 What-If 結果</span><span class="sxs-lookup"><span data-stu-id="d2c7a-129">Example 2: Get a What-If result at management group scope with ResourceIdOnly</span></span>
```powershell
PS C:\> Get-AzManagementGroupDeploymentWhatIfResult `
    -DeploymentName "deploy-01" `
    -Location "West US" `
    -ManagementGroupId "myManagementGroup" `
    -TemplateFile "D:\Azure\Templates\ServiceTemplate.json" `
    -TemplateParameterFile "D:\Azure\Templates\ServiceParameters.json" `
    -ResultFormat "ResourceIdOnly"
```

<span data-ttu-id="d2c7a-130">這個命令會使用自訂範本檔案和磁片上的參數檔案，在管理群組範圍中取得 What-If 的結果。</span><span class="sxs-lookup"><span data-stu-id="d2c7a-130">This command gets a What-If result at management group scope by using a custom template file and a parameter file on disk.</span></span>
<span data-ttu-id="d2c7a-131">此命令會使用 *Location* 參數指定要儲存部署資料的位置。</span><span class="sxs-lookup"><span data-stu-id="d2c7a-131">The command uses the *Location* parameter to specify where to store the deployment data.</span></span>
<span data-ttu-id="d2c7a-132">此命令會使用 *ManagementGroupId* 參數來指定要部署範本的管理群組。</span><span class="sxs-lookup"><span data-stu-id="d2c7a-132">The command uses the *ManagementGroupId* parameter to specify the management group where the template will be deployed.</span></span>
<span data-ttu-id="d2c7a-133">此命令使用 *TemplateFile* 參數來指定範本檔案。</span><span class="sxs-lookup"><span data-stu-id="d2c7a-133">The command uses the *TemplateFile* parameter to specify a template file.</span></span>
<span data-ttu-id="d2c7a-134">此命令會使用 *TemplateParameterFile* 參數來指定範本參數檔。</span><span class="sxs-lookup"><span data-stu-id="d2c7a-134">The command uses the *TemplateParameterFile* parameter to specify a template parameter file.</span></span>
<span data-ttu-id="d2c7a-135">此命令會使用 *ResultFormat* 參數，將 What-If 結果設定為僅包含資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="d2c7a-135">The command uses the *ResultFormat* parameter to set the What-If result to only contain resource IDs.</span></span>

## <span data-ttu-id="d2c7a-136">參數</span><span class="sxs-lookup"><span data-stu-id="d2c7a-136">PARAMETERS</span></span>

### <span data-ttu-id="d2c7a-137">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="d2c7a-137">-ApiVersion</span></span>
<span data-ttu-id="d2c7a-138">設定時，會指出要使用的資源提供者 API 版本。</span><span class="sxs-lookup"><span data-stu-id="d2c7a-138">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="d2c7a-139">如果未指定，API 版本會自動決定為最新的可用。</span><span class="sxs-lookup"><span data-stu-id="d2c7a-139">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="d2c7a-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d2c7a-140">-DefaultProfile</span></span>
<span data-ttu-id="d2c7a-141">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="d2c7a-141">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d2c7a-142">-ExcludeChangeType</span><span class="sxs-lookup"><span data-stu-id="d2c7a-142">-ExcludeChangeType</span></span>
<span data-ttu-id="d2c7a-143">要從 What-If 結果中排除的資源變更類型清單（以逗號分隔）。</span><span class="sxs-lookup"><span data-stu-id="d2c7a-143">Comma-separated list of resource change types to be excluded from What-If results.</span></span>

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

### <span data-ttu-id="d2c7a-144">-位置</span><span class="sxs-lookup"><span data-stu-id="d2c7a-144">-Location</span></span>
<span data-ttu-id="d2c7a-145">儲存部署資料的位置。</span><span class="sxs-lookup"><span data-stu-id="d2c7a-145">The location to store deployment data.</span></span>

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

### <span data-ttu-id="d2c7a-146">-ManagementGroupId</span><span class="sxs-lookup"><span data-stu-id="d2c7a-146">-ManagementGroupId</span></span>
<span data-ttu-id="d2c7a-147">管理群組識別碼。</span><span class="sxs-lookup"><span data-stu-id="d2c7a-147">The management group ID.</span></span>

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

### <span data-ttu-id="d2c7a-148">-名稱</span><span class="sxs-lookup"><span data-stu-id="d2c7a-148">-Name</span></span>
<span data-ttu-id="d2c7a-149">將要建立之部署的名稱。</span><span class="sxs-lookup"><span data-stu-id="d2c7a-149">The name of the deployment it's going to create.</span></span>
<span data-ttu-id="d2c7a-150">如果未指定，則預設為提供範本檔時的範本檔案名;預設為提供範本物件的目前時間（例如 "20131223140835"）。</span><span class="sxs-lookup"><span data-stu-id="d2c7a-150">If not specified, defaults to the template file name when a template file is provided; defaults to the current time when a template object is provided, e.g. "20131223140835".</span></span>

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

### <span data-ttu-id="d2c7a-151">-預先</span><span class="sxs-lookup"><span data-stu-id="d2c7a-151">-Pre</span></span>
<span data-ttu-id="d2c7a-152">設定時，表示 Cmdlet 應該使用預發行 API 版本，以便自動判斷要使用的版本。</span><span class="sxs-lookup"><span data-stu-id="d2c7a-152">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="d2c7a-153">-ResultFormat</span><span class="sxs-lookup"><span data-stu-id="d2c7a-153">-ResultFormat</span></span>
<span data-ttu-id="d2c7a-154">What-If 的結果格式。</span><span class="sxs-lookup"><span data-stu-id="d2c7a-154">The What-If result format.</span></span>

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

### <span data-ttu-id="d2c7a-155">-SkipTemplateParameterPrompt</span><span class="sxs-lookup"><span data-stu-id="d2c7a-155">-SkipTemplateParameterPrompt</span></span>
<span data-ttu-id="d2c7a-156">會跳過 PowerShell 動態參數處理，檢查提供的範本參數是否包含範本所使用的所有必要參數。</span><span class="sxs-lookup"><span data-stu-id="d2c7a-156">Skips the PowerShell dynamic parameter processing that checks if the provided template parameter contains all necessary parameters used by the template.</span></span>
<span data-ttu-id="d2c7a-157">這項檢查會提示使用者提供缺少參數的值，但提供-SkipTemplateParameterPrompt 將會在範本中發現未系結的參數時，立即忽略此提示和錯誤。</span><span class="sxs-lookup"><span data-stu-id="d2c7a-157">This check would prompt the user to provide a value for the missing parameters, but providing the -SkipTemplateParameterPrompt will ignore this prompt and error out immediately if a parameter was found not to be bound in the template.</span></span>
<span data-ttu-id="d2c7a-158">在非互動式腳本中，您可以提供 SkipTemplateParameterPrompt，以在不符合所有必要參數的情況下，提供較佳的錯誤訊息。</span><span class="sxs-lookup"><span data-stu-id="d2c7a-158">For non-interactive scripts, -SkipTemplateParameterPrompt can be provided to provide a better error message in the case where not all required parameters are satisfied.</span></span>

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

### <span data-ttu-id="d2c7a-159">-TemplateFile</span><span class="sxs-lookup"><span data-stu-id="d2c7a-159">-TemplateFile</span></span>
<span data-ttu-id="d2c7a-160">範本檔案的本機路徑。</span><span class="sxs-lookup"><span data-stu-id="d2c7a-160">Local path to the template file.</span></span>

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

### <span data-ttu-id="d2c7a-161">-TemplateObject</span><span class="sxs-lookup"><span data-stu-id="d2c7a-161">-TemplateObject</span></span>
<span data-ttu-id="d2c7a-162">代表範本的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="d2c7a-162">A hash table which represents the template.</span></span>

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

### <span data-ttu-id="d2c7a-163">-TemplateParameterFile</span><span class="sxs-lookup"><span data-stu-id="d2c7a-163">-TemplateParameterFile</span></span>
<span data-ttu-id="d2c7a-164">具有範本參數的檔案。</span><span class="sxs-lookup"><span data-stu-id="d2c7a-164">A file that has the template parameters.</span></span>

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

### <span data-ttu-id="d2c7a-165">-TemplateParameterObject</span><span class="sxs-lookup"><span data-stu-id="d2c7a-165">-TemplateParameterObject</span></span>
<span data-ttu-id="d2c7a-166">代表參數的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="d2c7a-166">A hash table which represents the parameters.</span></span>

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

### <span data-ttu-id="d2c7a-167">-TemplateParameterUri</span><span class="sxs-lookup"><span data-stu-id="d2c7a-167">-TemplateParameterUri</span></span>
<span data-ttu-id="d2c7a-168">範本參數檔的 Uri。</span><span class="sxs-lookup"><span data-stu-id="d2c7a-168">Uri to the template parameter file.</span></span>

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

### <span data-ttu-id="d2c7a-169">-TemplateUri</span><span class="sxs-lookup"><span data-stu-id="d2c7a-169">-TemplateUri</span></span>
<span data-ttu-id="d2c7a-170">範本檔案的 Uri。</span><span class="sxs-lookup"><span data-stu-id="d2c7a-170">Uri to the template file.</span></span>

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

### <span data-ttu-id="d2c7a-171">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d2c7a-171">CommonParameters</span></span>
<span data-ttu-id="d2c7a-172">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="d2c7a-172">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d2c7a-173">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="d2c7a-173">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d2c7a-174">輸入</span><span class="sxs-lookup"><span data-stu-id="d2c7a-174">INPUTS</span></span>

### <span data-ttu-id="d2c7a-175">System.object</span><span class="sxs-lookup"><span data-stu-id="d2c7a-175">System.String</span></span>

### <span data-ttu-id="d2c7a-176">[System.object] 集合. Hashtable</span><span class="sxs-lookup"><span data-stu-id="d2c7a-176">System.Collections.Hashtable</span></span>

## <span data-ttu-id="d2c7a-177">輸出</span><span class="sxs-lookup"><span data-stu-id="d2c7a-177">OUTPUTS</span></span>

### <span data-ttu-id="d2c7a-178">PSWhatIfOperationResult 中的 SdkModels，然後再</span><span class="sxs-lookup"><span data-stu-id="d2c7a-178">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.Deployments.PSWhatIfOperationResult</span></span>

## <span data-ttu-id="d2c7a-179">筆記</span><span class="sxs-lookup"><span data-stu-id="d2c7a-179">NOTES</span></span>

## <span data-ttu-id="d2c7a-180">相關連結</span><span class="sxs-lookup"><span data-stu-id="d2c7a-180">RELATED LINKS</span></span>