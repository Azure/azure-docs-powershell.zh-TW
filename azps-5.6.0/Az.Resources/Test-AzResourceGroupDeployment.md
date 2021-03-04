---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 0143CE35-3B1D-4829-B880-A5CA25B83883
online version: https://docs.microsoft.com/powershell/module/az.resources/test-azresourcegroupdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Test-AzResourceGroupDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Test-AzResourceGroupDeployment.md
ms.openlocfilehash: 0e0d4645901f60f9e290d197a47b133d6bf3db8c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101908037"
---
# <span data-ttu-id="82058-101">Test-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="82058-101">Test-AzResourceGroupDeployment</span></span>

## <span data-ttu-id="82058-102">簡介</span><span class="sxs-lookup"><span data-stu-id="82058-102">SYNOPSIS</span></span>
<span data-ttu-id="82058-103">驗證資源群組部署。</span><span class="sxs-lookup"><span data-stu-id="82058-103">Validates a resource group deployment.</span></span>

## <span data-ttu-id="82058-104">語法</span><span class="sxs-lookup"><span data-stu-id="82058-104">SYNTAX</span></span>

### <span data-ttu-id="82058-105">ByTemplateFileWithNoParameters (預設) </span><span class="sxs-lookup"><span data-stu-id="82058-105">ByTemplateFileWithNoParameters (Default)</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] [-QueryString <String>] -TemplateFile <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="82058-106">ByTemplateObjectAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="82058-106">ByTemplateObjectAndParameterObject</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] [-QueryString <String>] -TemplateParameterObject <Hashtable>
 -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="82058-107">ByTemplateFileAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="82058-107">ByTemplateFileAndParameterObject</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] [-QueryString <String>] -TemplateParameterObject <Hashtable>
 -TemplateFile <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="82058-108">ByTemplateUriAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="82058-108">ByTemplateUriAndParameterObject</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] [-QueryString <String>] -TemplateParameterObject <Hashtable>
 -TemplateUri <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="82058-109">ByTemplateObjectAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="82058-109">ByTemplateObjectAndParameterFile</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] [-QueryString <String>] -TemplateParameterFile <String>
 -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="82058-110">ByTemplateFileAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="82058-110">ByTemplateFileAndParameterFile</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] [-QueryString <String>] -TemplateParameterFile <String>
 -TemplateFile <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="82058-111">ByTemplateUriAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="82058-111">ByTemplateUriAndParameterFile</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] [-QueryString <String>] -TemplateParameterFile <String>
 -TemplateUri <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="82058-112">ByTemplateSpecResourceIdAndParams</span><span class="sxs-lookup"><span data-stu-id="82058-112">ByTemplateSpecResourceIdAndParams</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] [-QueryString <String>] -TemplateParameterFile <String>
 -TemplateSpecId <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="82058-113">ByTemplateObjectAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="82058-113">ByTemplateObjectAndParameterUri</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] [-QueryString <String>] -TemplateParameterUri <String>
 -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="82058-114">ByTemplateFileAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="82058-114">ByTemplateFileAndParameterUri</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] [-QueryString <String>] -TemplateParameterUri <String>
 -TemplateFile <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="82058-115">ByTemplateUriAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="82058-115">ByTemplateUriAndParameterUri</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] [-QueryString <String>] -TemplateParameterUri <String>
 -TemplateUri <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="82058-116">ByTemplateSpecResourceIdAndParamsUri</span><span class="sxs-lookup"><span data-stu-id="82058-116">ByTemplateSpecResourceIdAndParamsUri</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] [-QueryString <String>] -TemplateParameterUri <String>
 -TemplateSpecId <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="82058-117">ByTemplateObjectWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="82058-117">ByTemplateObjectWithNoParameters</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] [-QueryString <String>] -TemplateObject <Hashtable>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="82058-118">ByTemplateUriWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="82058-118">ByTemplateUriWithNoParameters</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] [-QueryString <String>] -TemplateUri <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="82058-119">ByTemplateSpecResourceId</span><span class="sxs-lookup"><span data-stu-id="82058-119">ByTemplateSpecResourceId</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] [-QueryString <String>] -TemplateSpecId <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="82058-120">描述</span><span class="sxs-lookup"><span data-stu-id="82058-120">DESCRIPTION</span></span>
<span data-ttu-id="82058-121">**Test-AzResourceGroupDeployment** Cmdlet 會判斷 Azure 資源群組部署範本及其參數值是否有效。</span><span class="sxs-lookup"><span data-stu-id="82058-121">The **Test-AzResourceGroupDeployment** cmdlet determines whether an Azure resource group deployment template and its parameter values are valid.</span></span>

## <span data-ttu-id="82058-122">例子</span><span class="sxs-lookup"><span data-stu-id="82058-122">EXAMPLES</span></span>

### <span data-ttu-id="82058-123">範例 1：使用自訂範本物件和參數檔案測試部署</span><span class="sxs-lookup"><span data-stu-id="82058-123">Example 1: Test deployment with a custom template object and parameter file</span></span>

```powershell
PS C:\> $TemplateFileText = [System.IO.File]::ReadAllText("D:\Azure\Templates\EngineeringSite.json")
PS C:\> $TemplateObject = ConvertFrom-Json $TemplateFileText -AsHashtable
PS C:\> Test-AzResourceGroupDeployment -ResourceGroupName "ContosoEngineering" -TemplateObject $TemplateObject -TemplateParameterFile "D:\Azure\Templates\EngSiteParams.json"
```

<span data-ttu-id="82058-124">此命令會使用從指定範本檔案和參數檔案建立的記憶體內雜湊表，測試指定資源群組中的部署。</span><span class="sxs-lookup"><span data-stu-id="82058-124">This command tests a deployment in the given resource group using the an in-memory hashtable created from the given template file and a parameter file.</span></span>

### <span data-ttu-id="82058-125">範例 2：透過範本檔案和參數檔案測試部署</span><span class="sxs-lookup"><span data-stu-id="82058-125">Example 2: Test deployment via template file and parameter file</span></span>

```powershell
PS C:\> Test-AzResourceGroupDeployment -ResourceGroupName testRG01 -TemplateFile "D:\Azure\Templates\sampleDeploymentTemplate.json" -TemplateParameterFile "D:\Azure\Templates\sampleDeploymentTemplateParams.json"
```

<span data-ttu-id="82058-126">此命令會使用提供的範本檔案和參數檔案測試指定資源群組和資源中的部署。</span><span class="sxs-lookup"><span data-stu-id="82058-126">This command tests a deployment in the given resource group and resource using the provided template file and a parameter file.</span></span>

## <span data-ttu-id="82058-127">參數</span><span class="sxs-lookup"><span data-stu-id="82058-127">PARAMETERS</span></span>

### <span data-ttu-id="82058-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="82058-128">-DefaultProfile</span></span>
<span data-ttu-id="82058-129">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="82058-129">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="82058-130">-模式</span><span class="sxs-lookup"><span data-stu-id="82058-130">-Mode</span></span>
<span data-ttu-id="82058-131">指定部署模式。</span><span class="sxs-lookup"><span data-stu-id="82058-131">Specifies the deployment mode.</span></span>
<span data-ttu-id="82058-132">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="82058-132">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="82058-133">增量</span><span class="sxs-lookup"><span data-stu-id="82058-133">Incremental</span></span>
- <span data-ttu-id="82058-134">完成</span><span class="sxs-lookup"><span data-stu-id="82058-134">Complete</span></span>

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

### <span data-ttu-id="82058-135">-Pre</span><span class="sxs-lookup"><span data-stu-id="82058-135">-Pre</span></span>
<span data-ttu-id="82058-136">表示此 Cmdlet 會在自動決定要使用哪個版本時，考慮測試版 API 版本。</span><span class="sxs-lookup"><span data-stu-id="82058-136">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="82058-137">-QueryString</span><span class="sxs-lookup"><span data-stu-id="82058-137">-QueryString</span></span>
<span data-ttu-id="82058-138">查詢字串 (例如，一個 SAS 權杖) TemplateUri 參數一起使用。</span><span class="sxs-lookup"><span data-stu-id="82058-138">The query string (for example, a SAS token) to be used with the TemplateUri parameter.</span></span> <span data-ttu-id="82058-139">會用於連結範本的情況</span><span class="sxs-lookup"><span data-stu-id="82058-139">Would be used in case of linked templates</span></span>

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

### <span data-ttu-id="82058-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="82058-140">-ResourceGroupName</span></span>
<span data-ttu-id="82058-141">指定要測試的資源組名。</span><span class="sxs-lookup"><span data-stu-id="82058-141">Specifies the name of the resource group to test.</span></span>

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

### <span data-ttu-id="82058-142">-RollBackDeploymentName</span><span class="sxs-lookup"><span data-stu-id="82058-142">-RollBackDeploymentName</span></span>
<span data-ttu-id="82058-143">如果使用 -RollbackToLastDeployment，則不應該使用資源群組中具有指定名稱的成功部署。</span><span class="sxs-lookup"><span data-stu-id="82058-143">Rollback to the successful deployment with the given name in the resource group, should not be used if -RollbackToLastDeployment is used.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="82058-144">-RollbackToLastDeployment</span><span class="sxs-lookup"><span data-stu-id="82058-144">-RollbackToLastDeployment</span></span>
<span data-ttu-id="82058-145">如果使用 -RollBackDeploymentName，則不應該出現資源群組中最後一個成功部署的卷回。</span><span class="sxs-lookup"><span data-stu-id="82058-145">Rollback to the last successful deployment in the resource group, should not be present if -RollBackDeploymentName is used.</span></span>

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

### <span data-ttu-id="82058-146">-SkipTemplateParameterPrompt</span><span class="sxs-lookup"><span data-stu-id="82058-146">-SkipTemplateParameterPrompt</span></span>
<span data-ttu-id="82058-147">跳過 PowerShell 動態參數處理，檢查所提供的範本參數是否包含範本使用的所有必要參數。</span><span class="sxs-lookup"><span data-stu-id="82058-147">Skips the PowerShell dynamic parameter processing that checks if the provided template parameter contains all necessary parameters used by the template.</span></span> <span data-ttu-id="82058-148">這項檢查會提示使用者提供遺失參數的值，但若發現參數未系在範本中，則提供 -SkipTemplateParameterPrompt 會忽略此提示並立即錯誤。</span><span class="sxs-lookup"><span data-stu-id="82058-148">This check would prompt the user to provide a value for the missing parameters, but providing the -SkipTemplateParameterPrompt will ignore this prompt and error out immediately if a parameter was found not to be bound in the template.</span></span> <span data-ttu-id="82058-149">針對非互動式腳本，您可以提供 -SkipTemplateParameterPrompt，以在未滿足所有所需參數的情況下提供更佳的錯誤訊息。</span><span class="sxs-lookup"><span data-stu-id="82058-149">For non-interactive scripts, -SkipTemplateParameterPrompt can be provided to provide a better error message in the case where not all required parameters are satisfied.</span></span>

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

### <span data-ttu-id="82058-150">-TemplateFile</span><span class="sxs-lookup"><span data-stu-id="82058-150">-TemplateFile</span></span>
<span data-ttu-id="82058-151">指定範本檔案的完整路徑。</span><span class="sxs-lookup"><span data-stu-id="82058-151">Specifies the full path of a template file.</span></span> <span data-ttu-id="82058-152">支援的範本檔案類型：json 和 bicep。</span><span class="sxs-lookup"><span data-stu-id="82058-152">Supported template file type: json and bicep.</span></span>

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

### <span data-ttu-id="82058-153">-TemplateObject</span><span class="sxs-lookup"><span data-stu-id="82058-153">-TemplateObject</span></span>
<span data-ttu-id="82058-154">代表範本的雜湊表格。</span><span class="sxs-lookup"><span data-stu-id="82058-154">A hash table which represents the template.</span></span>

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

### <span data-ttu-id="82058-155">-TemplateParameterFile</span><span class="sxs-lookup"><span data-stu-id="82058-155">-TemplateParameterFile</span></span>
<span data-ttu-id="82058-156">指定包含範本參數名稱和值的 JSON 檔案完整路徑。</span><span class="sxs-lookup"><span data-stu-id="82058-156">Specifies the full path of a JSON file that contains the names and values of the template parameters.</span></span>

```yaml
Type: System.String
Parameter Sets: ByTemplateObjectAndParameterFile, ByTemplateFileAndParameterFile, ByTemplateUriAndParameterFile, ByTemplateSpecResourceIdAndParams
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="82058-157">-TemplateParameterObject</span><span class="sxs-lookup"><span data-stu-id="82058-157">-TemplateParameterObject</span></span>
<span data-ttu-id="82058-158">指定範本參數名稱和值的雜湊表格。</span><span class="sxs-lookup"><span data-stu-id="82058-158">Specifies a hash table of template parameter names and values.</span></span>

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

### <span data-ttu-id="82058-159">-TemplateParameterUri</span><span class="sxs-lookup"><span data-stu-id="82058-159">-TemplateParameterUri</span></span>
<span data-ttu-id="82058-160">指定範本參數檔案的 URI。</span><span class="sxs-lookup"><span data-stu-id="82058-160">Specifies the URI of a template parameters file.</span></span>

```yaml
Type: System.String
Parameter Sets: ByTemplateObjectAndParameterUri, ByTemplateFileAndParameterUri, ByTemplateUriAndParameterUri, ByTemplateSpecResourceIdAndParamsUri
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="82058-161">-TemplateSpecId</span><span class="sxs-lookup"><span data-stu-id="82058-161">-TemplateSpecId</span></span>
<span data-ttu-id="82058-162">要部署的 templateSpec 資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="82058-162">Resource ID of the templateSpec to be deployed.</span></span>

```yaml
Type: System.String
Parameter Sets: ByTemplateSpecResourceIdAndParams, ByTemplateSpecResourceIdAndParamsUri, ByTemplateSpecResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="82058-163">-TemplateUri</span><span class="sxs-lookup"><span data-stu-id="82058-163">-TemplateUri</span></span>
<span data-ttu-id="82058-164">指定範本檔案的 URI。</span><span class="sxs-lookup"><span data-stu-id="82058-164">Specifies the URI of a template file.</span></span>

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

### <span data-ttu-id="82058-165">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="82058-165">CommonParameters</span></span>
<span data-ttu-id="82058-166">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="82058-166">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="82058-167">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="82058-167">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="82058-168">輸入</span><span class="sxs-lookup"><span data-stu-id="82058-168">INPUTS</span></span>

### <span data-ttu-id="82058-169">System.String</span><span class="sxs-lookup"><span data-stu-id="82058-169">System.String</span></span>

### <span data-ttu-id="82058-170">Microsoft.Azure.management.ResourceManager.models.DeploymentMode</span><span class="sxs-lookup"><span data-stu-id="82058-170">Microsoft.Azure.Management.ResourceManager.Models.DeploymentMode</span></span>

### <span data-ttu-id="82058-171">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="82058-171">System.Collections.Hashtable</span></span>

## <span data-ttu-id="82058-172">輸出</span><span class="sxs-lookup"><span data-stu-id="82058-172">OUTPUTS</span></span>

### <span data-ttu-id="82058-173">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceManagerError</span><span class="sxs-lookup"><span data-stu-id="82058-173">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceManagerError</span></span>

## <span data-ttu-id="82058-174">筆記</span><span class="sxs-lookup"><span data-stu-id="82058-174">NOTES</span></span>

## <span data-ttu-id="82058-175">相關連結</span><span class="sxs-lookup"><span data-stu-id="82058-175">RELATED LINKS</span></span>

[<span data-ttu-id="82058-176">Get-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="82058-176">Get-AzResourceGroupDeployment</span></span>](./Get-AzResourceGroupDeployment.md)

[<span data-ttu-id="82058-177">New-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="82058-177">New-AzResourceGroupDeployment</span></span>](./New-AzResourceGroupDeployment.md)

[<span data-ttu-id="82058-178">Remove-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="82058-178">Remove-AzResourceGroupDeployment</span></span>](./Remove-AzResourceGroupDeployment.md)

[<span data-ttu-id="82058-179">Stop-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="82058-179">Stop-AzResourceGroupDeployment</span></span>](./Stop-AzResourceGroupDeployment.md)


