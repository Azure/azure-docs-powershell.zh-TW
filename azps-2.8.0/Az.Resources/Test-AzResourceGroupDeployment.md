---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 0143CE35-3B1D-4829-B880-A5CA25B83883
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/test-azresourcegroupdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Test-AzResourceGroupDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Test-AzResourceGroupDeployment.md
ms.openlocfilehash: 01d7aa0cb0b363dac8e19e5b38796c43523d6296
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93792168"
---
# <span data-ttu-id="6b449-101">Test-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="6b449-101">Test-AzResourceGroupDeployment</span></span>

## <span data-ttu-id="6b449-102">摘要</span><span class="sxs-lookup"><span data-stu-id="6b449-102">SYNOPSIS</span></span>
<span data-ttu-id="6b449-103">驗證資源群組部署。</span><span class="sxs-lookup"><span data-stu-id="6b449-103">Validates a resource group deployment.</span></span>

## <span data-ttu-id="6b449-104">句法</span><span class="sxs-lookup"><span data-stu-id="6b449-104">SYNTAX</span></span>

### <span data-ttu-id="6b449-105">ByTemplateFileWithNoParameters (預設) </span><span class="sxs-lookup"><span data-stu-id="6b449-105">ByTemplateFileWithNoParameters (Default)</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] -TemplateFile <String> [-SkipTemplateParameterPrompt]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6b449-106">ByTemplateObjectAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="6b449-106">ByTemplateObjectAndParameterObject</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] -TemplateParameterObject <Hashtable> -TemplateObject <Hashtable>
 [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="6b449-107">ByTemplateFileAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="6b449-107">ByTemplateFileAndParameterObject</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] -TemplateParameterObject <Hashtable> -TemplateFile <String>
 [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="6b449-108">ByTemplateUriAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="6b449-108">ByTemplateUriAndParameterObject</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] -TemplateParameterObject <Hashtable> -TemplateUri <String>
 [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="6b449-109">ByTemplateObjectAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="6b449-109">ByTemplateObjectAndParameterFile</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] -TemplateParameterFile <String> -TemplateObject <Hashtable>
 [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="6b449-110">ByTemplateFileAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="6b449-110">ByTemplateFileAndParameterFile</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] -TemplateParameterFile <String> -TemplateFile <String>
 [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="6b449-111">ByTemplateUriAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="6b449-111">ByTemplateUriAndParameterFile</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] -TemplateParameterFile <String> -TemplateUri <String>
 [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="6b449-112">ByTemplateObjectAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="6b449-112">ByTemplateObjectAndParameterUri</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] -TemplateParameterUri <String> -TemplateObject <Hashtable>
 [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="6b449-113">ByTemplateFileAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="6b449-113">ByTemplateFileAndParameterUri</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] -TemplateParameterUri <String> -TemplateFile <String>
 [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="6b449-114">ByTemplateUriAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="6b449-114">ByTemplateUriAndParameterUri</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] -TemplateParameterUri <String> -TemplateUri <String>
 [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="6b449-115">ByTemplateObjectWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="6b449-115">ByTemplateObjectWithNoParameters</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6b449-116">ByTemplateUriWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="6b449-116">ByTemplateUriWithNoParameters</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] -TemplateUri <String> [-SkipTemplateParameterPrompt] [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6b449-117">說明</span><span class="sxs-lookup"><span data-stu-id="6b449-117">DESCRIPTION</span></span>
<span data-ttu-id="6b449-118">**Test AzResourceGroupDeployment** Cmdlet 會判斷 Azure 資源群組部署範本及其參數值是否有效。</span><span class="sxs-lookup"><span data-stu-id="6b449-118">The **Test-AzResourceGroupDeployment** cmdlet determines whether an Azure resource group deployment template and its parameter values are valid.</span></span>

## <span data-ttu-id="6b449-119">示例</span><span class="sxs-lookup"><span data-stu-id="6b449-119">EXAMPLES</span></span>

### <span data-ttu-id="6b449-120">範例1：使用自訂範本物件與參數檔案測試部署</span><span class="sxs-lookup"><span data-stu-id="6b449-120">Example 1: Test deployment with a custom template object and parameter file</span></span>
```
PS C:\> $TemplateFileText = [System.IO.File]::ReadAllText("D:\Azure\Templates\EngineeringSite.json")
PS C:\> $TemplateObject = ConvertFrom-Json $TemplateFileText -AsHashtable
PS C:\> Test-AzResourceGroupDeployment -ResourceGroupName "ContosoEngineering" -TemplateObject $TemplateObject -TemplateParameterFile "D:\Azure\Templates\EngSiteParams.json"
```

<span data-ttu-id="6b449-121">這個命令會使用從指定的範本檔案和參數檔案建立的記憶體中 hashtable，在指定的資源群組中測試部署。</span><span class="sxs-lookup"><span data-stu-id="6b449-121">This command tests a deployment in the given resource group using the an in-memory hashtable created from the given template file and a parameter file.</span></span>

## <span data-ttu-id="6b449-122">參數</span><span class="sxs-lookup"><span data-stu-id="6b449-122">PARAMETERS</span></span>

### <span data-ttu-id="6b449-123">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="6b449-123">-ApiVersion</span></span>
<span data-ttu-id="6b449-124">指定資源提供者支援的 API 版本。</span><span class="sxs-lookup"><span data-stu-id="6b449-124">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="6b449-125">您可以指定不同于預設版本的版本。</span><span class="sxs-lookup"><span data-stu-id="6b449-125">You can specify a different version than the default version.</span></span>

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

### <span data-ttu-id="6b449-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6b449-126">-DefaultProfile</span></span>
<span data-ttu-id="6b449-127">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="6b449-127">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6b449-128">模式</span><span class="sxs-lookup"><span data-stu-id="6b449-128">-Mode</span></span>
<span data-ttu-id="6b449-129">指定部署模式。</span><span class="sxs-lookup"><span data-stu-id="6b449-129">Specifies the deployment mode.</span></span>
<span data-ttu-id="6b449-130">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="6b449-130">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="6b449-131">少量</span><span class="sxs-lookup"><span data-stu-id="6b449-131">Incremental</span></span>
- <span data-ttu-id="6b449-132">完備</span><span class="sxs-lookup"><span data-stu-id="6b449-132">Complete</span></span>

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

### <span data-ttu-id="6b449-133">-預先</span><span class="sxs-lookup"><span data-stu-id="6b449-133">-Pre</span></span>
<span data-ttu-id="6b449-134">表示此 Cmdlet 會在自動決定要使用哪個版本時，考慮預發行 API 版本。</span><span class="sxs-lookup"><span data-stu-id="6b449-134">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="6b449-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6b449-135">-ResourceGroupName</span></span>
<span data-ttu-id="6b449-136">指定要測試之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="6b449-136">Specifies the name of the resource group to test.</span></span>

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

### <span data-ttu-id="6b449-137">-RollBackDeploymentName</span><span class="sxs-lookup"><span data-stu-id="6b449-137">-RollBackDeploymentName</span></span>
<span data-ttu-id="6b449-138">如果使用了-RollbackToLastDeployment，則會使用資源群組中的指定名稱回滾到成功的部署。</span><span class="sxs-lookup"><span data-stu-id="6b449-138">Rollback to the successful deployment with the given name in the resource group, should not be used if -RollbackToLastDeployment is used.</span></span>

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

### <span data-ttu-id="6b449-139">-RollbackToLastDeployment</span><span class="sxs-lookup"><span data-stu-id="6b449-139">-RollbackToLastDeployment</span></span>
<span data-ttu-id="6b449-140">如果使用-RollBackDeploymentName，則回退至 [資源] 群組中的最後一個成功部署。</span><span class="sxs-lookup"><span data-stu-id="6b449-140">Rollback to the last successful deployment in the resource group, should not be present if -RollBackDeploymentName is used.</span></span>

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

### <span data-ttu-id="6b449-141">-SkipTemplateParameterPrompt</span><span class="sxs-lookup"><span data-stu-id="6b449-141">-SkipTemplateParameterPrompt</span></span>
<span data-ttu-id="6b449-142">會跳過 PowerShell 動態參數處理，檢查提供的範本參數是否包含範本所使用的所有必要參數。</span><span class="sxs-lookup"><span data-stu-id="6b449-142">Skips the PowerShell dynamic parameter processing that checks if the provided template parameter contains all necessary parameters used by the template.</span></span> <span data-ttu-id="6b449-143">這項檢查會提示使用者提供缺少參數的值，但提供-SkipTemplateParameterPrompt 將會在範本中發現未系結的參數時，立即忽略此提示和錯誤。</span><span class="sxs-lookup"><span data-stu-id="6b449-143">This check would prompt the user to provide a value for the missing parameters, but providing the -SkipTemplateParameterPrompt will ignore this prompt and error out immediately if a parameter was found not to be bound in the template.</span></span> <span data-ttu-id="6b449-144">在非互動式腳本中，您可以提供 SkipTemplateParameterPrompt，以在不符合所有必要參數的情況下，提供較佳的錯誤訊息。</span><span class="sxs-lookup"><span data-stu-id="6b449-144">For non-interactive scripts, -SkipTemplateParameterPrompt can be provided to provide a better error message in the case where not all required parameters are satisfied.</span></span>

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

### <span data-ttu-id="6b449-145">-TemplateFile</span><span class="sxs-lookup"><span data-stu-id="6b449-145">-TemplateFile</span></span>
<span data-ttu-id="6b449-146">指定 JSON 範本檔的完整路徑。</span><span class="sxs-lookup"><span data-stu-id="6b449-146">Specifies the full path of a JSON template file.</span></span>

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

### <span data-ttu-id="6b449-147">-TemplateObject</span><span class="sxs-lookup"><span data-stu-id="6b449-147">-TemplateObject</span></span>
<span data-ttu-id="6b449-148">代表範本的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="6b449-148">A hash table which represents the template.</span></span>

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

### <span data-ttu-id="6b449-149">-TemplateParameterFile</span><span class="sxs-lookup"><span data-stu-id="6b449-149">-TemplateParameterFile</span></span>
<span data-ttu-id="6b449-150">指定包含範本參數之名稱和值的 JSON 檔案的完整路徑。</span><span class="sxs-lookup"><span data-stu-id="6b449-150">Specifies the full path of a JSON file that contains the names and values of the template parameters.</span></span>

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

### <span data-ttu-id="6b449-151">-TemplateParameterObject</span><span class="sxs-lookup"><span data-stu-id="6b449-151">-TemplateParameterObject</span></span>
<span data-ttu-id="6b449-152">指定範本參數名稱和值的雜湊表。</span><span class="sxs-lookup"><span data-stu-id="6b449-152">Specifies a hash table of template parameter names and values.</span></span>

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

### <span data-ttu-id="6b449-153">-TemplateParameterUri</span><span class="sxs-lookup"><span data-stu-id="6b449-153">-TemplateParameterUri</span></span>
<span data-ttu-id="6b449-154">指定範本參數檔的 URI。</span><span class="sxs-lookup"><span data-stu-id="6b449-154">Specifies the URI of a template parameters file.</span></span>

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

### <span data-ttu-id="6b449-155">-TemplateUri</span><span class="sxs-lookup"><span data-stu-id="6b449-155">-TemplateUri</span></span>
<span data-ttu-id="6b449-156">指定 JSON 範本檔案的 URI。</span><span class="sxs-lookup"><span data-stu-id="6b449-156">Specifies the URI of a JSON template file.</span></span>

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

### <span data-ttu-id="6b449-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6b449-157">CommonParameters</span></span>
<span data-ttu-id="6b449-158">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="6b449-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6b449-159">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="6b449-159">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6b449-160">輸入</span><span class="sxs-lookup"><span data-stu-id="6b449-160">INPUTS</span></span>

### <span data-ttu-id="6b449-161">System.object</span><span class="sxs-lookup"><span data-stu-id="6b449-161">System.String</span></span>

### <span data-ttu-id="6b449-162">DeploymentMode 中的 [管理]</span><span class="sxs-lookup"><span data-stu-id="6b449-162">Microsoft.Azure.Management.ResourceManager.Models.DeploymentMode</span></span>

### <span data-ttu-id="6b449-163">[System.object] 集合. Hashtable</span><span class="sxs-lookup"><span data-stu-id="6b449-163">System.Collections.Hashtable</span></span>

## <span data-ttu-id="6b449-164">輸出</span><span class="sxs-lookup"><span data-stu-id="6b449-164">OUTPUTS</span></span>

### <span data-ttu-id="6b449-165">PSResourceManagerError 中的 SdkModels （）</span><span class="sxs-lookup"><span data-stu-id="6b449-165">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceManagerError</span></span>

## <span data-ttu-id="6b449-166">筆記</span><span class="sxs-lookup"><span data-stu-id="6b449-166">NOTES</span></span>

## <span data-ttu-id="6b449-167">相關連結</span><span class="sxs-lookup"><span data-stu-id="6b449-167">RELATED LINKS</span></span>

[<span data-ttu-id="6b449-168">AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="6b449-168">Get-AzResourceGroupDeployment</span></span>](./Get-AzResourceGroupDeployment.md)

[<span data-ttu-id="6b449-169">新-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="6b449-169">New-AzResourceGroupDeployment</span></span>](./New-AzResourceGroupDeployment.md)

[<span data-ttu-id="6b449-170">移除-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="6b449-170">Remove-AzResourceGroupDeployment</span></span>](./Remove-AzResourceGroupDeployment.md)

[<span data-ttu-id="6b449-171">停止 AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="6b449-171">Stop-AzResourceGroupDeployment</span></span>](./Stop-AzResourceGroupDeployment.md)


