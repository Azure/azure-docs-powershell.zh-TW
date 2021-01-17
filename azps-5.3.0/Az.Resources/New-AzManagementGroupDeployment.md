---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-azmanagementgroupdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzManagementGroupDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzManagementGroupDeployment.md
ms.openlocfilehash: a04c19df84626fd08968e1950074306dfd7cf1ab
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98435452"
---
# <span data-ttu-id="5ff02-101">New-AzManagementGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="5ff02-101">New-AzManagementGroupDeployment</span></span>

## <span data-ttu-id="5ff02-102">摘要</span><span class="sxs-lookup"><span data-stu-id="5ff02-102">SYNOPSIS</span></span>
<span data-ttu-id="5ff02-103">在管理群組建立部署</span><span class="sxs-lookup"><span data-stu-id="5ff02-103">Create a deployment at a management group</span></span>

## <span data-ttu-id="5ff02-104">句法</span><span class="sxs-lookup"><span data-stu-id="5ff02-104">SYNTAX</span></span>

### <span data-ttu-id="5ff02-105">ByTemplateFileWithNoParameters (預設) </span><span class="sxs-lookup"><span data-stu-id="5ff02-105">ByTemplateFileWithNoParameters (Default)</span></span>
```
New-AzManagementGroupDeployment [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>]
 [-WhatIfExcludeChangeType <String[]>] [-AsJob] -TemplateFile <String> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5ff02-106">ByTemplateObjectAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="5ff02-106">ByTemplateObjectAndParameterObject</span></span>
```
New-AzManagementGroupDeployment [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>]
 [-WhatIfExcludeChangeType <String[]>] [-AsJob] -TemplateParameterObject <Hashtable>
 -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5ff02-107">ByTemplateFileAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="5ff02-107">ByTemplateFileAndParameterObject</span></span>
```
New-AzManagementGroupDeployment [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>]
 [-WhatIfExcludeChangeType <String[]>] [-AsJob] -TemplateParameterObject <Hashtable> -TemplateFile <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="5ff02-108">ByTemplateUriAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="5ff02-108">ByTemplateUriAndParameterObject</span></span>
```
New-AzManagementGroupDeployment [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>]
 [-WhatIfExcludeChangeType <String[]>] [-AsJob] -TemplateParameterObject <Hashtable> -TemplateUri <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="5ff02-109">ByTemplateObjectAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="5ff02-109">ByTemplateObjectAndParameterFile</span></span>
```
New-AzManagementGroupDeployment [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>]
 [-WhatIfExcludeChangeType <String[]>] [-AsJob] -TemplateParameterFile <String> -TemplateObject <Hashtable>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="5ff02-110">ByTemplateFileAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="5ff02-110">ByTemplateFileAndParameterFile</span></span>
```
New-AzManagementGroupDeployment [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>]
 [-WhatIfExcludeChangeType <String[]>] [-AsJob] -TemplateParameterFile <String> -TemplateFile <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="5ff02-111">ByTemplateUriAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="5ff02-111">ByTemplateUriAndParameterFile</span></span>
```
New-AzManagementGroupDeployment [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>]
 [-WhatIfExcludeChangeType <String[]>] [-AsJob] -TemplateParameterFile <String> -TemplateUri <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="5ff02-112">ByTemplateObjectAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="5ff02-112">ByTemplateObjectAndParameterUri</span></span>
```
New-AzManagementGroupDeployment [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>]
 [-WhatIfExcludeChangeType <String[]>] [-AsJob] -TemplateParameterUri <String> -TemplateObject <Hashtable>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="5ff02-113">ByTemplateFileAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="5ff02-113">ByTemplateFileAndParameterUri</span></span>
```
New-AzManagementGroupDeployment [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>]
 [-WhatIfExcludeChangeType <String[]>] [-AsJob] -TemplateParameterUri <String> -TemplateFile <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="5ff02-114">ByTemplateUriAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="5ff02-114">ByTemplateUriAndParameterUri</span></span>
```
New-AzManagementGroupDeployment [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>]
 [-WhatIfExcludeChangeType <String[]>] [-AsJob] -TemplateParameterUri <String> -TemplateUri <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="5ff02-115">ByTemplateObjectWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="5ff02-115">ByTemplateObjectWithNoParameters</span></span>
```
New-AzManagementGroupDeployment [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>]
 [-WhatIfExcludeChangeType <String[]>] [-AsJob] -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5ff02-116">ByTemplateUriWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="5ff02-116">ByTemplateUriWithNoParameters</span></span>
```
New-AzManagementGroupDeployment [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>]
 [-WhatIfExcludeChangeType <String[]>] [-AsJob] -TemplateUri <String> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5ff02-117">說明</span><span class="sxs-lookup"><span data-stu-id="5ff02-117">DESCRIPTION</span></span>
<span data-ttu-id="5ff02-118">**新的-AzManagementGroupDeployment** Cmdlet 會在管理群組新增部署。</span><span class="sxs-lookup"><span data-stu-id="5ff02-118">The **New-AzManagementGroupDeployment** cmdlet adds a deployment at a management group.</span></span>

<span data-ttu-id="5ff02-119">若要在管理群組新增部署，請指定管理群組、位置及範本。</span><span class="sxs-lookup"><span data-stu-id="5ff02-119">To add a deployment at a management group, specify the management group, location and a template.</span></span>
<span data-ttu-id="5ff02-120">位置會告知 Azure 資源管理員要儲存部署資料的位置。</span><span class="sxs-lookup"><span data-stu-id="5ff02-120">The location tells Azure Resource Manager where to store the deployment data.</span></span> <span data-ttu-id="5ff02-121">範本是一個 JSON 字串，其中包含要部署的個別資源。</span><span class="sxs-lookup"><span data-stu-id="5ff02-121">The template is a JSON string that contains individual resources to be deployed.</span></span>
<span data-ttu-id="5ff02-122">範本包含必要資源的參數預留位置，以及可設定的屬性值，例如名稱和大小。</span><span class="sxs-lookup"><span data-stu-id="5ff02-122">The template includes parameter placeholders for required resources and configurable property values, such as names and sizes.</span></span>

<span data-ttu-id="5ff02-123">若要在部署中使用自訂範本，請指定 *TemplateFile* 參數或 *TemplateUri* 參數。</span><span class="sxs-lookup"><span data-stu-id="5ff02-123">To use a custom template for the deployment, specify the *TemplateFile* parameter or *TemplateUri* parameter.</span></span>
<span data-ttu-id="5ff02-124">每個範本都有可設定屬性的參數。</span><span class="sxs-lookup"><span data-stu-id="5ff02-124">Each template has parameters for configurable properties.</span></span>
<span data-ttu-id="5ff02-125">若要指定範本參數的值，請指定 *TemplateParameterFile* 參數或 *TemplateParameterObject* 參數。</span><span class="sxs-lookup"><span data-stu-id="5ff02-125">To specify values for the template parameters, specify the *TemplateParameterFile* parameter or the *TemplateParameterObject* parameter.</span></span>
<span data-ttu-id="5ff02-126">或者，您也可以使用在指定範本時動態新增到命令中的範本參數。</span><span class="sxs-lookup"><span data-stu-id="5ff02-126">Alternatively, you can use the template parameters that are dynamically added to the command when you specify a template.</span></span>
<span data-ttu-id="5ff02-127">若要使用動態參數，請在命令提示字元輸入，或輸入減號 ( ) 來指示參數，然後使用 Tab 鍵來迴圈顯示可用的參數。</span><span class="sxs-lookup"><span data-stu-id="5ff02-127">To use dynamic parameters, type them at the command prompt, or type a minus sign (-) to indicate a parameter and use the Tab key to cycle through available parameters.</span></span>
<span data-ttu-id="5ff02-128">您在命令提示字元中輸入的範本參數值會優先于範本參數物件或檔案中的值。</span><span class="sxs-lookup"><span data-stu-id="5ff02-128">Template parameter values that you enter at the command prompt take precedence over values in a template parameter object or file.</span></span>

<span data-ttu-id="5ff02-129">若要將資源新增至資源群組，請使用 **New-AzResourceGroupDeployment** ，這會在資源群組建立部署。</span><span class="sxs-lookup"><span data-stu-id="5ff02-129">To add resources to a resource group, use the **New-AzResourceGroupDeployment** which creates a deployment at a resource group.</span></span>
<span data-ttu-id="5ff02-130">若要將資源新增至訂閱，請使用 **新的-AzSubscriptionDeployment** ，這會在訂閱範圍中建立部署，以部署訂閱層級資源。</span><span class="sxs-lookup"><span data-stu-id="5ff02-130">To add resources to a subscription, use the **New-AzSubscriptionDeployment** which creates a deployment at subscription scope, which deploys subscription level resources.</span></span>
<span data-ttu-id="5ff02-131">若要在租使用者範圍中新增資源，請使用 **新的-AzTenantDeployment** ，這會在租使用者範圍中建立部署。</span><span class="sxs-lookup"><span data-stu-id="5ff02-131">To add resources at tenant scope, use the **New-AzTenantDeployment** which creates a deployment at tenant scope.</span></span>

## <span data-ttu-id="5ff02-132">示例</span><span class="sxs-lookup"><span data-stu-id="5ff02-132">EXAMPLES</span></span>

### <span data-ttu-id="5ff02-133">範例1：使用自訂範本和參數檔案建立部署</span><span class="sxs-lookup"><span data-stu-id="5ff02-133">Example 1: Use a custom template and parameter file to create a deployment</span></span>
```
PS C:\> New-AzManagementGroupDeployment -ManagementGroupId "myMG" -Location "West US" -TemplateFile "D:\Azure\Templates\OrgSetup.json" -TemplateParameterFile "D:\Azure\Templates\OrgParms.json" -Tag @{"key1"="value1"; "key2"="value2";}
```

<span data-ttu-id="5ff02-134">這個命令會使用自訂的範本，以及磁片上的範本檔案（含已定義的 tags 參數），在管理群組「myMG」建立新的部署。</span><span class="sxs-lookup"><span data-stu-id="5ff02-134">This command creates a new deployment at the management group "myMG" by using a custom template and a template file on disk, with defined tags parameter.</span></span>
<span data-ttu-id="5ff02-135">此命令會使用 *TemplateFile* 參數來指定範本和 *TemplateParameterFile* 參數，以指定包含參數和參數值的檔案。</span><span class="sxs-lookup"><span data-stu-id="5ff02-135">The command uses the *TemplateFile* parameter to specify the template and the *TemplateParameterFile* parameter to specify a file that contains parameters and parameter values.</span></span>

### <span data-ttu-id="5ff02-136">範例2：使用自訂範本物件與參數檔案建立部署</span><span class="sxs-lookup"><span data-stu-id="5ff02-136">Example 2: Use a custom template object and parameter file to create a deployment</span></span>
```
PS C:\> $TemplateFileText = [System.IO.File]::ReadAllText("D:\Azure\Templates\OrgSetup.json")
PS C:\> $TemplateObject = ConvertFrom-Json $TemplateFileText -AsHashtable
PS C:\> New-AzManagementGroupDeployment -ManagementGroupId "myMG" -Location "West US" -TemplateObject $TemplateObject -TemplateParameterFile "D:\Azure\Templates\OrgParams.json"
```

<span data-ttu-id="5ff02-137">這個命令會使用自訂範本與磁片上已轉換成記憶體中的 hashtable 的範本檔案，在管理群組「myMG」建立新的部署。</span><span class="sxs-lookup"><span data-stu-id="5ff02-137">This command creates a new deployment at the management group "myMG" by using a custom template and a template file on disk that has been converted to an in-memory hashtable.</span></span>
<span data-ttu-id="5ff02-138">前兩個命令會讀取磁片上範本檔案的文字，並將它轉換成記憶體中的 hashtable。</span><span class="sxs-lookup"><span data-stu-id="5ff02-138">The first two commands read the text for the template file on disk and convert it to an in-memory hashtable.</span></span>
<span data-ttu-id="5ff02-139">最後一個命令使用 *TemplateObject* 參數來指定此 Hashtable 和 *TemplateParameterFile* 參數，以指定包含參數和參數值的檔案。</span><span class="sxs-lookup"><span data-stu-id="5ff02-139">The last command uses the *TemplateObject* parameter to specify this hashtable and the *TemplateParameterFile* parameter to specify a file that contains parameters and parameter values.</span></span>

## <span data-ttu-id="5ff02-140">參數</span><span class="sxs-lookup"><span data-stu-id="5ff02-140">PARAMETERS</span></span>

### <span data-ttu-id="5ff02-141">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5ff02-141">-AsJob</span></span>
<span data-ttu-id="5ff02-142">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="5ff02-142">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="5ff02-143">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5ff02-143">-DefaultProfile</span></span>
<span data-ttu-id="5ff02-144">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="5ff02-144">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5ff02-145">-DeploymentDebugLogLevel</span><span class="sxs-lookup"><span data-stu-id="5ff02-145">-DeploymentDebugLogLevel</span></span>
<span data-ttu-id="5ff02-146">部署調試記錄層級。</span><span class="sxs-lookup"><span data-stu-id="5ff02-146">The deployment debug log level.</span></span>

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

### <span data-ttu-id="5ff02-147">-位置</span><span class="sxs-lookup"><span data-stu-id="5ff02-147">-Location</span></span>
<span data-ttu-id="5ff02-148">儲存部署資料的位置。</span><span class="sxs-lookup"><span data-stu-id="5ff02-148">The location to store deployment data.</span></span>

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

### <span data-ttu-id="5ff02-149">-ManagementGroupId</span><span class="sxs-lookup"><span data-stu-id="5ff02-149">-ManagementGroupId</span></span>
<span data-ttu-id="5ff02-150">管理群組識別碼。</span><span class="sxs-lookup"><span data-stu-id="5ff02-150">The management group ID.</span></span>

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

### <span data-ttu-id="5ff02-151">-名稱</span><span class="sxs-lookup"><span data-stu-id="5ff02-151">-Name</span></span>
<span data-ttu-id="5ff02-152">將要建立之部署的名稱。</span><span class="sxs-lookup"><span data-stu-id="5ff02-152">The name of the deployment it's going to create.</span></span> <span data-ttu-id="5ff02-153">如果未指定，則預設為提供範本檔時的範本檔案名;預設為提供範本物件的目前時間（例如 "20131223140835"）。</span><span class="sxs-lookup"><span data-stu-id="5ff02-153">If not specified, defaults to the template file name when a template file is provided; defaults to the current time when a template object is provided, e.g. "20131223140835".</span></span>

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

### <span data-ttu-id="5ff02-154">-預先</span><span class="sxs-lookup"><span data-stu-id="5ff02-154">-Pre</span></span>
<span data-ttu-id="5ff02-155">設定時，表示 Cmdlet 應該使用預發行 API 版本，以便自動判斷要使用的版本。</span><span class="sxs-lookup"><span data-stu-id="5ff02-155">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="5ff02-156">-SkipTemplateParameterPrompt</span><span class="sxs-lookup"><span data-stu-id="5ff02-156">-SkipTemplateParameterPrompt</span></span>
<span data-ttu-id="5ff02-157">會跳過 PowerShell 動態參數處理，檢查提供的範本參數是否包含範本所使用的所有必要參數。</span><span class="sxs-lookup"><span data-stu-id="5ff02-157">Skips the PowerShell dynamic parameter processing that checks if the provided template parameter contains all necessary parameters used by the template.</span></span>
<span data-ttu-id="5ff02-158">這項檢查會提示使用者提供缺少參數的值，但提供-SkipTemplateParameterPrompt 將會在範本中發現未系結的參數時，立即忽略此提示和錯誤。</span><span class="sxs-lookup"><span data-stu-id="5ff02-158">This check would prompt the user to provide a value for the missing parameters, but providing the -SkipTemplateParameterPrompt will ignore this prompt and error out immediately if a parameter was found not to be bound in the template.</span></span>
<span data-ttu-id="5ff02-159">在非互動式腳本中，您可以提供 SkipTemplateParameterPrompt，以在不符合所有必要參數的情況下，提供較佳的錯誤訊息。</span><span class="sxs-lookup"><span data-stu-id="5ff02-159">For non-interactive scripts, -SkipTemplateParameterPrompt can be provided to provide a better error message in the case where not all required parameters are satisfied.</span></span>

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

### <span data-ttu-id="5ff02-160">-Tag</span><span class="sxs-lookup"><span data-stu-id="5ff02-160">-Tag</span></span>
<span data-ttu-id="5ff02-161">要放在部署上的標記。</span><span class="sxs-lookup"><span data-stu-id="5ff02-161">The tags to put on the deployment.</span></span>

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

### <span data-ttu-id="5ff02-162">-TemplateFile</span><span class="sxs-lookup"><span data-stu-id="5ff02-162">-TemplateFile</span></span>
<span data-ttu-id="5ff02-163">範本檔案的本機路徑。</span><span class="sxs-lookup"><span data-stu-id="5ff02-163">Local path to the template file.</span></span>

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

### <span data-ttu-id="5ff02-164">-TemplateObject</span><span class="sxs-lookup"><span data-stu-id="5ff02-164">-TemplateObject</span></span>
<span data-ttu-id="5ff02-165">代表範本的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="5ff02-165">A hash table which represents the template.</span></span>

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

### <span data-ttu-id="5ff02-166">-TemplateParameterFile</span><span class="sxs-lookup"><span data-stu-id="5ff02-166">-TemplateParameterFile</span></span>
<span data-ttu-id="5ff02-167">具有範本參數的檔案。</span><span class="sxs-lookup"><span data-stu-id="5ff02-167">A file that has the template parameters.</span></span>

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

### <span data-ttu-id="5ff02-168">-TemplateParameterObject</span><span class="sxs-lookup"><span data-stu-id="5ff02-168">-TemplateParameterObject</span></span>
<span data-ttu-id="5ff02-169">代表參數的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="5ff02-169">A hash table which represents the parameters.</span></span>

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

### <span data-ttu-id="5ff02-170">-TemplateParameterUri</span><span class="sxs-lookup"><span data-stu-id="5ff02-170">-TemplateParameterUri</span></span>
<span data-ttu-id="5ff02-171">範本參數檔的 Uri。</span><span class="sxs-lookup"><span data-stu-id="5ff02-171">Uri to the template parameter file.</span></span>

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

### <span data-ttu-id="5ff02-172">-TemplateUri</span><span class="sxs-lookup"><span data-stu-id="5ff02-172">-TemplateUri</span></span>
<span data-ttu-id="5ff02-173">範本檔案的 Uri。</span><span class="sxs-lookup"><span data-stu-id="5ff02-173">Uri to the template file.</span></span>

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

### <span data-ttu-id="5ff02-174">-WhatIfExcludeChangeType</span><span class="sxs-lookup"><span data-stu-id="5ff02-174">-WhatIfExcludeChangeType</span></span>
<span data-ttu-id="5ff02-175">要從 What-If 結果中排除的逗號分隔資源變更類型。</span><span class="sxs-lookup"><span data-stu-id="5ff02-175">Comma-separated resource change types to be excluded from What-If results.</span></span> <span data-ttu-id="5ff02-176">在設定了-WhatIf 或-Confirm 切換時適用。</span><span class="sxs-lookup"><span data-stu-id="5ff02-176">Applicable when the -WhatIf or -Confirm switch is set.</span></span>

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

### <span data-ttu-id="5ff02-177">-WhatIfResultFormat</span><span class="sxs-lookup"><span data-stu-id="5ff02-177">-WhatIfResultFormat</span></span>
<span data-ttu-id="5ff02-178">What-If 的結果格式。</span><span class="sxs-lookup"><span data-stu-id="5ff02-178">The What-If result format.</span></span> <span data-ttu-id="5ff02-179">在設定了-WhatIf 或-Confirm 切換時適用。</span><span class="sxs-lookup"><span data-stu-id="5ff02-179">Applicable when the -WhatIf or -Confirm switch is set.</span></span>

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

### <span data-ttu-id="5ff02-180">-確認</span><span class="sxs-lookup"><span data-stu-id="5ff02-180">-Confirm</span></span>
<span data-ttu-id="5ff02-181">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="5ff02-181">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5ff02-182">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5ff02-182">-WhatIf</span></span>
<span data-ttu-id="5ff02-183">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="5ff02-183">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5ff02-184">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="5ff02-184">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5ff02-185">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5ff02-185">CommonParameters</span></span>
<span data-ttu-id="5ff02-186">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="5ff02-186">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5ff02-187">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="5ff02-187">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5ff02-188">輸入</span><span class="sxs-lookup"><span data-stu-id="5ff02-188">INPUTS</span></span>

### <span data-ttu-id="5ff02-189">[System.object] 集合. Hashtable</span><span class="sxs-lookup"><span data-stu-id="5ff02-189">System.Collections.Hashtable</span></span>

### <span data-ttu-id="5ff02-190">System.object</span><span class="sxs-lookup"><span data-stu-id="5ff02-190">System.String</span></span>

## <span data-ttu-id="5ff02-191">輸出</span><span class="sxs-lookup"><span data-stu-id="5ff02-191">OUTPUTS</span></span>

### <span data-ttu-id="5ff02-192">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span><span class="sxs-lookup"><span data-stu-id="5ff02-192">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="5ff02-193">筆記</span><span class="sxs-lookup"><span data-stu-id="5ff02-193">NOTES</span></span>

## <span data-ttu-id="5ff02-194">相關連結</span><span class="sxs-lookup"><span data-stu-id="5ff02-194">RELATED LINKS</span></span>
