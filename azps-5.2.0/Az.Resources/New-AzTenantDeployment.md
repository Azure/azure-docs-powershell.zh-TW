---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-aztenantdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzTenantDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzTenantDeployment.md
ms.openlocfilehash: 8135dc4c4bdb6eb21761dbf5cb7ecea216a81593
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98280814"
---
# <span data-ttu-id="cb809-101">New-AzTenantDeployment</span><span class="sxs-lookup"><span data-stu-id="cb809-101">New-AzTenantDeployment</span></span>

## <span data-ttu-id="cb809-102">摘要</span><span class="sxs-lookup"><span data-stu-id="cb809-102">SYNOPSIS</span></span>
<span data-ttu-id="cb809-103">在租使用者範圍建立部署</span><span class="sxs-lookup"><span data-stu-id="cb809-103">Create a deployment at tenant scope</span></span>

## <span data-ttu-id="cb809-104">句法</span><span class="sxs-lookup"><span data-stu-id="cb809-104">SYNTAX</span></span>

### <span data-ttu-id="cb809-105">ByTemplateFileWithNoParameters (預設) </span><span class="sxs-lookup"><span data-stu-id="cb809-105">ByTemplateFileWithNoParameters (Default)</span></span>
```
New-AzTenantDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-AsJob]
 -TemplateFile <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cb809-106">ByTemplateObjectAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="cb809-106">ByTemplateObjectAndParameterObject</span></span>
```
New-AzTenantDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-AsJob]
 -TemplateParameterObject <Hashtable> -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cb809-107">ByTemplateFileAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="cb809-107">ByTemplateFileAndParameterObject</span></span>
```
New-AzTenantDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-AsJob]
 -TemplateParameterObject <Hashtable> -TemplateFile <String> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cb809-108">ByTemplateUriAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="cb809-108">ByTemplateUriAndParameterObject</span></span>
```
New-AzTenantDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-AsJob]
 -TemplateParameterObject <Hashtable> -TemplateUri <String> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cb809-109">ByTemplateObjectAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="cb809-109">ByTemplateObjectAndParameterFile</span></span>
```
New-AzTenantDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-AsJob]
 -TemplateParameterFile <String> -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cb809-110">ByTemplateFileAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="cb809-110">ByTemplateFileAndParameterFile</span></span>
```
New-AzTenantDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-AsJob]
 -TemplateParameterFile <String> -TemplateFile <String> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cb809-111">ByTemplateUriAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="cb809-111">ByTemplateUriAndParameterFile</span></span>
```
New-AzTenantDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-AsJob]
 -TemplateParameterFile <String> -TemplateUri <String> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cb809-112">ByTemplateObjectAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="cb809-112">ByTemplateObjectAndParameterUri</span></span>
```
New-AzTenantDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-AsJob]
 -TemplateParameterUri <String> -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cb809-113">ByTemplateFileAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="cb809-113">ByTemplateFileAndParameterUri</span></span>
```
New-AzTenantDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-AsJob]
 -TemplateParameterUri <String> -TemplateFile <String> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cb809-114">ByTemplateUriAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="cb809-114">ByTemplateUriAndParameterUri</span></span>
```
New-AzTenantDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-AsJob]
 -TemplateParameterUri <String> -TemplateUri <String> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cb809-115">ByTemplateObjectWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="cb809-115">ByTemplateObjectWithNoParameters</span></span>
```
New-AzTenantDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-AsJob]
 -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cb809-116">ByTemplateUriWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="cb809-116">ByTemplateUriWithNoParameters</span></span>
```
New-AzTenantDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-AsJob]
 -TemplateUri <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cb809-117">說明</span><span class="sxs-lookup"><span data-stu-id="cb809-117">DESCRIPTION</span></span>
<span data-ttu-id="cb809-118">**新的-AzTenantDeployment** Cmdlet 會在目前的租使用者範圍內新增部署。</span><span class="sxs-lookup"><span data-stu-id="cb809-118">The **New-AzTenantDeployment** cmdlet adds a deployment at the current tenant scope.</span></span>

<span data-ttu-id="cb809-119">若要在租使用者範圍中新增部署，請指定位置和範本。</span><span class="sxs-lookup"><span data-stu-id="cb809-119">To add a deployment at tenant scope, specify the location and a template.</span></span>
<span data-ttu-id="cb809-120">位置會告知 Azure 資源管理員要儲存部署資料的位置。</span><span class="sxs-lookup"><span data-stu-id="cb809-120">The location tells Azure Resource Manager where to store the deployment data.</span></span> <span data-ttu-id="cb809-121">範本是一個 JSON 字串，其中包含要部署的個別資源。</span><span class="sxs-lookup"><span data-stu-id="cb809-121">The template is a JSON string that contains individual resources to be deployed.</span></span>
<span data-ttu-id="cb809-122">範本包含必要資源的參數預留位置，以及可設定的屬性值，例如名稱和大小。</span><span class="sxs-lookup"><span data-stu-id="cb809-122">The template includes parameter placeholders for required resources and configurable property values, such as names and sizes.</span></span>

<span data-ttu-id="cb809-123">若要在部署中使用自訂範本，請指定 *TemplateFile* 參數或 *TemplateUri* 參數。</span><span class="sxs-lookup"><span data-stu-id="cb809-123">To use a custom template for the deployment, specify the *TemplateFile* parameter or *TemplateUri* parameter.</span></span>
<span data-ttu-id="cb809-124">每個範本都有可設定屬性的參數。</span><span class="sxs-lookup"><span data-stu-id="cb809-124">Each template has parameters for configurable properties.</span></span>
<span data-ttu-id="cb809-125">若要指定範本參數的值，請指定 *TemplateParameterFile* 參數或 *TemplateParameterObject* 參數。</span><span class="sxs-lookup"><span data-stu-id="cb809-125">To specify values for the template parameters, specify the *TemplateParameterFile* parameter or the *TemplateParameterObject* parameter.</span></span>
<span data-ttu-id="cb809-126">或者，您也可以使用在指定範本時動態新增到命令中的範本參數。</span><span class="sxs-lookup"><span data-stu-id="cb809-126">Alternatively, you can use the template parameters that are dynamically added to the command when you specify a template.</span></span>
<span data-ttu-id="cb809-127">若要使用動態參數，請在命令提示字元輸入，或輸入減號 ( ) 來指示參數，然後使用 Tab 鍵來迴圈顯示可用的參數。</span><span class="sxs-lookup"><span data-stu-id="cb809-127">To use dynamic parameters, type them at the command prompt, or type a minus sign (-) to indicate a parameter and use the Tab key to cycle through available parameters.</span></span>
<span data-ttu-id="cb809-128">您在命令提示字元中輸入的範本參數值會優先于範本參數物件或檔案中的值。</span><span class="sxs-lookup"><span data-stu-id="cb809-128">Template parameter values that you enter at the command prompt take precedence over values in a template parameter object or file.</span></span>

<span data-ttu-id="cb809-129">若要將資源新增至資源群組，請使用 **New-AzResourceGroupDeployment** ，這會在資源群組建立部署。</span><span class="sxs-lookup"><span data-stu-id="cb809-129">To add resources to a resource group, use the **New-AzResourceGroupDeployment** which creates a deployment at a resource group.</span></span>
<span data-ttu-id="cb809-130">若要將資源新增至訂閱，請使用 **新的-AzSubscriptionDeployment** ，這會在訂閱範圍中建立部署，以部署訂閱層級資源。</span><span class="sxs-lookup"><span data-stu-id="cb809-130">To add resources to a subscription, use the **New-AzSubscriptionDeployment** which creates a deployment at subscription scope, which deploys subscription level resources.</span></span>
<span data-ttu-id="cb809-131">若要在管理群組新增資源，請使用 [ **New-AzManagementGroupDeployment** ]，在管理群組建立部署。</span><span class="sxs-lookup"><span data-stu-id="cb809-131">To add resources at a management group, use the **New-AzManagementGroupDeployment** which creates a deployment at a management group.</span></span>

## <span data-ttu-id="cb809-132">示例</span><span class="sxs-lookup"><span data-stu-id="cb809-132">EXAMPLES</span></span>

### <span data-ttu-id="cb809-133">範例1：使用自訂範本和參數檔案建立部署</span><span class="sxs-lookup"><span data-stu-id="cb809-133">Example 1: Use a custom template and parameter file to create a deployment</span></span>
```
PS C:\> New-AzTenantDeployment -Location "West US" -TemplateFile "D:\Azure\Templates\OrgSetup.json" -TemplateParameterFile "D:\Azure\Templates\OrgParms.json" -Tag @{"key1"="value1"; "key2"="value2";}
```

<span data-ttu-id="cb809-134">這個命令會使用自訂的範本與磁片上的範本檔案（含已定義的 tags 參數），在目前租使用者範圍內建立新的部署。</span><span class="sxs-lookup"><span data-stu-id="cb809-134">This command creates a new deployment at the current tenant scope by using a custom template and a template file on disk, with defined tags parameter.</span></span>
<span data-ttu-id="cb809-135">此命令會使用 *TemplateFile* 參數來指定範本和 *TemplateParameterFile* 參數，以指定包含參數和參數值的檔案。</span><span class="sxs-lookup"><span data-stu-id="cb809-135">The command uses the *TemplateFile* parameter to specify the template and the *TemplateParameterFile* parameter to specify a file that contains parameters and parameter values.</span></span>

### <span data-ttu-id="cb809-136">範例2：使用自訂範本物件與參數檔案建立部署</span><span class="sxs-lookup"><span data-stu-id="cb809-136">Example 2: Use a custom template object and parameter file to create a deployment</span></span>
```
PS C:\> $TemplateFileText = [System.IO.File]::ReadAllText("D:\Azure\Templates\OrgSetup.json")
PS C:\> $TemplateObject = ConvertFrom-Json $TemplateFileText -AsHashtable
PS C:\> New-AzTenantDeployment -Location "West US" -TemplateObject $TemplateObject -TemplateParameterFile "D:\Azure\Templates\OrgParams.json"
```

<span data-ttu-id="cb809-137">這個命令會在目前的租使用者中建立新的部署，方法是使用自訂範本，以及磁片上已轉換成記憶體中的 hashtable 的範本檔案。</span><span class="sxs-lookup"><span data-stu-id="cb809-137">This command creates a new deployment at the current tenant by using a custom template and a template file on disk that has been converted to an in-memory hashtable.</span></span>
<span data-ttu-id="cb809-138">前兩個命令會讀取磁片上範本檔案的文字，並將它轉換成記憶體中的 hashtable。</span><span class="sxs-lookup"><span data-stu-id="cb809-138">The first two commands read the text for the template file on disk and convert it to an in-memory hashtable.</span></span>
<span data-ttu-id="cb809-139">最後一個命令使用 *TemplateObject* 參數來指定此 Hashtable 和 *TemplateParameterFile* 參數，以指定包含參數和參數值的檔案。</span><span class="sxs-lookup"><span data-stu-id="cb809-139">The last command uses the *TemplateObject* parameter to specify this hashtable and the *TemplateParameterFile* parameter to specify a file that contains parameters and parameter values.</span></span>

## <span data-ttu-id="cb809-140">參數</span><span class="sxs-lookup"><span data-stu-id="cb809-140">PARAMETERS</span></span>

### <span data-ttu-id="cb809-141">-AsJob</span><span class="sxs-lookup"><span data-stu-id="cb809-141">-AsJob</span></span>
<span data-ttu-id="cb809-142">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="cb809-142">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="cb809-143">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cb809-143">-DefaultProfile</span></span>
<span data-ttu-id="cb809-144">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="cb809-144">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cb809-145">-DeploymentDebugLogLevel</span><span class="sxs-lookup"><span data-stu-id="cb809-145">-DeploymentDebugLogLevel</span></span>
<span data-ttu-id="cb809-146">部署調試記錄層級。</span><span class="sxs-lookup"><span data-stu-id="cb809-146">The deployment debug log level.</span></span>

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

### <span data-ttu-id="cb809-147">-位置</span><span class="sxs-lookup"><span data-stu-id="cb809-147">-Location</span></span>
<span data-ttu-id="cb809-148">儲存部署資料的位置。</span><span class="sxs-lookup"><span data-stu-id="cb809-148">The location to store deployment data.</span></span>

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

### <span data-ttu-id="cb809-149">-名稱</span><span class="sxs-lookup"><span data-stu-id="cb809-149">-Name</span></span>
<span data-ttu-id="cb809-150">將要建立之部署的名稱。</span><span class="sxs-lookup"><span data-stu-id="cb809-150">The name of the deployment it's going to create.</span></span> <span data-ttu-id="cb809-151">如果未指定，則預設為提供範本檔時的範本檔案名;預設為提供範本物件的目前時間（例如 "20131223140835"）。</span><span class="sxs-lookup"><span data-stu-id="cb809-151">If not specified, defaults to the template file name when a template file is provided; defaults to the current time when a template object is provided, e.g. "20131223140835".</span></span>

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

### <span data-ttu-id="cb809-152">-預先</span><span class="sxs-lookup"><span data-stu-id="cb809-152">-Pre</span></span>
<span data-ttu-id="cb809-153">設定時，表示 Cmdlet 應該使用預發行 API 版本，以便自動判斷要使用的版本。</span><span class="sxs-lookup"><span data-stu-id="cb809-153">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="cb809-154">-SkipTemplateParameterPrompt</span><span class="sxs-lookup"><span data-stu-id="cb809-154">-SkipTemplateParameterPrompt</span></span>
<span data-ttu-id="cb809-155">會跳過 PowerShell 動態參數處理，檢查提供的範本參數是否包含範本所使用的所有必要參數。</span><span class="sxs-lookup"><span data-stu-id="cb809-155">Skips the PowerShell dynamic parameter processing that checks if the provided template parameter contains all necessary parameters used by the template.</span></span>
<span data-ttu-id="cb809-156">這項檢查會提示使用者提供缺少參數的值，但提供-SkipTemplateParameterPrompt 將會在範本中發現未系結的參數時，立即忽略此提示和錯誤。</span><span class="sxs-lookup"><span data-stu-id="cb809-156">This check would prompt the user to provide a value for the missing parameters, but providing the -SkipTemplateParameterPrompt will ignore this prompt and error out immediately if a parameter was found not to be bound in the template.</span></span>
<span data-ttu-id="cb809-157">在非互動式腳本中，您可以提供 SkipTemplateParameterPrompt，以在不符合所有必要參數的情況下，提供較佳的錯誤訊息。</span><span class="sxs-lookup"><span data-stu-id="cb809-157">For non-interactive scripts, -SkipTemplateParameterPrompt can be provided to provide a better error message in the case where not all required parameters are satisfied.</span></span>

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

### <span data-ttu-id="cb809-158">-Tag</span><span class="sxs-lookup"><span data-stu-id="cb809-158">-Tag</span></span>
<span data-ttu-id="cb809-159">要放在部署上的標記。</span><span class="sxs-lookup"><span data-stu-id="cb809-159">The tags to put on the deployment.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cb809-160">-TemplateFile</span><span class="sxs-lookup"><span data-stu-id="cb809-160">-TemplateFile</span></span>
<span data-ttu-id="cb809-161">範本檔案的本機路徑。</span><span class="sxs-lookup"><span data-stu-id="cb809-161">Local path to the template file.</span></span>

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

### <span data-ttu-id="cb809-162">-TemplateObject</span><span class="sxs-lookup"><span data-stu-id="cb809-162">-TemplateObject</span></span>
<span data-ttu-id="cb809-163">代表範本的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="cb809-163">A hash table which represents the template.</span></span>

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

### <span data-ttu-id="cb809-164">-TemplateParameterFile</span><span class="sxs-lookup"><span data-stu-id="cb809-164">-TemplateParameterFile</span></span>
<span data-ttu-id="cb809-165">具有範本參數的檔案。</span><span class="sxs-lookup"><span data-stu-id="cb809-165">A file that has the template parameters.</span></span>

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

### <span data-ttu-id="cb809-166">-TemplateParameterObject</span><span class="sxs-lookup"><span data-stu-id="cb809-166">-TemplateParameterObject</span></span>
<span data-ttu-id="cb809-167">代表參數的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="cb809-167">A hash table which represents the parameters.</span></span>

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

### <span data-ttu-id="cb809-168">-TemplateParameterUri</span><span class="sxs-lookup"><span data-stu-id="cb809-168">-TemplateParameterUri</span></span>
<span data-ttu-id="cb809-169">範本參數檔的 Uri。</span><span class="sxs-lookup"><span data-stu-id="cb809-169">Uri to the template parameter file.</span></span>

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

### <span data-ttu-id="cb809-170">-TemplateUri</span><span class="sxs-lookup"><span data-stu-id="cb809-170">-TemplateUri</span></span>
<span data-ttu-id="cb809-171">範本檔案的 Uri。</span><span class="sxs-lookup"><span data-stu-id="cb809-171">Uri to the template file.</span></span>

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

### <span data-ttu-id="cb809-172">-WhatIfExcludeChangeType</span><span class="sxs-lookup"><span data-stu-id="cb809-172">-WhatIfExcludeChangeType</span></span>
<span data-ttu-id="cb809-173">要從 What-If 結果中排除的逗號分隔資源變更類型。</span><span class="sxs-lookup"><span data-stu-id="cb809-173">Comma-separated resource change types to be excluded from What-If results.</span></span> <span data-ttu-id="cb809-174">在設定了-WhatIf 或-Confirm 切換時適用。</span><span class="sxs-lookup"><span data-stu-id="cb809-174">Applicable when the -WhatIf or -Confirm switch is set.</span></span>

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

### <span data-ttu-id="cb809-175">-WhatIfResultFormat</span><span class="sxs-lookup"><span data-stu-id="cb809-175">-WhatIfResultFormat</span></span>
<span data-ttu-id="cb809-176">What-If 的結果格式。</span><span class="sxs-lookup"><span data-stu-id="cb809-176">The What-If result format.</span></span> <span data-ttu-id="cb809-177">在設定了-WhatIf 或-Confirm 切換時適用。</span><span class="sxs-lookup"><span data-stu-id="cb809-177">Applicable when the -WhatIf or -Confirm switch is set.</span></span>

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

### <span data-ttu-id="cb809-178">-確認</span><span class="sxs-lookup"><span data-stu-id="cb809-178">-Confirm</span></span>
<span data-ttu-id="cb809-179">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="cb809-179">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cb809-180">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cb809-180">-WhatIf</span></span>
<span data-ttu-id="cb809-181">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="cb809-181">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cb809-182">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="cb809-182">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cb809-183">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cb809-183">CommonParameters</span></span>
<span data-ttu-id="cb809-184">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="cb809-184">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cb809-185">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="cb809-185">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cb809-186">輸入</span><span class="sxs-lookup"><span data-stu-id="cb809-186">INPUTS</span></span>

### <span data-ttu-id="cb809-187">[System.object] 集合. Hashtable</span><span class="sxs-lookup"><span data-stu-id="cb809-187">System.Collections.Hashtable</span></span>

### <span data-ttu-id="cb809-188">System.object</span><span class="sxs-lookup"><span data-stu-id="cb809-188">System.String</span></span>

## <span data-ttu-id="cb809-189">輸出</span><span class="sxs-lookup"><span data-stu-id="cb809-189">OUTPUTS</span></span>

### <span data-ttu-id="cb809-190">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span><span class="sxs-lookup"><span data-stu-id="cb809-190">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="cb809-191">筆記</span><span class="sxs-lookup"><span data-stu-id="cb809-191">NOTES</span></span>

## <span data-ttu-id="cb809-192">相關連結</span><span class="sxs-lookup"><span data-stu-id="cb809-192">RELATED LINKS</span></span>
