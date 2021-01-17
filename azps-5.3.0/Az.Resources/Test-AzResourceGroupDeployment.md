---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 0143CE35-3B1D-4829-B880-A5CA25B83883
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/test-azresourcegroupdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Test-AzResourceGroupDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Test-AzResourceGroupDeployment.md
ms.openlocfilehash: 5ee86c91b1dc1354b078b727e3bc9ebfe5a43bfe
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98435381"
---
# <span data-ttu-id="4a476-101">Test-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="4a476-101">Test-AzResourceGroupDeployment</span></span>

## <span data-ttu-id="4a476-102">摘要</span><span class="sxs-lookup"><span data-stu-id="4a476-102">SYNOPSIS</span></span>
<span data-ttu-id="4a476-103">驗證資源群組部署。</span><span class="sxs-lookup"><span data-stu-id="4a476-103">Validates a resource group deployment.</span></span>

## <span data-ttu-id="4a476-104">句法</span><span class="sxs-lookup"><span data-stu-id="4a476-104">SYNTAX</span></span>

### <span data-ttu-id="4a476-105">ByTemplateFileWithNoParameters (預設) </span><span class="sxs-lookup"><span data-stu-id="4a476-105">ByTemplateFileWithNoParameters (Default)</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] -TemplateFile <String> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4a476-106">ByTemplateObjectAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="4a476-106">ByTemplateObjectAndParameterObject</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] -TemplateParameterObject <Hashtable> -TemplateObject <Hashtable>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4a476-107">ByTemplateFileAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="4a476-107">ByTemplateFileAndParameterObject</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] -TemplateParameterObject <Hashtable> -TemplateFile <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4a476-108">ByTemplateUriAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="4a476-108">ByTemplateUriAndParameterObject</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] -TemplateParameterObject <Hashtable> -TemplateUri <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4a476-109">ByTemplateObjectAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="4a476-109">ByTemplateObjectAndParameterFile</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] -TemplateParameterFile <String> -TemplateObject <Hashtable>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4a476-110">ByTemplateFileAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="4a476-110">ByTemplateFileAndParameterFile</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] -TemplateParameterFile <String> -TemplateFile <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4a476-111">ByTemplateUriAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="4a476-111">ByTemplateUriAndParameterFile</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] -TemplateParameterFile <String> -TemplateUri <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4a476-112">ByTemplateObjectAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="4a476-112">ByTemplateObjectAndParameterUri</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] -TemplateParameterUri <String> -TemplateObject <Hashtable>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4a476-113">ByTemplateFileAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="4a476-113">ByTemplateFileAndParameterUri</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] -TemplateParameterUri <String> -TemplateFile <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4a476-114">ByTemplateUriAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="4a476-114">ByTemplateUriAndParameterUri</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] -TemplateParameterUri <String> -TemplateUri <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4a476-115">ByTemplateObjectWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="4a476-115">ByTemplateObjectWithNoParameters</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4a476-116">ByTemplateUriWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="4a476-116">ByTemplateUriWithNoParameters</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] -TemplateUri <String> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4a476-117">說明</span><span class="sxs-lookup"><span data-stu-id="4a476-117">DESCRIPTION</span></span>
<span data-ttu-id="4a476-118">**Test AzResourceGroupDeployment** Cmdlet 會判斷 Azure 資源群組部署範本及其參數值是否有效。</span><span class="sxs-lookup"><span data-stu-id="4a476-118">The **Test-AzResourceGroupDeployment** cmdlet determines whether an Azure resource group deployment template and its parameter values are valid.</span></span>

## <span data-ttu-id="4a476-119">示例</span><span class="sxs-lookup"><span data-stu-id="4a476-119">EXAMPLES</span></span>

### <span data-ttu-id="4a476-120">範例1：使用自訂範本物件與參數檔案測試部署</span><span class="sxs-lookup"><span data-stu-id="4a476-120">Example 1: Test deployment with a custom template object and parameter file</span></span>

```powershell
PS C:\> $TemplateFileText = [System.IO.File]::ReadAllText("D:\Azure\Templates\EngineeringSite.json")
PS C:\> $TemplateObject = ConvertFrom-Json $TemplateFileText -AsHashtable
PS C:\> Test-AzResourceGroupDeployment -ResourceGroupName "ContosoEngineering" -TemplateObject $TemplateObject -TemplateParameterFile "D:\Azure\Templates\EngSiteParams.json"
```

<span data-ttu-id="4a476-121">這個命令會使用從指定的範本檔案和參數檔案建立的記憶體中 hashtable，在指定的資源群組中測試部署。</span><span class="sxs-lookup"><span data-stu-id="4a476-121">This command tests a deployment in the given resource group using the an in-memory hashtable created from the given template file and a parameter file.</span></span>

### <span data-ttu-id="4a476-122">範例2：透過範本檔案和參數檔案測試部署</span><span class="sxs-lookup"><span data-stu-id="4a476-122">Example 2: Test deployment via template file and parameter file</span></span>

```powershell
PS C:\> Test-AzResourceGroupDeployment -ResourceGroupName testRG01 -TemplateFile "D:\Azure\Templates\sampleDeploymentTemplate.json" -TemplateParameterFile "D:\Azure\Templates\sampleDeploymentTemplateParams.json"
```

<span data-ttu-id="4a476-123">這個命令會使用所提供的範本檔案和參數檔案，在指定的資源群組和資源中測試部署。</span><span class="sxs-lookup"><span data-stu-id="4a476-123">This command tests a deployment in the given resource group and resource using the provided template file and a parameter file.</span></span>

## <span data-ttu-id="4a476-124">參數</span><span class="sxs-lookup"><span data-stu-id="4a476-124">PARAMETERS</span></span>

### <span data-ttu-id="4a476-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4a476-125">-DefaultProfile</span></span>
<span data-ttu-id="4a476-126">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="4a476-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4a476-127">模式</span><span class="sxs-lookup"><span data-stu-id="4a476-127">-Mode</span></span>
<span data-ttu-id="4a476-128">指定部署模式。</span><span class="sxs-lookup"><span data-stu-id="4a476-128">Specifies the deployment mode.</span></span>
<span data-ttu-id="4a476-129">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="4a476-129">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="4a476-130">少量</span><span class="sxs-lookup"><span data-stu-id="4a476-130">Incremental</span></span>
- <span data-ttu-id="4a476-131">完備</span><span class="sxs-lookup"><span data-stu-id="4a476-131">Complete</span></span>

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

### <span data-ttu-id="4a476-132">-預先</span><span class="sxs-lookup"><span data-stu-id="4a476-132">-Pre</span></span>
<span data-ttu-id="4a476-133">表示此 Cmdlet 會在自動決定要使用哪個版本時，考慮預發行 API 版本。</span><span class="sxs-lookup"><span data-stu-id="4a476-133">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="4a476-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4a476-134">-ResourceGroupName</span></span>
<span data-ttu-id="4a476-135">指定要測試之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="4a476-135">Specifies the name of the resource group to test.</span></span>

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

### <span data-ttu-id="4a476-136">-RollBackDeploymentName</span><span class="sxs-lookup"><span data-stu-id="4a476-136">-RollBackDeploymentName</span></span>
<span data-ttu-id="4a476-137">如果使用了-RollbackToLastDeployment，則會使用資源群組中的指定名稱回滾到成功的部署。</span><span class="sxs-lookup"><span data-stu-id="4a476-137">Rollback to the successful deployment with the given name in the resource group, should not be used if -RollbackToLastDeployment is used.</span></span>

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

### <span data-ttu-id="4a476-138">-RollbackToLastDeployment</span><span class="sxs-lookup"><span data-stu-id="4a476-138">-RollbackToLastDeployment</span></span>
<span data-ttu-id="4a476-139">如果使用-RollBackDeploymentName，則回退至 [資源] 群組中的最後一個成功部署。</span><span class="sxs-lookup"><span data-stu-id="4a476-139">Rollback to the last successful deployment in the resource group, should not be present if -RollBackDeploymentName is used.</span></span>

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

### <span data-ttu-id="4a476-140">-SkipTemplateParameterPrompt</span><span class="sxs-lookup"><span data-stu-id="4a476-140">-SkipTemplateParameterPrompt</span></span>
<span data-ttu-id="4a476-141">會跳過 PowerShell 動態參數處理，檢查提供的範本參數是否包含範本所使用的所有必要參數。</span><span class="sxs-lookup"><span data-stu-id="4a476-141">Skips the PowerShell dynamic parameter processing that checks if the provided template parameter contains all necessary parameters used by the template.</span></span> <span data-ttu-id="4a476-142">這項檢查會提示使用者提供缺少參數的值，但提供-SkipTemplateParameterPrompt 將會在範本中發現未系結的參數時，立即忽略此提示和錯誤。</span><span class="sxs-lookup"><span data-stu-id="4a476-142">This check would prompt the user to provide a value for the missing parameters, but providing the -SkipTemplateParameterPrompt will ignore this prompt and error out immediately if a parameter was found not to be bound in the template.</span></span> <span data-ttu-id="4a476-143">在非互動式腳本中，您可以提供 SkipTemplateParameterPrompt，以在不符合所有必要參數的情況下，提供較佳的錯誤訊息。</span><span class="sxs-lookup"><span data-stu-id="4a476-143">For non-interactive scripts, -SkipTemplateParameterPrompt can be provided to provide a better error message in the case where not all required parameters are satisfied.</span></span>

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

### <span data-ttu-id="4a476-144">-TemplateFile</span><span class="sxs-lookup"><span data-stu-id="4a476-144">-TemplateFile</span></span>
<span data-ttu-id="4a476-145">指定 JSON 範本檔的完整路徑。</span><span class="sxs-lookup"><span data-stu-id="4a476-145">Specifies the full path of a JSON template file.</span></span>

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

### <span data-ttu-id="4a476-146">-TemplateObject</span><span class="sxs-lookup"><span data-stu-id="4a476-146">-TemplateObject</span></span>
<span data-ttu-id="4a476-147">代表範本的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="4a476-147">A hash table which represents the template.</span></span>

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

### <span data-ttu-id="4a476-148">-TemplateParameterFile</span><span class="sxs-lookup"><span data-stu-id="4a476-148">-TemplateParameterFile</span></span>
<span data-ttu-id="4a476-149">指定包含範本參數之名稱和值的 JSON 檔案的完整路徑。</span><span class="sxs-lookup"><span data-stu-id="4a476-149">Specifies the full path of a JSON file that contains the names and values of the template parameters.</span></span>

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

### <span data-ttu-id="4a476-150">-TemplateParameterObject</span><span class="sxs-lookup"><span data-stu-id="4a476-150">-TemplateParameterObject</span></span>
<span data-ttu-id="4a476-151">指定範本參數名稱和值的雜湊表。</span><span class="sxs-lookup"><span data-stu-id="4a476-151">Specifies a hash table of template parameter names and values.</span></span>

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

### <span data-ttu-id="4a476-152">-TemplateParameterUri</span><span class="sxs-lookup"><span data-stu-id="4a476-152">-TemplateParameterUri</span></span>
<span data-ttu-id="4a476-153">指定範本參數檔的 URI。</span><span class="sxs-lookup"><span data-stu-id="4a476-153">Specifies the URI of a template parameters file.</span></span>

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

### <span data-ttu-id="4a476-154">-TemplateUri</span><span class="sxs-lookup"><span data-stu-id="4a476-154">-TemplateUri</span></span>
<span data-ttu-id="4a476-155">指定 JSON 範本檔案的 URI。</span><span class="sxs-lookup"><span data-stu-id="4a476-155">Specifies the URI of a JSON template file.</span></span>

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

### <span data-ttu-id="4a476-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4a476-156">CommonParameters</span></span>
<span data-ttu-id="4a476-157">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="4a476-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4a476-158">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="4a476-158">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4a476-159">輸入</span><span class="sxs-lookup"><span data-stu-id="4a476-159">INPUTS</span></span>

### <span data-ttu-id="4a476-160">System.object</span><span class="sxs-lookup"><span data-stu-id="4a476-160">System.String</span></span>

### <span data-ttu-id="4a476-161">DeploymentMode 中的 [管理]</span><span class="sxs-lookup"><span data-stu-id="4a476-161">Microsoft.Azure.Management.ResourceManager.Models.DeploymentMode</span></span>

### <span data-ttu-id="4a476-162">[System.object] 集合. Hashtable</span><span class="sxs-lookup"><span data-stu-id="4a476-162">System.Collections.Hashtable</span></span>

## <span data-ttu-id="4a476-163">輸出</span><span class="sxs-lookup"><span data-stu-id="4a476-163">OUTPUTS</span></span>

### <span data-ttu-id="4a476-164">PSResourceManagerError 中的 SdkModels （）</span><span class="sxs-lookup"><span data-stu-id="4a476-164">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceManagerError</span></span>

## <span data-ttu-id="4a476-165">筆記</span><span class="sxs-lookup"><span data-stu-id="4a476-165">NOTES</span></span>

## <span data-ttu-id="4a476-166">相關連結</span><span class="sxs-lookup"><span data-stu-id="4a476-166">RELATED LINKS</span></span>

[<span data-ttu-id="4a476-167">AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="4a476-167">Get-AzResourceGroupDeployment</span></span>](./Get-AzResourceGroupDeployment.md)

[<span data-ttu-id="4a476-168">新-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="4a476-168">New-AzResourceGroupDeployment</span></span>](./New-AzResourceGroupDeployment.md)

[<span data-ttu-id="4a476-169">移除-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="4a476-169">Remove-AzResourceGroupDeployment</span></span>](./Remove-AzResourceGroupDeployment.md)

[<span data-ttu-id="4a476-170">停止 AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="4a476-170">Stop-AzResourceGroupDeployment</span></span>](./Stop-AzResourceGroupDeployment.md)


