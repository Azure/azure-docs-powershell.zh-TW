---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azresourcegroupdeploymentwhatifresult
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzResourceGroupDeploymentWhatIfResult.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzResourceGroupDeploymentWhatIfResult.md
ms.openlocfilehash: 09b0a1a6691b4c3d491d15d226fb8260fb7ae00e
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98278608"
---
# <span data-ttu-id="c08e3-101">Get-AzResourceGroupDeploymentWhatIfResult</span><span class="sxs-lookup"><span data-stu-id="c08e3-101">Get-AzResourceGroupDeploymentWhatIfResult</span></span>

## <span data-ttu-id="c08e3-102">摘要</span><span class="sxs-lookup"><span data-stu-id="c08e3-102">SYNOPSIS</span></span>
<span data-ttu-id="c08e3-103">取得在資源群組範圍中部署的 ARM 範本 What-If 結果。</span><span class="sxs-lookup"><span data-stu-id="c08e3-103">Gets an ARM template What-If result for a deployment at resource group scope.</span></span> 

## <span data-ttu-id="c08e3-104">句法</span><span class="sxs-lookup"><span data-stu-id="c08e3-104">SYNTAX</span></span>

### <span data-ttu-id="c08e3-105">ByTemplateFileWithNoParameters (預設) </span><span class="sxs-lookup"><span data-stu-id="c08e3-105">ByTemplateFileWithNoParameters (Default)</span></span>
```
Get-AzResourceGroupDeploymentWhatIfResult [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-ResultFormat <WhatIfResultFormat>] [-ExcludeChangeType <String[]>] -TemplateFile <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c08e3-106">ByTemplateObjectAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="c08e3-106">ByTemplateObjectAndParameterObject</span></span>
```
Get-AzResourceGroupDeploymentWhatIfResult [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-ResultFormat <WhatIfResultFormat>] [-ExcludeChangeType <String[]>] -TemplateParameterObject <Hashtable>
 -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c08e3-107">ByTemplateFileAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="c08e3-107">ByTemplateFileAndParameterObject</span></span>
```
Get-AzResourceGroupDeploymentWhatIfResult [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-ResultFormat <WhatIfResultFormat>] [-ExcludeChangeType <String[]>] -TemplateParameterObject <Hashtable>
 -TemplateFile <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c08e3-108">ByTemplateUriAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="c08e3-108">ByTemplateUriAndParameterObject</span></span>
```
Get-AzResourceGroupDeploymentWhatIfResult [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-ResultFormat <WhatIfResultFormat>] [-ExcludeChangeType <String[]>] -TemplateParameterObject <Hashtable>
 -TemplateUri <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c08e3-109">ByTemplateObjectAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="c08e3-109">ByTemplateObjectAndParameterFile</span></span>
```
Get-AzResourceGroupDeploymentWhatIfResult [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-ResultFormat <WhatIfResultFormat>] [-ExcludeChangeType <String[]>] -TemplateParameterFile <String>
 -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c08e3-110">ByTemplateFileAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="c08e3-110">ByTemplateFileAndParameterFile</span></span>
```
Get-AzResourceGroupDeploymentWhatIfResult [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-ResultFormat <WhatIfResultFormat>] [-ExcludeChangeType <String[]>] -TemplateParameterFile <String>
 -TemplateFile <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c08e3-111">ByTemplateUriAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="c08e3-111">ByTemplateUriAndParameterFile</span></span>
```
Get-AzResourceGroupDeploymentWhatIfResult [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-ResultFormat <WhatIfResultFormat>] [-ExcludeChangeType <String[]>] -TemplateParameterFile <String>
 -TemplateUri <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c08e3-112">ByTemplateObjectAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="c08e3-112">ByTemplateObjectAndParameterUri</span></span>
```
Get-AzResourceGroupDeploymentWhatIfResult [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-ResultFormat <WhatIfResultFormat>] [-ExcludeChangeType <String[]>] -TemplateParameterUri <String>
 -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c08e3-113">ByTemplateFileAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="c08e3-113">ByTemplateFileAndParameterUri</span></span>
```
Get-AzResourceGroupDeploymentWhatIfResult [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-ResultFormat <WhatIfResultFormat>] [-ExcludeChangeType <String[]>] -TemplateParameterUri <String>
 -TemplateFile <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c08e3-114">ByTemplateUriAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="c08e3-114">ByTemplateUriAndParameterUri</span></span>
```
Get-AzResourceGroupDeploymentWhatIfResult [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-ResultFormat <WhatIfResultFormat>] [-ExcludeChangeType <String[]>] -TemplateParameterUri <String>
 -TemplateUri <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c08e3-115">ByTemplateObjectWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="c08e3-115">ByTemplateObjectWithNoParameters</span></span>
```
Get-AzResourceGroupDeploymentWhatIfResult [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-ResultFormat <WhatIfResultFormat>] [-ExcludeChangeType <String[]>] -TemplateObject <Hashtable>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c08e3-116">ByTemplateUriWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="c08e3-116">ByTemplateUriWithNoParameters</span></span>
```
Get-AzResourceGroupDeploymentWhatIfResult [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-ResultFormat <WhatIfResultFormat>] [-ExcludeChangeType <String[]>] -TemplateUri <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c08e3-117">說明</span><span class="sxs-lookup"><span data-stu-id="c08e3-117">DESCRIPTION</span></span>
<span data-ttu-id="c08e3-118">**AzResourceGroupDeploymentWhatIfResult** Cmdlet 會取得 ARM 範本，What-If 在指定的資源群組範圍中部署範本的結果。</span><span class="sxs-lookup"><span data-stu-id="c08e3-118">The **Get-AzResourceGroupDeploymentWhatIfResult** cmdlet gets the ARM template What-If result for a template deployment at the specified resource group scope.</span></span> <span data-ttu-id="c08e3-119">它會傳回一份變更清單，指出如果應用部署但不會對真實資源進行任何變更，就會更新哪些資源。</span><span class="sxs-lookup"><span data-stu-id="c08e3-119">It returns a list of changes indicating what resources will be updated if the deployment is applied without making any changes to real resources.</span></span> <span data-ttu-id="c08e3-120">若要指定傳回結果的格式，請使用 *ResultFormat* 參數。</span><span class="sxs-lookup"><span data-stu-id="c08e3-120">To specify the format for the returning result, use the *ResultFormat* parameter.</span></span>

## <span data-ttu-id="c08e3-121">示例</span><span class="sxs-lookup"><span data-stu-id="c08e3-121">EXAMPLES</span></span>

### <span data-ttu-id="c08e3-122">範例1：在資源群組範圍中取得 What-If 結果</span><span class="sxs-lookup"><span data-stu-id="c08e3-122">Example 1: Get a What-If result at resource group scope</span></span>
```powershell
PS C:\> Get-AzResourceGroupDeploymentWhatIfResult `
    -DeploymentName "deploy-01" `
    -ResourceGroupName "myRG1" `
    -TemplateFile "D:\Azure\Templates\ServiceTemplate.json" `
    -TemplateParameterFile "D:\Azure\Templates\ServiceParameters.json" `
    -ResultFormat "FullResourcePayloads"
```

<span data-ttu-id="c08e3-123">這個命令會使用自訂範本檔案和磁片上的參數檔案，在指定的資源群組範圍中取得 What-If 結果。</span><span class="sxs-lookup"><span data-stu-id="c08e3-123">This command gets a What-If result at the specified resource group scope by using a custom template file and a parameter file on disk.</span></span>
<span data-ttu-id="c08e3-124">此命令會使用 *ResourceGroupName* 參數來指定要部署範本的資源群組。</span><span class="sxs-lookup"><span data-stu-id="c08e3-124">The command uses the *ResourceGroupName* parameter to specify a resource group where the template will be deployed.</span></span>
<span data-ttu-id="c08e3-125">此命令使用 *TemplateFile* 參數來指定範本檔案。</span><span class="sxs-lookup"><span data-stu-id="c08e3-125">The command uses the *TemplateFile* parameter to specify a template file.</span></span>
<span data-ttu-id="c08e3-126">此命令會使用 *TemplateParameterFile* 參數來指定範本參數檔。</span><span class="sxs-lookup"><span data-stu-id="c08e3-126">The command uses the *TemplateParameterFile* parameter to specify a template parameter file.</span></span>
<span data-ttu-id="c08e3-127">此命令會使用 *ResultFormat* 參數來設定 What-If 結果，以包含完整的資源載荷。</span><span class="sxs-lookup"><span data-stu-id="c08e3-127">The command uses the *ResultFormat* parameter to set the What-If result to include full resource payloads.</span></span>

### <span data-ttu-id="c08e3-128">範例2：使用 ResourceIdOnly 在資源群組範圍中取得 What-If 結果</span><span class="sxs-lookup"><span data-stu-id="c08e3-128">Example 2: Get a What-If result at resource group scope with ResourceIdOnly</span></span>
```powershell
PS C:\> Get-AzResourceGroupDeploymentWhatIfResult `
    -DeploymentName "deploy-01" `
    -ResourceGroupName "myRG1" `
    -TemplateFile "D:\Azure\Templates\ServiceTemplate.json" `
    -TemplateParameterFile "D:\Azure\Templates\ServiceParameters.json" `
    -ResultFormat "ResourceIdOnly"
```

<span data-ttu-id="c08e3-129">這個命令會使用自訂範本檔案和磁片上的參數檔案，在指定的資源群組範圍中取得 What-If 結果。</span><span class="sxs-lookup"><span data-stu-id="c08e3-129">This command gets a What-If result at the specified resource group scope by using a custom template file and a parameter file on disk.</span></span>
<span data-ttu-id="c08e3-130">此命令會使用 *ResourceGroupName* 參數來指定要部署範本的資源群組。</span><span class="sxs-lookup"><span data-stu-id="c08e3-130">The command uses the *ResourceGroupName* parameter to specify a resource group where the template will be deployed.</span></span>
<span data-ttu-id="c08e3-131">此命令使用 *TemplateFile* 參數來指定範本檔案。</span><span class="sxs-lookup"><span data-stu-id="c08e3-131">The command uses the *TemplateFile* parameter to specify a template file.</span></span>
<span data-ttu-id="c08e3-132">此命令會使用 *TemplateParameterFile* 參數來指定範本參數檔。</span><span class="sxs-lookup"><span data-stu-id="c08e3-132">The command uses the *TemplateParameterFile* parameter to specify a template parameter file.</span></span>
<span data-ttu-id="c08e3-133">此命令會使用 *ResultFormat* 參數，將 What-If 結果設定為僅包含資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="c08e3-133">The command uses the *ResultFormat* parameter to set the What-If result to only contain resource IDs.</span></span>

## <span data-ttu-id="c08e3-134">參數</span><span class="sxs-lookup"><span data-stu-id="c08e3-134">PARAMETERS</span></span>

### <span data-ttu-id="c08e3-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c08e3-135">-DefaultProfile</span></span>
<span data-ttu-id="c08e3-136">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="c08e3-136">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c08e3-137">-ExcludeChangeType</span><span class="sxs-lookup"><span data-stu-id="c08e3-137">-ExcludeChangeType</span></span>
<span data-ttu-id="c08e3-138">要從 What-If 結果中排除的逗號分隔資源變更類型。</span><span class="sxs-lookup"><span data-stu-id="c08e3-138">Comma-separated resource change types to be excluded from What-If results.</span></span>

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

### <span data-ttu-id="c08e3-139">模式</span><span class="sxs-lookup"><span data-stu-id="c08e3-139">-Mode</span></span>
<span data-ttu-id="c08e3-140">部署模式。</span><span class="sxs-lookup"><span data-stu-id="c08e3-140">The deployment mode.</span></span>

```yaml
Type: Microsoft.Azure.Management.ResourceManager.Models.DeploymentMode
Parameter Sets: (All)
Aliases:
Accepted values: Incremental, Complete

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c08e3-141">-名稱</span><span class="sxs-lookup"><span data-stu-id="c08e3-141">-Name</span></span>
<span data-ttu-id="c08e3-142">將要建立之部署的名稱。</span><span class="sxs-lookup"><span data-stu-id="c08e3-142">The name of the deployment it's going to create.</span></span> <span data-ttu-id="c08e3-143">如果未指定，則預設為提供範本檔時的範本檔案名;預設為提供範本物件的目前時間（例如 "20131223140835"）。</span><span class="sxs-lookup"><span data-stu-id="c08e3-143">If not specified, defaults to the template file name when a template file is provided; defaults to the current time when a template object is provided, e.g. "20131223140835".</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: DeploymentName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c08e3-144">-預先</span><span class="sxs-lookup"><span data-stu-id="c08e3-144">-Pre</span></span>
<span data-ttu-id="c08e3-145">設定時，表示 Cmdlet 應該使用預發行 API 版本，以便自動判斷要使用的版本。</span><span class="sxs-lookup"><span data-stu-id="c08e3-145">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="c08e3-146">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c08e3-146">-ResourceGroupName</span></span>
<span data-ttu-id="c08e3-147">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="c08e3-147">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c08e3-148">-ResultFormat</span><span class="sxs-lookup"><span data-stu-id="c08e3-148">-ResultFormat</span></span>
<span data-ttu-id="c08e3-149">What-If 的結果格式。</span><span class="sxs-lookup"><span data-stu-id="c08e3-149">The What-If result format.</span></span>

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

### <span data-ttu-id="c08e3-150">-SkipTemplateParameterPrompt</span><span class="sxs-lookup"><span data-stu-id="c08e3-150">-SkipTemplateParameterPrompt</span></span>
<span data-ttu-id="c08e3-151">會跳過 PowerShell 動態參數處理，檢查提供的範本參數是否包含範本所使用的所有必要參數。</span><span class="sxs-lookup"><span data-stu-id="c08e3-151">Skips the PowerShell dynamic parameter processing that checks if the provided template parameter contains all necessary parameters used by the template.</span></span>
<span data-ttu-id="c08e3-152">這項檢查會提示使用者提供缺少參數的值，但提供-SkipTemplateParameterPrompt 將會在範本中發現未系結的參數時，立即忽略此提示和錯誤。</span><span class="sxs-lookup"><span data-stu-id="c08e3-152">This check would prompt the user to provide a value for the missing parameters, but providing the -SkipTemplateParameterPrompt will ignore this prompt and error out immediately if a parameter was found not to be bound in the template.</span></span>
<span data-ttu-id="c08e3-153">在非互動式腳本中，您可以提供 SkipTemplateParameterPrompt，以在不符合所有必要參數的情況下，提供較佳的錯誤訊息。</span><span class="sxs-lookup"><span data-stu-id="c08e3-153">For non-interactive scripts, -SkipTemplateParameterPrompt can be provided to provide a better error message in the case where not all required parameters are satisfied.</span></span>

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

### <span data-ttu-id="c08e3-154">-TemplateFile</span><span class="sxs-lookup"><span data-stu-id="c08e3-154">-TemplateFile</span></span>
<span data-ttu-id="c08e3-155">範本檔案的本機路徑。</span><span class="sxs-lookup"><span data-stu-id="c08e3-155">Local path to the template file.</span></span>

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

### <span data-ttu-id="c08e3-156">-TemplateObject</span><span class="sxs-lookup"><span data-stu-id="c08e3-156">-TemplateObject</span></span>
<span data-ttu-id="c08e3-157">代表範本的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="c08e3-157">A hash table which represents the template.</span></span>

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

### <span data-ttu-id="c08e3-158">-TemplateParameterFile</span><span class="sxs-lookup"><span data-stu-id="c08e3-158">-TemplateParameterFile</span></span>
<span data-ttu-id="c08e3-159">具有範本參數的檔案。</span><span class="sxs-lookup"><span data-stu-id="c08e3-159">A file that has the template parameters.</span></span>

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

### <span data-ttu-id="c08e3-160">-TemplateParameterObject</span><span class="sxs-lookup"><span data-stu-id="c08e3-160">-TemplateParameterObject</span></span>
<span data-ttu-id="c08e3-161">代表參數的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="c08e3-161">A hash table which represents the parameters.</span></span>

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

### <span data-ttu-id="c08e3-162">-TemplateParameterUri</span><span class="sxs-lookup"><span data-stu-id="c08e3-162">-TemplateParameterUri</span></span>
<span data-ttu-id="c08e3-163">範本參數檔的 Uri。</span><span class="sxs-lookup"><span data-stu-id="c08e3-163">Uri to the template parameter file.</span></span>

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

### <span data-ttu-id="c08e3-164">-TemplateUri</span><span class="sxs-lookup"><span data-stu-id="c08e3-164">-TemplateUri</span></span>
<span data-ttu-id="c08e3-165">範本檔案的 Uri。</span><span class="sxs-lookup"><span data-stu-id="c08e3-165">Uri to the template file.</span></span>

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

### <span data-ttu-id="c08e3-166">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c08e3-166">CommonParameters</span></span>
<span data-ttu-id="c08e3-167">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="c08e3-167">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c08e3-168">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="c08e3-168">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c08e3-169">輸入</span><span class="sxs-lookup"><span data-stu-id="c08e3-169">INPUTS</span></span>

### <span data-ttu-id="c08e3-170">System.object</span><span class="sxs-lookup"><span data-stu-id="c08e3-170">System.String</span></span>

### <span data-ttu-id="c08e3-171">DeploymentMode 中的 [管理]</span><span class="sxs-lookup"><span data-stu-id="c08e3-171">Microsoft.Azure.Management.ResourceManager.Models.DeploymentMode</span></span>

### <span data-ttu-id="c08e3-172">[System.object] 集合. Hashtable</span><span class="sxs-lookup"><span data-stu-id="c08e3-172">System.Collections.Hashtable</span></span>

## <span data-ttu-id="c08e3-173">輸出</span><span class="sxs-lookup"><span data-stu-id="c08e3-173">OUTPUTS</span></span>

### <span data-ttu-id="c08e3-174">PSWhatIfOperationResult 中的 SdkModels，然後再</span><span class="sxs-lookup"><span data-stu-id="c08e3-174">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.Deployments.PSWhatIfOperationResult</span></span>

## <span data-ttu-id="c08e3-175">筆記</span><span class="sxs-lookup"><span data-stu-id="c08e3-175">NOTES</span></span>

## <span data-ttu-id="c08e3-176">相關連結</span><span class="sxs-lookup"><span data-stu-id="c08e3-176">RELATED LINKS</span></span>
