---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/test-azmanagementgroupdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Test-AzManagementGroupDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Test-AzManagementGroupDeployment.md
ms.openlocfilehash: ad7b595ce7a1247a8ed4bb7dbd121471f7e0d65b
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94127343"
---
# <span data-ttu-id="3ceb5-101">Test-AzManagementGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="3ceb5-101">Test-AzManagementGroupDeployment</span></span>

## <span data-ttu-id="3ceb5-102">摘要</span><span class="sxs-lookup"><span data-stu-id="3ceb5-102">SYNOPSIS</span></span>
<span data-ttu-id="3ceb5-103">驗證管理群組的部署。</span><span class="sxs-lookup"><span data-stu-id="3ceb5-103">Validates a deployment at a management group.</span></span>

## <span data-ttu-id="3ceb5-104">句法</span><span class="sxs-lookup"><span data-stu-id="3ceb5-104">SYNTAX</span></span>

### <span data-ttu-id="3ceb5-105">ByTemplateFileWithNoParameters (預設) </span><span class="sxs-lookup"><span data-stu-id="3ceb5-105">ByTemplateFileWithNoParameters (Default)</span></span>
```
Test-AzManagementGroupDeployment -ManagementGroupId <String> -Location <String> -TemplateFile <String>
 [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="3ceb5-106">ByTemplateObjectAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="3ceb5-106">ByTemplateObjectAndParameterObject</span></span>
```
Test-AzManagementGroupDeployment -ManagementGroupId <String> -Location <String>
 -TemplateParameterObject <Hashtable> -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3ceb5-107">ByTemplateFileAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="3ceb5-107">ByTemplateFileAndParameterObject</span></span>
```
Test-AzManagementGroupDeployment -ManagementGroupId <String> -Location <String>
 -TemplateParameterObject <Hashtable> -TemplateFile <String> [-SkipTemplateParameterPrompt]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3ceb5-108">ByTemplateUriAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="3ceb5-108">ByTemplateUriAndParameterObject</span></span>
```
Test-AzManagementGroupDeployment -ManagementGroupId <String> -Location <String>
 -TemplateParameterObject <Hashtable> -TemplateUri <String> [-SkipTemplateParameterPrompt]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3ceb5-109">ByTemplateObjectAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="3ceb5-109">ByTemplateObjectAndParameterFile</span></span>
```
Test-AzManagementGroupDeployment -ManagementGroupId <String> -Location <String> -TemplateParameterFile <String>
 -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3ceb5-110">ByTemplateFileAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="3ceb5-110">ByTemplateFileAndParameterFile</span></span>
```
Test-AzManagementGroupDeployment -ManagementGroupId <String> -Location <String> -TemplateParameterFile <String>
 -TemplateFile <String> [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3ceb5-111">ByTemplateUriAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="3ceb5-111">ByTemplateUriAndParameterFile</span></span>
```
Test-AzManagementGroupDeployment -ManagementGroupId <String> -Location <String> -TemplateParameterFile <String>
 -TemplateUri <String> [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3ceb5-112">ByTemplateObjectAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="3ceb5-112">ByTemplateObjectAndParameterUri</span></span>
```
Test-AzManagementGroupDeployment -ManagementGroupId <String> -Location <String> -TemplateParameterUri <String>
 -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3ceb5-113">ByTemplateFileAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="3ceb5-113">ByTemplateFileAndParameterUri</span></span>
```
Test-AzManagementGroupDeployment -ManagementGroupId <String> -Location <String> -TemplateParameterUri <String>
 -TemplateFile <String> [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3ceb5-114">ByTemplateUriAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="3ceb5-114">ByTemplateUriAndParameterUri</span></span>
```
Test-AzManagementGroupDeployment -ManagementGroupId <String> -Location <String> -TemplateParameterUri <String>
 -TemplateUri <String> [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3ceb5-115">ByTemplateObjectWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="3ceb5-115">ByTemplateObjectWithNoParameters</span></span>
```
Test-AzManagementGroupDeployment -ManagementGroupId <String> -Location <String> -TemplateObject <Hashtable>
 [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="3ceb5-116">ByTemplateUriWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="3ceb5-116">ByTemplateUriWithNoParameters</span></span>
```
Test-AzManagementGroupDeployment -ManagementGroupId <String> -Location <String> -TemplateUri <String>
 [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="3ceb5-117">說明</span><span class="sxs-lookup"><span data-stu-id="3ceb5-117">DESCRIPTION</span></span>
<span data-ttu-id="3ceb5-118">**Test AzManagementGroupDeployment** Cmdlet 會判斷部署範本及其參數值在管理群組中是否有效。</span><span class="sxs-lookup"><span data-stu-id="3ceb5-118">The **Test-AzManagementGroupDeployment** cmdlet determines whether a deployment template and its parameter values are valid at a management group.</span></span>

## <span data-ttu-id="3ceb5-119">示例</span><span class="sxs-lookup"><span data-stu-id="3ceb5-119">EXAMPLES</span></span>

### <span data-ttu-id="3ceb5-120">範例1：使用自訂範本和參數檔案測試部署</span><span class="sxs-lookup"><span data-stu-id="3ceb5-120">Example 1: Test deployment with a custom template and parameter file</span></span>
```
PS C:\> Test-AzManagementGroupDeployment -ManagementGroupId "myMG" -Location "West US" -TemplateFile "D:\Azure\Templates\OrgSetup.json" -TemplateParameterFile "D:\Azure\Templates\OrgParms.json"
```

<span data-ttu-id="3ceb5-121">這個命令會使用指定的範本檔案和參數檔案，在管理群組「myMG」測試部署。</span><span class="sxs-lookup"><span data-stu-id="3ceb5-121">This command tests a deployment at the management group "myMG" using the given template file and parameters file.</span></span>

### <span data-ttu-id="3ceb5-122">範例2：使用自訂範本物件與參數檔案測試部署</span><span class="sxs-lookup"><span data-stu-id="3ceb5-122">Example 2: Test deployment with a custom template object and parameter file</span></span>
```
PS C:\> $TemplateFileText = [System.IO.File]::ReadAllText("D:\Azure\Templates\OrgSetup.json")
PS C:\> $TemplateObject = ConvertFrom-Json $TemplateFileText -AsHashtable
PS C:\> Test-AzManagementGroupDeployment -ManagementGroupId "myMG" -Location "West US" -TemplateObject $TemplateObject -TemplateParameterFile "D:\Azure\Templates\EngSiteParams.json"
```

<span data-ttu-id="3ceb5-123">這個命令會使用從指定的範本檔案和參數檔案建立的記憶體內部雜湊表，在管理群組「myMG」測試部署。</span><span class="sxs-lookup"><span data-stu-id="3ceb5-123">This command tests a deployment at the management group "myMG" using the an in-memory hashtable created from the given template file and a parameter file.</span></span>

## <span data-ttu-id="3ceb5-124">參數</span><span class="sxs-lookup"><span data-stu-id="3ceb5-124">PARAMETERS</span></span>

### <span data-ttu-id="3ceb5-125">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="3ceb5-125">-ApiVersion</span></span>
<span data-ttu-id="3ceb5-126">設定時，會指出要使用的資源提供者 API 版本。</span><span class="sxs-lookup"><span data-stu-id="3ceb5-126">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="3ceb5-127">如果未指定，API 版本會自動決定為最新的可用。</span><span class="sxs-lookup"><span data-stu-id="3ceb5-127">If not specified, the API version is automatically determined as the latest available.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3ceb5-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3ceb5-128">-DefaultProfile</span></span>
<span data-ttu-id="3ceb5-129">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="3ceb5-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3ceb5-130">-位置</span><span class="sxs-lookup"><span data-stu-id="3ceb5-130">-Location</span></span>
<span data-ttu-id="3ceb5-131">儲存部署資料的位置。</span><span class="sxs-lookup"><span data-stu-id="3ceb5-131">The location to store deployment data.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3ceb5-132">-ManagementGroupId</span><span class="sxs-lookup"><span data-stu-id="3ceb5-132">-ManagementGroupId</span></span>
<span data-ttu-id="3ceb5-133">管理群組識別碼。</span><span class="sxs-lookup"><span data-stu-id="3ceb5-133">The management group id.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3ceb5-134">-預先</span><span class="sxs-lookup"><span data-stu-id="3ceb5-134">-Pre</span></span>
<span data-ttu-id="3ceb5-135">設定時，表示 Cmdlet 應該使用預發行 API 版本，以便自動判斷要使用的版本。</span><span class="sxs-lookup"><span data-stu-id="3ceb5-135">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3ceb5-136">-SkipTemplateParameterPrompt</span><span class="sxs-lookup"><span data-stu-id="3ceb5-136">-SkipTemplateParameterPrompt</span></span>
<span data-ttu-id="3ceb5-137">會跳過 PowerShell 動態參數處理，檢查提供的範本參數是否包含範本所使用的所有必要參數。</span><span class="sxs-lookup"><span data-stu-id="3ceb5-137">Skips the PowerShell dynamic parameter processing that checks if the provided template parameter contains all necessary parameters used by the template.</span></span>
<span data-ttu-id="3ceb5-138">這項檢查會提示使用者提供缺少參數的值，但提供-SkipTemplateParameterPrompt 將會在範本中發現未系結的參數時，立即忽略此提示和錯誤。</span><span class="sxs-lookup"><span data-stu-id="3ceb5-138">This check would prompt the user to provide a value for the missing parameters, but providing the -SkipTemplateParameterPrompt will ignore this prompt and error out immediately if a parameter was found not to be bound in the template.</span></span>
<span data-ttu-id="3ceb5-139">在非互動式腳本中，您可以提供 SkipTemplateParameterPrompt，以在不符合所有必要參數的情況下，提供較佳的錯誤訊息。</span><span class="sxs-lookup"><span data-stu-id="3ceb5-139">For non-interactive scripts, -SkipTemplateParameterPrompt can be provided to provide a better error message in the case where not all required parameters are satisfied.</span></span>

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

### <span data-ttu-id="3ceb5-140">-TemplateFile</span><span class="sxs-lookup"><span data-stu-id="3ceb5-140">-TemplateFile</span></span>
<span data-ttu-id="3ceb5-141">範本檔案的本機路徑。</span><span class="sxs-lookup"><span data-stu-id="3ceb5-141">Local path to the template file.</span></span>

```yaml
Type: String
Parameter Sets: ByTemplateFileWithNoParameters, ByTemplateFileAndParameterObject, ByTemplateFileAndParameterFile, ByTemplateFileAndParameterUri
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3ceb5-142">-TemplateObject</span><span class="sxs-lookup"><span data-stu-id="3ceb5-142">-TemplateObject</span></span>
<span data-ttu-id="3ceb5-143">代表範本的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="3ceb5-143">A hash table which represents the template.</span></span>

```yaml
Type: Hashtable
Parameter Sets: ByTemplateObjectAndParameterObject, ByTemplateObjectAndParameterFile, ByTemplateObjectAndParameterUri, ByTemplateObjectWithNoParameters
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3ceb5-144">-TemplateParameterFile</span><span class="sxs-lookup"><span data-stu-id="3ceb5-144">-TemplateParameterFile</span></span>
<span data-ttu-id="3ceb5-145">具有範本參數的檔案。</span><span class="sxs-lookup"><span data-stu-id="3ceb5-145">A file that has the template parameters.</span></span>

```yaml
Type: String
Parameter Sets: ByTemplateObjectAndParameterFile, ByTemplateFileAndParameterFile, ByTemplateUriAndParameterFile
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3ceb5-146">-TemplateParameterObject</span><span class="sxs-lookup"><span data-stu-id="3ceb5-146">-TemplateParameterObject</span></span>
<span data-ttu-id="3ceb5-147">代表參數的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="3ceb5-147">A hash table which represents the parameters.</span></span>

```yaml
Type: Hashtable
Parameter Sets: ByTemplateObjectAndParameterObject, ByTemplateFileAndParameterObject, ByTemplateUriAndParameterObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3ceb5-148">-TemplateParameterUri</span><span class="sxs-lookup"><span data-stu-id="3ceb5-148">-TemplateParameterUri</span></span>
<span data-ttu-id="3ceb5-149">範本參數檔的 Uri。</span><span class="sxs-lookup"><span data-stu-id="3ceb5-149">Uri to the template parameter file.</span></span>

```yaml
Type: String
Parameter Sets: ByTemplateObjectAndParameterUri, ByTemplateFileAndParameterUri, ByTemplateUriAndParameterUri
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3ceb5-150">-TemplateUri</span><span class="sxs-lookup"><span data-stu-id="3ceb5-150">-TemplateUri</span></span>
<span data-ttu-id="3ceb5-151">範本檔案的 Uri。</span><span class="sxs-lookup"><span data-stu-id="3ceb5-151">Uri to the template file.</span></span>

```yaml
Type: String
Parameter Sets: ByTemplateUriAndParameterObject, ByTemplateUriAndParameterFile, ByTemplateUriAndParameterUri, ByTemplateUriWithNoParameters
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3ceb5-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3ceb5-152">CommonParameters</span></span>
<span data-ttu-id="3ceb5-153">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="3ceb5-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3ceb5-154">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="3ceb5-154">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3ceb5-155">輸入</span><span class="sxs-lookup"><span data-stu-id="3ceb5-155">INPUTS</span></span>

### <span data-ttu-id="3ceb5-156">[System.object] 集合. Hashtable</span><span class="sxs-lookup"><span data-stu-id="3ceb5-156">System.Collections.Hashtable</span></span>

### <span data-ttu-id="3ceb5-157">System.object</span><span class="sxs-lookup"><span data-stu-id="3ceb5-157">System.String</span></span>

## <span data-ttu-id="3ceb5-158">輸出</span><span class="sxs-lookup"><span data-stu-id="3ceb5-158">OUTPUTS</span></span>

### <span data-ttu-id="3ceb5-159">PSResourceManagerError 中的 SdkModels （）</span><span class="sxs-lookup"><span data-stu-id="3ceb5-159">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceManagerError</span></span>

## <span data-ttu-id="3ceb5-160">筆記</span><span class="sxs-lookup"><span data-stu-id="3ceb5-160">NOTES</span></span>

## <span data-ttu-id="3ceb5-161">相關連結</span><span class="sxs-lookup"><span data-stu-id="3ceb5-161">RELATED LINKS</span></span>
