---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/test-azdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Test-AzDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Test-AzDeployment.md
ms.openlocfilehash: 182cf4d60cf2b81f5a465f9ffad5d862b09e3787
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93792169"
---
# <span data-ttu-id="3d20d-101">Test-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="3d20d-101">Test-AzDeployment</span></span>

## <span data-ttu-id="3d20d-102">摘要</span><span class="sxs-lookup"><span data-stu-id="3d20d-102">SYNOPSIS</span></span>
<span data-ttu-id="3d20d-103">驗證部署。</span><span class="sxs-lookup"><span data-stu-id="3d20d-103">Validates a deployment.</span></span>

## <span data-ttu-id="3d20d-104">句法</span><span class="sxs-lookup"><span data-stu-id="3d20d-104">SYNTAX</span></span>

### <span data-ttu-id="3d20d-105">ByTemplateFileWithNoParameters (預設) </span><span class="sxs-lookup"><span data-stu-id="3d20d-105">ByTemplateFileWithNoParameters (Default)</span></span>
```
Test-AzDeployment -Location <String> -TemplateFile <String> [-SkipTemplateParameterPrompt]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3d20d-106">ByTemplateObjectAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="3d20d-106">ByTemplateObjectAndParameterObject</span></span>
```
Test-AzDeployment -Location <String> -TemplateParameterObject <Hashtable> -TemplateObject <Hashtable>
 [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="3d20d-107">ByTemplateFileAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="3d20d-107">ByTemplateFileAndParameterObject</span></span>
```
Test-AzDeployment -Location <String> -TemplateParameterObject <Hashtable> -TemplateFile <String>
 [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="3d20d-108">ByTemplateUriAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="3d20d-108">ByTemplateUriAndParameterObject</span></span>
```
Test-AzDeployment -Location <String> -TemplateParameterObject <Hashtable> -TemplateUri <String>
 [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="3d20d-109">ByTemplateObjectAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="3d20d-109">ByTemplateObjectAndParameterFile</span></span>
```
Test-AzDeployment -Location <String> -TemplateParameterFile <String> -TemplateObject <Hashtable>
 [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="3d20d-110">ByTemplateFileAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="3d20d-110">ByTemplateFileAndParameterFile</span></span>
```
Test-AzDeployment -Location <String> -TemplateParameterFile <String> -TemplateFile <String>
 [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="3d20d-111">ByTemplateUriAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="3d20d-111">ByTemplateUriAndParameterFile</span></span>
```
Test-AzDeployment -Location <String> -TemplateParameterFile <String> -TemplateUri <String>
 [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="3d20d-112">ByTemplateObjectAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="3d20d-112">ByTemplateObjectAndParameterUri</span></span>
```
Test-AzDeployment -Location <String> -TemplateParameterUri <String> -TemplateObject <Hashtable>
 [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="3d20d-113">ByTemplateFileAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="3d20d-113">ByTemplateFileAndParameterUri</span></span>
```
Test-AzDeployment -Location <String> -TemplateParameterUri <String> -TemplateFile <String>
 [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="3d20d-114">ByTemplateUriAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="3d20d-114">ByTemplateUriAndParameterUri</span></span>
```
Test-AzDeployment -Location <String> -TemplateParameterUri <String> -TemplateUri <String>
 [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="3d20d-115">ByTemplateObjectWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="3d20d-115">ByTemplateObjectWithNoParameters</span></span>
```
Test-AzDeployment -Location <String> -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3d20d-116">ByTemplateUriWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="3d20d-116">ByTemplateUriWithNoParameters</span></span>
```
Test-AzDeployment -Location <String> -TemplateUri <String> [-SkipTemplateParameterPrompt]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3d20d-117">說明</span><span class="sxs-lookup"><span data-stu-id="3d20d-117">DESCRIPTION</span></span>
<span data-ttu-id="3d20d-118">**Test AzDeployment** Cmdlet 會判斷部署範本及其參數值是否有效。</span><span class="sxs-lookup"><span data-stu-id="3d20d-118">The **Test-AzDeployment** cmdlet determines whether a deployment template and its parameter values are valid.</span></span>

## <span data-ttu-id="3d20d-119">示例</span><span class="sxs-lookup"><span data-stu-id="3d20d-119">EXAMPLES</span></span>

### <span data-ttu-id="3d20d-120">範例1：使用自訂範本和參數檔案測試部署</span><span class="sxs-lookup"><span data-stu-id="3d20d-120">Example 1: Test deployment with a custom template and parameter file</span></span>
```
PS C:\> Test-AzDeployment -Location "West US" -TemplateFile "D:\Azure\Templates\EngineeringSite.json" -TemplateParameterFile "D:\Azure\Templates\EngSiteParms.json"
```

<span data-ttu-id="3d20d-121">這個命令會使用指定的範本檔案和參數檔案，在目前的訂閱範圍內測試部署。</span><span class="sxs-lookup"><span data-stu-id="3d20d-121">This command tests a deployment at the current subscription scope using the given template file and parameters file.</span></span>

### <span data-ttu-id="3d20d-122">範例2：使用自訂範本物件與參數檔案測試部署</span><span class="sxs-lookup"><span data-stu-id="3d20d-122">Example 2: Test deployment with a custom template object and parameter file</span></span>
```
PS C:\> $TemplateFileText = [System.IO.File]::ReadAllText("D:\Azure\Templates\EngineeringSite.json")
PS C:\> $TemplateObject = ConvertFrom-Json $TemplateFileText -AsHashtable
PS C:\> Test-AzDeployment -Location "West US" -TemplateObject $TemplateObject -TemplateParameterFile "D:\Azure\Templates\EngSiteParams.json"
```

<span data-ttu-id="3d20d-123">這個命令會使用從指定的範本檔案和參數檔案建立的記憶體中 hashtable，在目前的訂閱範圍測試部署。</span><span class="sxs-lookup"><span data-stu-id="3d20d-123">This command tests a deployment at the current subscription scope using the an in-memory hashtable created from the given template file and a parameter file.</span></span>

## <span data-ttu-id="3d20d-124">參數</span><span class="sxs-lookup"><span data-stu-id="3d20d-124">PARAMETERS</span></span>

### <span data-ttu-id="3d20d-125">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="3d20d-125">-ApiVersion</span></span>
<span data-ttu-id="3d20d-126">設定時，會指出要使用的資源提供者 API 版本。</span><span class="sxs-lookup"><span data-stu-id="3d20d-126">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="3d20d-127">如果未指定，API 版本會自動決定為最新的可用。</span><span class="sxs-lookup"><span data-stu-id="3d20d-127">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="3d20d-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3d20d-128">-DefaultProfile</span></span>
<span data-ttu-id="3d20d-129">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="3d20d-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3d20d-130">-位置</span><span class="sxs-lookup"><span data-stu-id="3d20d-130">-Location</span></span>
<span data-ttu-id="3d20d-131">儲存部署資料的位置。</span><span class="sxs-lookup"><span data-stu-id="3d20d-131">The location to store deployment data.</span></span>

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

### <span data-ttu-id="3d20d-132">-預先</span><span class="sxs-lookup"><span data-stu-id="3d20d-132">-Pre</span></span>
<span data-ttu-id="3d20d-133">設定時，表示 Cmdlet 應該使用預發行 API 版本，以便自動判斷要使用的版本。</span><span class="sxs-lookup"><span data-stu-id="3d20d-133">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="3d20d-134">-SkipTemplateParameterPrompt</span><span class="sxs-lookup"><span data-stu-id="3d20d-134">-SkipTemplateParameterPrompt</span></span>
<span data-ttu-id="3d20d-135">會跳過 PowerShell 動態參數處理，檢查提供的範本參數是否包含範本所使用的所有必要參數。</span><span class="sxs-lookup"><span data-stu-id="3d20d-135">Skips the PowerShell dynamic parameter processing that checks if the provided template parameter contains all necessary parameters used by the template.</span></span> <span data-ttu-id="3d20d-136">這項檢查會提示使用者提供缺少參數的值，但提供-SkipTemplateParameterPrompt 將會在範本中發現未系結的參數時，立即忽略此提示和錯誤。</span><span class="sxs-lookup"><span data-stu-id="3d20d-136">This check would prompt the user to provide a value for the missing parameters, but providing the -SkipTemplateParameterPrompt will ignore this prompt and error out immediately if a parameter was found not to be bound in the template.</span></span> <span data-ttu-id="3d20d-137">在非互動式腳本中，您可以提供 SkipTemplateParameterPrompt，以在不符合所有必要參數的情況下，提供較佳的錯誤訊息。</span><span class="sxs-lookup"><span data-stu-id="3d20d-137">For non-interactive scripts, -SkipTemplateParameterPrompt can be provided to provide a better error message in the case where not all required parameters are satisfied.</span></span>

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

### <span data-ttu-id="3d20d-138">-TemplateFile</span><span class="sxs-lookup"><span data-stu-id="3d20d-138">-TemplateFile</span></span>
<span data-ttu-id="3d20d-139">範本檔案的本機路徑。</span><span class="sxs-lookup"><span data-stu-id="3d20d-139">Local path to the template file.</span></span>

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

### <span data-ttu-id="3d20d-140">-TemplateObject</span><span class="sxs-lookup"><span data-stu-id="3d20d-140">-TemplateObject</span></span>
<span data-ttu-id="3d20d-141">代表範本的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="3d20d-141">A hash table which represents the template.</span></span>

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

### <span data-ttu-id="3d20d-142">-TemplateParameterFile</span><span class="sxs-lookup"><span data-stu-id="3d20d-142">-TemplateParameterFile</span></span>
<span data-ttu-id="3d20d-143">具有範本參數的檔案。</span><span class="sxs-lookup"><span data-stu-id="3d20d-143">A file that has the template parameters.</span></span>

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

### <span data-ttu-id="3d20d-144">-TemplateParameterObject</span><span class="sxs-lookup"><span data-stu-id="3d20d-144">-TemplateParameterObject</span></span>
<span data-ttu-id="3d20d-145">代表參數的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="3d20d-145">A hash table which represents the parameters.</span></span>

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

### <span data-ttu-id="3d20d-146">-TemplateParameterUri</span><span class="sxs-lookup"><span data-stu-id="3d20d-146">-TemplateParameterUri</span></span>
<span data-ttu-id="3d20d-147">範本參數檔的 Uri。</span><span class="sxs-lookup"><span data-stu-id="3d20d-147">Uri to the template parameter file.</span></span>

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

### <span data-ttu-id="3d20d-148">-TemplateUri</span><span class="sxs-lookup"><span data-stu-id="3d20d-148">-TemplateUri</span></span>
<span data-ttu-id="3d20d-149">範本檔案的 Uri。</span><span class="sxs-lookup"><span data-stu-id="3d20d-149">Uri to the template file.</span></span>

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

### <span data-ttu-id="3d20d-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3d20d-150">CommonParameters</span></span>
<span data-ttu-id="3d20d-151">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="3d20d-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3d20d-152">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="3d20d-152">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3d20d-153">輸入</span><span class="sxs-lookup"><span data-stu-id="3d20d-153">INPUTS</span></span>

### <span data-ttu-id="3d20d-154">[System.object] 集合. Hashtable</span><span class="sxs-lookup"><span data-stu-id="3d20d-154">System.Collections.Hashtable</span></span>

### <span data-ttu-id="3d20d-155">System.object</span><span class="sxs-lookup"><span data-stu-id="3d20d-155">System.String</span></span>

## <span data-ttu-id="3d20d-156">輸出</span><span class="sxs-lookup"><span data-stu-id="3d20d-156">OUTPUTS</span></span>

### <span data-ttu-id="3d20d-157">PSResourceManagerError 中的 SdkModels （）</span><span class="sxs-lookup"><span data-stu-id="3d20d-157">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceManagerError</span></span>

## <span data-ttu-id="3d20d-158">筆記</span><span class="sxs-lookup"><span data-stu-id="3d20d-158">NOTES</span></span>

## <span data-ttu-id="3d20d-159">相關連結</span><span class="sxs-lookup"><span data-stu-id="3d20d-159">RELATED LINKS</span></span>
