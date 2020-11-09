---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/test-aztenantdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Test-AzTenantDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Test-AzTenantDeployment.md
ms.openlocfilehash: 5144dacb044523c2ad72d0a9c24aa43427f14f99
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94288067"
---
# <span data-ttu-id="2e6fd-101">Test-AzTenantDeployment</span><span class="sxs-lookup"><span data-stu-id="2e6fd-101">Test-AzTenantDeployment</span></span>

## <span data-ttu-id="2e6fd-102">摘要</span><span class="sxs-lookup"><span data-stu-id="2e6fd-102">SYNOPSIS</span></span>
<span data-ttu-id="2e6fd-103">驗證租使用者範圍內的部署。</span><span class="sxs-lookup"><span data-stu-id="2e6fd-103">Validates a deployment at tenant scope.</span></span>

## <span data-ttu-id="2e6fd-104">句法</span><span class="sxs-lookup"><span data-stu-id="2e6fd-104">SYNTAX</span></span>

### <span data-ttu-id="2e6fd-105">ByTemplateFileWithNoParameters (預設) </span><span class="sxs-lookup"><span data-stu-id="2e6fd-105">ByTemplateFileWithNoParameters (Default)</span></span>
```
Test-AzTenantDeployment -Location <String> -TemplateFile <String> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2e6fd-106">ByTemplateObjectAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="2e6fd-106">ByTemplateObjectAndParameterObject</span></span>
```
Test-AzTenantDeployment -Location <String> -TemplateParameterObject <Hashtable> -TemplateObject <Hashtable>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2e6fd-107">ByTemplateFileAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="2e6fd-107">ByTemplateFileAndParameterObject</span></span>
```
Test-AzTenantDeployment -Location <String> -TemplateParameterObject <Hashtable> -TemplateFile <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2e6fd-108">ByTemplateUriAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="2e6fd-108">ByTemplateUriAndParameterObject</span></span>
```
Test-AzTenantDeployment -Location <String> -TemplateParameterObject <Hashtable> -TemplateUri <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2e6fd-109">ByTemplateObjectAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="2e6fd-109">ByTemplateObjectAndParameterFile</span></span>
```
Test-AzTenantDeployment -Location <String> -TemplateParameterFile <String> -TemplateObject <Hashtable>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2e6fd-110">ByTemplateFileAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="2e6fd-110">ByTemplateFileAndParameterFile</span></span>
```
Test-AzTenantDeployment -Location <String> -TemplateParameterFile <String> -TemplateFile <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2e6fd-111">ByTemplateUriAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="2e6fd-111">ByTemplateUriAndParameterFile</span></span>
```
Test-AzTenantDeployment -Location <String> -TemplateParameterFile <String> -TemplateUri <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2e6fd-112">ByTemplateObjectAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="2e6fd-112">ByTemplateObjectAndParameterUri</span></span>
```
Test-AzTenantDeployment -Location <String> -TemplateParameterUri <String> -TemplateObject <Hashtable>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2e6fd-113">ByTemplateFileAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="2e6fd-113">ByTemplateFileAndParameterUri</span></span>
```
Test-AzTenantDeployment -Location <String> -TemplateParameterUri <String> -TemplateFile <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2e6fd-114">ByTemplateUriAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="2e6fd-114">ByTemplateUriAndParameterUri</span></span>
```
Test-AzTenantDeployment -Location <String> -TemplateParameterUri <String> -TemplateUri <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2e6fd-115">ByTemplateObjectWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="2e6fd-115">ByTemplateObjectWithNoParameters</span></span>
```
Test-AzTenantDeployment -Location <String> -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2e6fd-116">ByTemplateUriWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="2e6fd-116">ByTemplateUriWithNoParameters</span></span>
```
Test-AzTenantDeployment -Location <String> -TemplateUri <String> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2e6fd-117">說明</span><span class="sxs-lookup"><span data-stu-id="2e6fd-117">DESCRIPTION</span></span>
<span data-ttu-id="2e6fd-118">**Test AzTenantDeployment** Cmdlet 會判斷部署範本及其參數值在目前租使用者範圍中是否有效。</span><span class="sxs-lookup"><span data-stu-id="2e6fd-118">The **Test-AzTenantDeployment** cmdlet determines whether a deployment template and its parameter values are valid at the current tenant scope.</span></span>

## <span data-ttu-id="2e6fd-119">示例</span><span class="sxs-lookup"><span data-stu-id="2e6fd-119">EXAMPLES</span></span>

### <span data-ttu-id="2e6fd-120">範例1：使用自訂範本和參數檔案測試部署</span><span class="sxs-lookup"><span data-stu-id="2e6fd-120">Example 1: Test deployment with a custom template and parameter file</span></span>
```
PS C:\> Test-AzTenantDeployment -Location "West US" -TemplateFile "D:\Azure\Templates\OrgSetup.json" -TemplateParameterFile "D:\Azure\Templates\OrgParms.json"
```

<span data-ttu-id="2e6fd-121">這個命令會使用指定的範本檔案和參數檔，在目前的租使用者範圍測試部署。</span><span class="sxs-lookup"><span data-stu-id="2e6fd-121">This command tests a deployment at the current tenant scope using the given template file and parameters file.</span></span>

### <span data-ttu-id="2e6fd-122">範例2：使用自訂範本物件與參數檔案測試部署</span><span class="sxs-lookup"><span data-stu-id="2e6fd-122">Example 2: Test deployment with a custom template object and parameter file</span></span>
```
PS C:\> $TemplateFileText = [System.IO.File]::ReadAllText("D:\Azure\Templates\OrgSetup.json")
PS C:\> $TemplateObject = ConvertFrom-Json $TemplateFileText -AsHashtable
PS C:\> Test-AzTenantDeployment -Location "West US" -TemplateObject $TemplateObject -TemplateParameterFile "D:\Azure\Templates\EngSiteParams.json"
```

<span data-ttu-id="2e6fd-123">這個命令會使用從指定的範本檔案和參數檔案建立的記憶體中 hashtable，在目前的租使用者範圍測試部署。</span><span class="sxs-lookup"><span data-stu-id="2e6fd-123">This command tests a deployment at the current tenant scope using the an in-memory hashtable created from the given template file and a parameter file.</span></span>

## <span data-ttu-id="2e6fd-124">參數</span><span class="sxs-lookup"><span data-stu-id="2e6fd-124">PARAMETERS</span></span>

### <span data-ttu-id="2e6fd-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2e6fd-125">-DefaultProfile</span></span>
<span data-ttu-id="2e6fd-126">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="2e6fd-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2e6fd-127">-位置</span><span class="sxs-lookup"><span data-stu-id="2e6fd-127">-Location</span></span>
<span data-ttu-id="2e6fd-128">儲存部署資料的位置。</span><span class="sxs-lookup"><span data-stu-id="2e6fd-128">The location to store deployment data.</span></span>

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

### <span data-ttu-id="2e6fd-129">-預先</span><span class="sxs-lookup"><span data-stu-id="2e6fd-129">-Pre</span></span>
<span data-ttu-id="2e6fd-130">設定時，表示 Cmdlet 應該使用預發行 API 版本，以便自動判斷要使用的版本。</span><span class="sxs-lookup"><span data-stu-id="2e6fd-130">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="2e6fd-131">-SkipTemplateParameterPrompt</span><span class="sxs-lookup"><span data-stu-id="2e6fd-131">-SkipTemplateParameterPrompt</span></span>
<span data-ttu-id="2e6fd-132">會跳過 PowerShell 動態參數處理，檢查提供的範本參數是否包含範本所使用的所有必要參數。</span><span class="sxs-lookup"><span data-stu-id="2e6fd-132">Skips the PowerShell dynamic parameter processing that checks if the provided template parameter contains all necessary parameters used by the template.</span></span>
<span data-ttu-id="2e6fd-133">這項檢查會提示使用者提供缺少參數的值，但提供-SkipTemplateParameterPrompt 將會在範本中發現未系結的參數時，立即忽略此提示和錯誤。</span><span class="sxs-lookup"><span data-stu-id="2e6fd-133">This check would prompt the user to provide a value for the missing parameters, but providing the -SkipTemplateParameterPrompt will ignore this prompt and error out immediately if a parameter was found not to be bound in the template.</span></span>
<span data-ttu-id="2e6fd-134">在非互動式腳本中，您可以提供 SkipTemplateParameterPrompt，以在不符合所有必要參數的情況下，提供較佳的錯誤訊息。</span><span class="sxs-lookup"><span data-stu-id="2e6fd-134">For non-interactive scripts, -SkipTemplateParameterPrompt can be provided to provide a better error message in the case where not all required parameters are satisfied.</span></span>

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

### <span data-ttu-id="2e6fd-135">-TemplateFile</span><span class="sxs-lookup"><span data-stu-id="2e6fd-135">-TemplateFile</span></span>
<span data-ttu-id="2e6fd-136">範本檔案的本機路徑。</span><span class="sxs-lookup"><span data-stu-id="2e6fd-136">Local path to the template file.</span></span>

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

### <span data-ttu-id="2e6fd-137">-TemplateObject</span><span class="sxs-lookup"><span data-stu-id="2e6fd-137">-TemplateObject</span></span>
<span data-ttu-id="2e6fd-138">代表範本的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="2e6fd-138">A hash table which represents the template.</span></span>

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

### <span data-ttu-id="2e6fd-139">-TemplateParameterFile</span><span class="sxs-lookup"><span data-stu-id="2e6fd-139">-TemplateParameterFile</span></span>
<span data-ttu-id="2e6fd-140">具有範本參數的檔案。</span><span class="sxs-lookup"><span data-stu-id="2e6fd-140">A file that has the template parameters.</span></span>

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

### <span data-ttu-id="2e6fd-141">-TemplateParameterObject</span><span class="sxs-lookup"><span data-stu-id="2e6fd-141">-TemplateParameterObject</span></span>
<span data-ttu-id="2e6fd-142">代表參數的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="2e6fd-142">A hash table which represents the parameters.</span></span>

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

### <span data-ttu-id="2e6fd-143">-TemplateParameterUri</span><span class="sxs-lookup"><span data-stu-id="2e6fd-143">-TemplateParameterUri</span></span>
<span data-ttu-id="2e6fd-144">範本參數檔的 Uri。</span><span class="sxs-lookup"><span data-stu-id="2e6fd-144">Uri to the template parameter file.</span></span>

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

### <span data-ttu-id="2e6fd-145">-TemplateUri</span><span class="sxs-lookup"><span data-stu-id="2e6fd-145">-TemplateUri</span></span>
<span data-ttu-id="2e6fd-146">範本檔案的 Uri。</span><span class="sxs-lookup"><span data-stu-id="2e6fd-146">Uri to the template file.</span></span>

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

### <span data-ttu-id="2e6fd-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2e6fd-147">CommonParameters</span></span>
<span data-ttu-id="2e6fd-148">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="2e6fd-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2e6fd-149">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="2e6fd-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2e6fd-150">輸入</span><span class="sxs-lookup"><span data-stu-id="2e6fd-150">INPUTS</span></span>

### <span data-ttu-id="2e6fd-151">[System.object] 集合. Hashtable</span><span class="sxs-lookup"><span data-stu-id="2e6fd-151">System.Collections.Hashtable</span></span>

### <span data-ttu-id="2e6fd-152">System.object</span><span class="sxs-lookup"><span data-stu-id="2e6fd-152">System.String</span></span>

## <span data-ttu-id="2e6fd-153">輸出</span><span class="sxs-lookup"><span data-stu-id="2e6fd-153">OUTPUTS</span></span>

### <span data-ttu-id="2e6fd-154">PSResourceManagerError 中的 SdkModels （）</span><span class="sxs-lookup"><span data-stu-id="2e6fd-154">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceManagerError</span></span>

## <span data-ttu-id="2e6fd-155">筆記</span><span class="sxs-lookup"><span data-stu-id="2e6fd-155">NOTES</span></span>

## <span data-ttu-id="2e6fd-156">相關連結</span><span class="sxs-lookup"><span data-stu-id="2e6fd-156">RELATED LINKS</span></span>
