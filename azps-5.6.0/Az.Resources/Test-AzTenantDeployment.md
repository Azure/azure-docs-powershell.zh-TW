---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/powershell/module/az.resources/test-aztenantdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Test-AzTenantDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Test-AzTenantDeployment.md
ms.openlocfilehash: 5c440c6f150993b947a0db2162ef0fd664e73220
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101903949"
---
# <span data-ttu-id="da7cd-101">Test-AzTenantDeployment</span><span class="sxs-lookup"><span data-stu-id="da7cd-101">Test-AzTenantDeployment</span></span>

## <span data-ttu-id="da7cd-102">簡介</span><span class="sxs-lookup"><span data-stu-id="da7cd-102">SYNOPSIS</span></span>
<span data-ttu-id="da7cd-103">在租使用者範圍驗證部署。</span><span class="sxs-lookup"><span data-stu-id="da7cd-103">Validates a deployment at tenant scope.</span></span>

## <span data-ttu-id="da7cd-104">語法</span><span class="sxs-lookup"><span data-stu-id="da7cd-104">SYNTAX</span></span>

### <span data-ttu-id="da7cd-105">ByTemplateFileWithNoParameters (預設) </span><span class="sxs-lookup"><span data-stu-id="da7cd-105">ByTemplateFileWithNoParameters (Default)</span></span>
```
Test-AzTenantDeployment -Location <String> [-QueryString <String>] -TemplateFile <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="da7cd-106">ByTemplateObjectAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="da7cd-106">ByTemplateObjectAndParameterObject</span></span>
```
Test-AzTenantDeployment -Location <String> [-QueryString <String>] -TemplateParameterObject <Hashtable>
 -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="da7cd-107">ByTemplateFileAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="da7cd-107">ByTemplateFileAndParameterObject</span></span>
```
Test-AzTenantDeployment -Location <String> [-QueryString <String>] -TemplateParameterObject <Hashtable>
 -TemplateFile <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="da7cd-108">ByTemplateUriAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="da7cd-108">ByTemplateUriAndParameterObject</span></span>
```
Test-AzTenantDeployment -Location <String> [-QueryString <String>] -TemplateParameterObject <Hashtable>
 -TemplateUri <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="da7cd-109">ByTemplateObjectAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="da7cd-109">ByTemplateObjectAndParameterFile</span></span>
```
Test-AzTenantDeployment -Location <String> [-QueryString <String>] -TemplateParameterFile <String>
 -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="da7cd-110">ByTemplateFileAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="da7cd-110">ByTemplateFileAndParameterFile</span></span>
```
Test-AzTenantDeployment -Location <String> [-QueryString <String>] -TemplateParameterFile <String>
 -TemplateFile <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="da7cd-111">ByTemplateUriAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="da7cd-111">ByTemplateUriAndParameterFile</span></span>
```
Test-AzTenantDeployment -Location <String> [-QueryString <String>] -TemplateParameterFile <String>
 -TemplateUri <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="da7cd-112">ByTemplateSpecResourceIdAndParams</span><span class="sxs-lookup"><span data-stu-id="da7cd-112">ByTemplateSpecResourceIdAndParams</span></span>
```
Test-AzTenantDeployment -Location <String> [-QueryString <String>] -TemplateParameterFile <String>
 -TemplateSpecId <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="da7cd-113">ByTemplateObjectAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="da7cd-113">ByTemplateObjectAndParameterUri</span></span>
```
Test-AzTenantDeployment -Location <String> [-QueryString <String>] -TemplateParameterUri <String>
 -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="da7cd-114">ByTemplateFileAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="da7cd-114">ByTemplateFileAndParameterUri</span></span>
```
Test-AzTenantDeployment -Location <String> [-QueryString <String>] -TemplateParameterUri <String>
 -TemplateFile <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="da7cd-115">ByTemplateUriAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="da7cd-115">ByTemplateUriAndParameterUri</span></span>
```
Test-AzTenantDeployment -Location <String> [-QueryString <String>] -TemplateParameterUri <String>
 -TemplateUri <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="da7cd-116">ByTemplateSpecResourceIdAndParamsUri</span><span class="sxs-lookup"><span data-stu-id="da7cd-116">ByTemplateSpecResourceIdAndParamsUri</span></span>
```
Test-AzTenantDeployment -Location <String> [-QueryString <String>] -TemplateParameterUri <String>
 -TemplateSpecId <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="da7cd-117">ByTemplateObjectWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="da7cd-117">ByTemplateObjectWithNoParameters</span></span>
```
Test-AzTenantDeployment -Location <String> [-QueryString <String>] -TemplateObject <Hashtable>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="da7cd-118">ByTemplateUriWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="da7cd-118">ByTemplateUriWithNoParameters</span></span>
```
Test-AzTenantDeployment -Location <String> [-QueryString <String>] -TemplateUri <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="da7cd-119">ByTemplateSpecResourceId</span><span class="sxs-lookup"><span data-stu-id="da7cd-119">ByTemplateSpecResourceId</span></span>
```
Test-AzTenantDeployment -Location <String> [-QueryString <String>] -TemplateSpecId <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="da7cd-120">描述</span><span class="sxs-lookup"><span data-stu-id="da7cd-120">DESCRIPTION</span></span>
<span data-ttu-id="da7cd-121">**Test-AzTenantDeployment** Cmdlet 會決定部署範本及其參數值在目前的租使用者範圍中是否有效。</span><span class="sxs-lookup"><span data-stu-id="da7cd-121">The **Test-AzTenantDeployment** cmdlet determines whether a deployment template and its parameter values are valid at the current tenant scope.</span></span>

## <span data-ttu-id="da7cd-122">例子</span><span class="sxs-lookup"><span data-stu-id="da7cd-122">EXAMPLES</span></span>

### <span data-ttu-id="da7cd-123">範例 1：使用自訂範本和參數檔案測試部署</span><span class="sxs-lookup"><span data-stu-id="da7cd-123">Example 1: Test deployment with a custom template and parameter file</span></span>
```
PS C:\> Test-AzTenantDeployment -Location "West US" -TemplateFile "D:\Azure\Templates\OrgSetup.json" -TemplateParameterFile "D:\Azure\Templates\OrgParms.json"
```

<span data-ttu-id="da7cd-124">此命令會使用指定範本檔案和參數檔案，測試目前租使用者範圍中的部署。</span><span class="sxs-lookup"><span data-stu-id="da7cd-124">This command tests a deployment at the current tenant scope using the given template file and parameters file.</span></span>

### <span data-ttu-id="da7cd-125">範例 2：使用自訂範本物件和參數檔案測試部署</span><span class="sxs-lookup"><span data-stu-id="da7cd-125">Example 2: Test deployment with a custom template object and parameter file</span></span>
```
PS C:\> $TemplateFileText = [System.IO.File]::ReadAllText("D:\Azure\Templates\OrgSetup.json")
PS C:\> $TemplateObject = ConvertFrom-Json $TemplateFileText -AsHashtable
PS C:\> Test-AzTenantDeployment -Location "West US" -TemplateObject $TemplateObject -TemplateParameterFile "D:\Azure\Templates\EngSiteParams.json"
```

<span data-ttu-id="da7cd-126">此命令會使用從指定範本檔案和參數檔案建立的記憶體內雜湊表，測試目前租使用者範圍中的部署。</span><span class="sxs-lookup"><span data-stu-id="da7cd-126">This command tests a deployment at the current tenant scope using the an in-memory hashtable created from the given template file and a parameter file.</span></span>

## <span data-ttu-id="da7cd-127">參數</span><span class="sxs-lookup"><span data-stu-id="da7cd-127">PARAMETERS</span></span>

### <span data-ttu-id="da7cd-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="da7cd-128">-DefaultProfile</span></span>
<span data-ttu-id="da7cd-129">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="da7cd-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="da7cd-130">-位置</span><span class="sxs-lookup"><span data-stu-id="da7cd-130">-Location</span></span>
<span data-ttu-id="da7cd-131">儲存部署資料的位置。</span><span class="sxs-lookup"><span data-stu-id="da7cd-131">The location to store deployment data.</span></span>

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

### <span data-ttu-id="da7cd-132">-Pre</span><span class="sxs-lookup"><span data-stu-id="da7cd-132">-Pre</span></span>
<span data-ttu-id="da7cd-133">設定之後，表示當系統自動決定要使用哪個版本時，Cmdlet 應該使用測試版 API 版本。</span><span class="sxs-lookup"><span data-stu-id="da7cd-133">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="da7cd-134">-QueryString</span><span class="sxs-lookup"><span data-stu-id="da7cd-134">-QueryString</span></span>
<span data-ttu-id="da7cd-135">查詢字串 (例如，一個 SAS 權杖) TemplateUri 參數一起使用。</span><span class="sxs-lookup"><span data-stu-id="da7cd-135">The query string (for example, a SAS token) to be used with the TemplateUri parameter.</span></span> <span data-ttu-id="da7cd-136">會用於連結範本的情況</span><span class="sxs-lookup"><span data-stu-id="da7cd-136">Would be used in case of linked templates</span></span>

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

### <span data-ttu-id="da7cd-137">-SkipTemplateParameterPrompt</span><span class="sxs-lookup"><span data-stu-id="da7cd-137">-SkipTemplateParameterPrompt</span></span>
<span data-ttu-id="da7cd-138">跳過 PowerShell 動態參數處理，檢查所提供的範本參數是否包含範本使用的所有必要參數。</span><span class="sxs-lookup"><span data-stu-id="da7cd-138">Skips the PowerShell dynamic parameter processing that checks if the provided template parameter contains all necessary parameters used by the template.</span></span>
<span data-ttu-id="da7cd-139">這項檢查會提示使用者提供遺失參數的值，但若發現參數未系在範本中，則提供 -SkipTemplateParameterPrompt 會忽略此提示並立即錯誤。</span><span class="sxs-lookup"><span data-stu-id="da7cd-139">This check would prompt the user to provide a value for the missing parameters, but providing the -SkipTemplateParameterPrompt will ignore this prompt and error out immediately if a parameter was found not to be bound in the template.</span></span>
<span data-ttu-id="da7cd-140">針對非互動式腳本，您可以提供 -SkipTemplateParameterPrompt，以在未滿足所有所需參數的情況下提供更佳的錯誤訊息。</span><span class="sxs-lookup"><span data-stu-id="da7cd-140">For non-interactive scripts, -SkipTemplateParameterPrompt can be provided to provide a better error message in the case where not all required parameters are satisfied.</span></span>

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

### <span data-ttu-id="da7cd-141">-TemplateFile</span><span class="sxs-lookup"><span data-stu-id="da7cd-141">-TemplateFile</span></span>
<span data-ttu-id="da7cd-142">範本檔案的當地路徑。</span><span class="sxs-lookup"><span data-stu-id="da7cd-142">Local path to the template file.</span></span> <span data-ttu-id="da7cd-143">支援的範本檔案類型：json 和 bicep。</span><span class="sxs-lookup"><span data-stu-id="da7cd-143">Supported template file type: json and bicep.</span></span>

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

### <span data-ttu-id="da7cd-144">-TemplateObject</span><span class="sxs-lookup"><span data-stu-id="da7cd-144">-TemplateObject</span></span>
<span data-ttu-id="da7cd-145">代表範本的雜湊表格。</span><span class="sxs-lookup"><span data-stu-id="da7cd-145">A hash table which represents the template.</span></span>

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

### <span data-ttu-id="da7cd-146">-TemplateParameterFile</span><span class="sxs-lookup"><span data-stu-id="da7cd-146">-TemplateParameterFile</span></span>
<span data-ttu-id="da7cd-147">具有範本參數的檔案。</span><span class="sxs-lookup"><span data-stu-id="da7cd-147">A file that has the template parameters.</span></span>

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

### <span data-ttu-id="da7cd-148">-TemplateParameterObject</span><span class="sxs-lookup"><span data-stu-id="da7cd-148">-TemplateParameterObject</span></span>
<span data-ttu-id="da7cd-149">代表參數的雜湊表格。</span><span class="sxs-lookup"><span data-stu-id="da7cd-149">A hash table which represents the parameters.</span></span>

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

### <span data-ttu-id="da7cd-150">-TemplateParameterUri</span><span class="sxs-lookup"><span data-stu-id="da7cd-150">-TemplateParameterUri</span></span>
<span data-ttu-id="da7cd-151">Uri 到範本參數檔案。</span><span class="sxs-lookup"><span data-stu-id="da7cd-151">Uri to the template parameter file.</span></span>

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

### <span data-ttu-id="da7cd-152">-TemplateSpecId</span><span class="sxs-lookup"><span data-stu-id="da7cd-152">-TemplateSpecId</span></span>
<span data-ttu-id="da7cd-153">要部署的 templateSpec 資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="da7cd-153">Resource ID of the templateSpec to be deployed.</span></span>

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

### <span data-ttu-id="da7cd-154">-TemplateUri</span><span class="sxs-lookup"><span data-stu-id="da7cd-154">-TemplateUri</span></span>
<span data-ttu-id="da7cd-155">Uri 到範本檔案。</span><span class="sxs-lookup"><span data-stu-id="da7cd-155">Uri to the template file.</span></span>

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

### <span data-ttu-id="da7cd-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="da7cd-156">CommonParameters</span></span>
<span data-ttu-id="da7cd-157">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="da7cd-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="da7cd-158">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="da7cd-158">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="da7cd-159">輸入</span><span class="sxs-lookup"><span data-stu-id="da7cd-159">INPUTS</span></span>

### <span data-ttu-id="da7cd-160">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="da7cd-160">System.Collections.Hashtable</span></span>

### <span data-ttu-id="da7cd-161">System.String</span><span class="sxs-lookup"><span data-stu-id="da7cd-161">System.String</span></span>

## <span data-ttu-id="da7cd-162">輸出</span><span class="sxs-lookup"><span data-stu-id="da7cd-162">OUTPUTS</span></span>

### <span data-ttu-id="da7cd-163">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceManagerError</span><span class="sxs-lookup"><span data-stu-id="da7cd-163">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceManagerError</span></span>

## <span data-ttu-id="da7cd-164">筆記</span><span class="sxs-lookup"><span data-stu-id="da7cd-164">NOTES</span></span>

## <span data-ttu-id="da7cd-165">相關連結</span><span class="sxs-lookup"><span data-stu-id="da7cd-165">RELATED LINKS</span></span>
