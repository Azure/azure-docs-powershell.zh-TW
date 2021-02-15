---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-aztenantdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzTenantDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzTenantDeployment.md
ms.openlocfilehash: d2a54022768bd3751ed18713fdc123ef2ef9cbf1
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100142591"
---
# <span data-ttu-id="3bd8d-101">New-AzTenantDeployment</span><span class="sxs-lookup"><span data-stu-id="3bd8d-101">New-AzTenantDeployment</span></span>

## <span data-ttu-id="3bd8d-102">摘要</span><span class="sxs-lookup"><span data-stu-id="3bd8d-102">SYNOPSIS</span></span>
<span data-ttu-id="3bd8d-103">在租使用者範圍建立部署</span><span class="sxs-lookup"><span data-stu-id="3bd8d-103">Create a deployment at tenant scope</span></span>

## <span data-ttu-id="3bd8d-104">句法</span><span class="sxs-lookup"><span data-stu-id="3bd8d-104">SYNTAX</span></span>

### <span data-ttu-id="3bd8d-105">ByTemplateFileWithNoParameters (預設) </span><span class="sxs-lookup"><span data-stu-id="3bd8d-105">ByTemplateFileWithNoParameters (Default)</span></span>
```
New-AzTenantDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-AsJob]
 [-QueryString <String>] -TemplateFile <String> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3bd8d-106">ByTemplateObjectAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="3bd8d-106">ByTemplateObjectAndParameterObject</span></span>
```
New-AzTenantDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-AsJob]
 [-QueryString <String>] -TemplateParameterObject <Hashtable> -TemplateObject <Hashtable>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3bd8d-107">ByTemplateFileAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="3bd8d-107">ByTemplateFileAndParameterObject</span></span>
```
New-AzTenantDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-AsJob]
 [-QueryString <String>] -TemplateParameterObject <Hashtable> -TemplateFile <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3bd8d-108">ByTemplateUriAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="3bd8d-108">ByTemplateUriAndParameterObject</span></span>
```
New-AzTenantDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-AsJob]
 [-QueryString <String>] -TemplateParameterObject <Hashtable> -TemplateUri <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3bd8d-109">ByTemplateObjectAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="3bd8d-109">ByTemplateObjectAndParameterFile</span></span>
```
New-AzTenantDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-AsJob]
 [-QueryString <String>] -TemplateParameterFile <String> -TemplateObject <Hashtable>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3bd8d-110">ByTemplateFileAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="3bd8d-110">ByTemplateFileAndParameterFile</span></span>
```
New-AzTenantDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-AsJob]
 [-QueryString <String>] -TemplateParameterFile <String> -TemplateFile <String> [-SkipTemplateParameterPrompt]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3bd8d-111">ByTemplateUriAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="3bd8d-111">ByTemplateUriAndParameterFile</span></span>
```
New-AzTenantDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-AsJob]
 [-QueryString <String>] -TemplateParameterFile <String> -TemplateUri <String> [-SkipTemplateParameterPrompt]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3bd8d-112">ByTemplateSpecResourceIdAndParams</span><span class="sxs-lookup"><span data-stu-id="3bd8d-112">ByTemplateSpecResourceIdAndParams</span></span>
```
New-AzTenantDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-AsJob]
 [-QueryString <String>] -TemplateParameterFile <String> -TemplateSpecId <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3bd8d-113">ByTemplateObjectAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="3bd8d-113">ByTemplateObjectAndParameterUri</span></span>
```
New-AzTenantDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-AsJob]
 [-QueryString <String>] -TemplateParameterUri <String> -TemplateObject <Hashtable>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3bd8d-114">ByTemplateFileAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="3bd8d-114">ByTemplateFileAndParameterUri</span></span>
```
New-AzTenantDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-AsJob]
 [-QueryString <String>] -TemplateParameterUri <String> -TemplateFile <String> [-SkipTemplateParameterPrompt]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3bd8d-115">ByTemplateUriAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="3bd8d-115">ByTemplateUriAndParameterUri</span></span>
```
New-AzTenantDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-AsJob]
 [-QueryString <String>] -TemplateParameterUri <String> -TemplateUri <String> [-SkipTemplateParameterPrompt]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3bd8d-116">ByTemplateSpecResourceIdAndParamsUri</span><span class="sxs-lookup"><span data-stu-id="3bd8d-116">ByTemplateSpecResourceIdAndParamsUri</span></span>
```
New-AzTenantDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-AsJob]
 [-QueryString <String>] -TemplateParameterUri <String> -TemplateSpecId <String> [-SkipTemplateParameterPrompt]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3bd8d-117">ByTemplateObjectWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="3bd8d-117">ByTemplateObjectWithNoParameters</span></span>
```
New-AzTenantDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-AsJob]
 [-QueryString <String>] -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3bd8d-118">ByTemplateUriWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="3bd8d-118">ByTemplateUriWithNoParameters</span></span>
```
New-AzTenantDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-AsJob]
 [-QueryString <String>] -TemplateUri <String> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3bd8d-119">ByTemplateSpecResourceId</span><span class="sxs-lookup"><span data-stu-id="3bd8d-119">ByTemplateSpecResourceId</span></span>
```
New-AzTenantDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-AsJob]
 [-QueryString <String>] -TemplateSpecId <String> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3bd8d-120">說明</span><span class="sxs-lookup"><span data-stu-id="3bd8d-120">DESCRIPTION</span></span>
<span data-ttu-id="3bd8d-121">**新的-AzTenantDeployment** Cmdlet 會在目前的租使用者範圍內新增部署。</span><span class="sxs-lookup"><span data-stu-id="3bd8d-121">The **New-AzTenantDeployment** cmdlet adds a deployment at the current tenant scope.</span></span>

<span data-ttu-id="3bd8d-122">若要在租使用者範圍中新增部署，請指定位置和範本。</span><span class="sxs-lookup"><span data-stu-id="3bd8d-122">To add a deployment at tenant scope, specify the location and a template.</span></span>
<span data-ttu-id="3bd8d-123">位置會告知 Azure 資源管理員要儲存部署資料的位置。</span><span class="sxs-lookup"><span data-stu-id="3bd8d-123">The location tells Azure Resource Manager where to store the deployment data.</span></span> <span data-ttu-id="3bd8d-124">範本是一個 JSON 字串，其中包含要部署的個別資源。</span><span class="sxs-lookup"><span data-stu-id="3bd8d-124">The template is a JSON string that contains individual resources to be deployed.</span></span>
<span data-ttu-id="3bd8d-125">範本包含必要資源的參數預留位置，以及可設定的屬性值，例如名稱和大小。</span><span class="sxs-lookup"><span data-stu-id="3bd8d-125">The template includes parameter placeholders for required resources and configurable property values, such as names and sizes.</span></span>

<span data-ttu-id="3bd8d-126">若要在部署中使用自訂範本，請指定 *TemplateFile* 參數或 *TemplateUri* 參數。</span><span class="sxs-lookup"><span data-stu-id="3bd8d-126">To use a custom template for the deployment, specify the *TemplateFile* parameter or *TemplateUri* parameter.</span></span>
<span data-ttu-id="3bd8d-127">每個範本都有可設定屬性的參數。</span><span class="sxs-lookup"><span data-stu-id="3bd8d-127">Each template has parameters for configurable properties.</span></span>
<span data-ttu-id="3bd8d-128">若要指定範本參數的值，請指定 *TemplateParameterFile* 參數或 *TemplateParameterObject* 參數。</span><span class="sxs-lookup"><span data-stu-id="3bd8d-128">To specify values for the template parameters, specify the *TemplateParameterFile* parameter or the *TemplateParameterObject* parameter.</span></span>
<span data-ttu-id="3bd8d-129">或者，您也可以使用在指定範本時動態新增到命令中的範本參數。</span><span class="sxs-lookup"><span data-stu-id="3bd8d-129">Alternatively, you can use the template parameters that are dynamically added to the command when you specify a template.</span></span>
<span data-ttu-id="3bd8d-130">若要使用動態參數，請在命令提示字元輸入，或輸入減號 ( ) 來指示參數，然後使用 Tab 鍵來迴圈顯示可用的參數。</span><span class="sxs-lookup"><span data-stu-id="3bd8d-130">To use dynamic parameters, type them at the command prompt, or type a minus sign (-) to indicate a parameter and use the Tab key to cycle through available parameters.</span></span>
<span data-ttu-id="3bd8d-131">您在命令提示字元中輸入的範本參數值會優先于範本參數物件或檔案中的值。</span><span class="sxs-lookup"><span data-stu-id="3bd8d-131">Template parameter values that you enter at the command prompt take precedence over values in a template parameter object or file.</span></span>

<span data-ttu-id="3bd8d-132">若要將資源新增至資源群組，請使用 **New-AzResourceGroupDeployment** ，這會在資源群組建立部署。</span><span class="sxs-lookup"><span data-stu-id="3bd8d-132">To add resources to a resource group, use the **New-AzResourceGroupDeployment** which creates a deployment at a resource group.</span></span>
<span data-ttu-id="3bd8d-133">若要將資源新增至訂閱，請使用 **新的-AzSubscriptionDeployment** ，這會在訂閱範圍中建立部署，以部署訂閱層級資源。</span><span class="sxs-lookup"><span data-stu-id="3bd8d-133">To add resources to a subscription, use the **New-AzSubscriptionDeployment** which creates a deployment at subscription scope, which deploys subscription level resources.</span></span>
<span data-ttu-id="3bd8d-134">若要在管理群組新增資源，請使用 [ **New-AzManagementGroupDeployment** ]，在管理群組建立部署。</span><span class="sxs-lookup"><span data-stu-id="3bd8d-134">To add resources at a management group, use the **New-AzManagementGroupDeployment** which creates a deployment at a management group.</span></span>

## <span data-ttu-id="3bd8d-135">示例</span><span class="sxs-lookup"><span data-stu-id="3bd8d-135">EXAMPLES</span></span>

### <span data-ttu-id="3bd8d-136">範例1：使用自訂範本和參數檔案建立部署</span><span class="sxs-lookup"><span data-stu-id="3bd8d-136">Example 1: Use a custom template and parameter file to create a deployment</span></span>
```
PS C:\> New-AzTenantDeployment -Location "West US" -TemplateFile "D:\Azure\Templates\OrgSetup.json" -TemplateParameterFile "D:\Azure\Templates\OrgParms.json" -Tag @{"key1"="value1"; "key2"="value2";}
```

<span data-ttu-id="3bd8d-137">這個命令會使用自訂的範本與磁片上的範本檔案（含已定義的 tags 參數），在目前租使用者範圍內建立新的部署。</span><span class="sxs-lookup"><span data-stu-id="3bd8d-137">This command creates a new deployment at the current tenant scope by using a custom template and a template file on disk, with defined tags parameter.</span></span>
<span data-ttu-id="3bd8d-138">此命令會使用 *TemplateFile* 參數來指定範本和 *TemplateParameterFile* 參數，以指定包含參數和參數值的檔案。</span><span class="sxs-lookup"><span data-stu-id="3bd8d-138">The command uses the *TemplateFile* parameter to specify the template and the *TemplateParameterFile* parameter to specify a file that contains parameters and parameter values.</span></span>

### <span data-ttu-id="3bd8d-139">範例2：使用自訂範本物件與參數檔案建立部署</span><span class="sxs-lookup"><span data-stu-id="3bd8d-139">Example 2: Use a custom template object and parameter file to create a deployment</span></span>
```
PS C:\> $TemplateFileText = [System.IO.File]::ReadAllText("D:\Azure\Templates\OrgSetup.json")
PS C:\> $TemplateObject = ConvertFrom-Json $TemplateFileText -AsHashtable
PS C:\> New-AzTenantDeployment -Location "West US" -TemplateObject $TemplateObject -TemplateParameterFile "D:\Azure\Templates\OrgParams.json"
```

<span data-ttu-id="3bd8d-140">這個命令會在目前的租使用者中建立新的部署，方法是使用自訂範本，以及磁片上已轉換成記憶體中的 hashtable 的範本檔案。</span><span class="sxs-lookup"><span data-stu-id="3bd8d-140">This command creates a new deployment at the current tenant by using a custom template and a template file on disk that has been converted to an in-memory hashtable.</span></span>
<span data-ttu-id="3bd8d-141">前兩個命令會讀取磁片上範本檔案的文字，並將它轉換成記憶體中的 hashtable。</span><span class="sxs-lookup"><span data-stu-id="3bd8d-141">The first two commands read the text for the template file on disk and convert it to an in-memory hashtable.</span></span>
<span data-ttu-id="3bd8d-142">最後一個命令使用 *TemplateObject* 參數來指定此 Hashtable 和 *TemplateParameterFile* 參數，以指定包含參數和參數值的檔案。</span><span class="sxs-lookup"><span data-stu-id="3bd8d-142">The last command uses the *TemplateObject* parameter to specify this hashtable and the *TemplateParameterFile* parameter to specify a file that contains parameters and parameter values.</span></span>

## <span data-ttu-id="3bd8d-143">參數</span><span class="sxs-lookup"><span data-stu-id="3bd8d-143">PARAMETERS</span></span>

### <span data-ttu-id="3bd8d-144">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3bd8d-144">-AsJob</span></span>
<span data-ttu-id="3bd8d-145">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="3bd8d-145">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="3bd8d-146">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3bd8d-146">-DefaultProfile</span></span>
<span data-ttu-id="3bd8d-147">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="3bd8d-147">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3bd8d-148">-DeploymentDebugLogLevel</span><span class="sxs-lookup"><span data-stu-id="3bd8d-148">-DeploymentDebugLogLevel</span></span>
<span data-ttu-id="3bd8d-149">部署調試記錄層級。</span><span class="sxs-lookup"><span data-stu-id="3bd8d-149">The deployment debug log level.</span></span>

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

### <span data-ttu-id="3bd8d-150">-位置</span><span class="sxs-lookup"><span data-stu-id="3bd8d-150">-Location</span></span>
<span data-ttu-id="3bd8d-151">儲存部署資料的位置。</span><span class="sxs-lookup"><span data-stu-id="3bd8d-151">The location to store deployment data.</span></span>

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

### <span data-ttu-id="3bd8d-152">-名稱</span><span class="sxs-lookup"><span data-stu-id="3bd8d-152">-Name</span></span>
<span data-ttu-id="3bd8d-153">將要建立之部署的名稱。</span><span class="sxs-lookup"><span data-stu-id="3bd8d-153">The name of the deployment it's going to create.</span></span> <span data-ttu-id="3bd8d-154">如果未指定，則預設為提供範本檔時的範本檔案名;預設為提供範本物件的目前時間（例如 "20131223140835"）。</span><span class="sxs-lookup"><span data-stu-id="3bd8d-154">If not specified, defaults to the template file name when a template file is provided; defaults to the current time when a template object is provided, e.g. "20131223140835".</span></span>

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

### <span data-ttu-id="3bd8d-155">-預先</span><span class="sxs-lookup"><span data-stu-id="3bd8d-155">-Pre</span></span>
<span data-ttu-id="3bd8d-156">設定時，表示 Cmdlet 應該使用預發行 API 版本，以便自動判斷要使用的版本。</span><span class="sxs-lookup"><span data-stu-id="3bd8d-156">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="3bd8d-157">-QueryString</span><span class="sxs-lookup"><span data-stu-id="3bd8d-157">-QueryString</span></span>
<span data-ttu-id="3bd8d-158">查詢字串 (例如，要與 TemplateUri 參數搭配使用的 SAS 權杖) 。</span><span class="sxs-lookup"><span data-stu-id="3bd8d-158">The query string (for example, a SAS token) to be used with the TemplateUri parameter.</span></span> <span data-ttu-id="3bd8d-159">會在連結範本時使用</span><span class="sxs-lookup"><span data-stu-id="3bd8d-159">Would be used in case of linked templates</span></span>

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

### <span data-ttu-id="3bd8d-160">-SkipTemplateParameterPrompt</span><span class="sxs-lookup"><span data-stu-id="3bd8d-160">-SkipTemplateParameterPrompt</span></span>
<span data-ttu-id="3bd8d-161">會跳過 PowerShell 動態參數處理，檢查提供的範本參數是否包含範本所使用的所有必要參數。</span><span class="sxs-lookup"><span data-stu-id="3bd8d-161">Skips the PowerShell dynamic parameter processing that checks if the provided template parameter contains all necessary parameters used by the template.</span></span>
<span data-ttu-id="3bd8d-162">這項檢查會提示使用者提供缺少參數的值，但提供-SkipTemplateParameterPrompt 將會在範本中發現未系結的參數時，立即忽略此提示和錯誤。</span><span class="sxs-lookup"><span data-stu-id="3bd8d-162">This check would prompt the user to provide a value for the missing parameters, but providing the -SkipTemplateParameterPrompt will ignore this prompt and error out immediately if a parameter was found not to be bound in the template.</span></span>
<span data-ttu-id="3bd8d-163">在非互動式腳本中，您可以提供 SkipTemplateParameterPrompt，以在不符合所有必要參數的情況下，提供較佳的錯誤訊息。</span><span class="sxs-lookup"><span data-stu-id="3bd8d-163">For non-interactive scripts, -SkipTemplateParameterPrompt can be provided to provide a better error message in the case where not all required parameters are satisfied.</span></span>

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

### <span data-ttu-id="3bd8d-164">-Tag</span><span class="sxs-lookup"><span data-stu-id="3bd8d-164">-Tag</span></span>
<span data-ttu-id="3bd8d-165">要放在部署上的標記。</span><span class="sxs-lookup"><span data-stu-id="3bd8d-165">The tags to put on the deployment.</span></span>

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

### <span data-ttu-id="3bd8d-166">-TemplateFile</span><span class="sxs-lookup"><span data-stu-id="3bd8d-166">-TemplateFile</span></span>
<span data-ttu-id="3bd8d-167">範本檔案的本機路徑。</span><span class="sxs-lookup"><span data-stu-id="3bd8d-167">Local path to the template file.</span></span>

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

### <span data-ttu-id="3bd8d-168">-TemplateObject</span><span class="sxs-lookup"><span data-stu-id="3bd8d-168">-TemplateObject</span></span>
<span data-ttu-id="3bd8d-169">代表範本的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="3bd8d-169">A hash table which represents the template.</span></span>

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

### <span data-ttu-id="3bd8d-170">-TemplateParameterFile</span><span class="sxs-lookup"><span data-stu-id="3bd8d-170">-TemplateParameterFile</span></span>
<span data-ttu-id="3bd8d-171">具有範本參數的檔案。</span><span class="sxs-lookup"><span data-stu-id="3bd8d-171">A file that has the template parameters.</span></span>

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

### <span data-ttu-id="3bd8d-172">-TemplateParameterObject</span><span class="sxs-lookup"><span data-stu-id="3bd8d-172">-TemplateParameterObject</span></span>
<span data-ttu-id="3bd8d-173">代表參數的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="3bd8d-173">A hash table which represents the parameters.</span></span>

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

### <span data-ttu-id="3bd8d-174">-TemplateParameterUri</span><span class="sxs-lookup"><span data-stu-id="3bd8d-174">-TemplateParameterUri</span></span>
<span data-ttu-id="3bd8d-175">範本參數檔的 Uri。</span><span class="sxs-lookup"><span data-stu-id="3bd8d-175">Uri to the template parameter file.</span></span>

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

### <span data-ttu-id="3bd8d-176">-TemplateSpecId</span><span class="sxs-lookup"><span data-stu-id="3bd8d-176">-TemplateSpecId</span></span>
<span data-ttu-id="3bd8d-177">要部署之 templateSpec 的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="3bd8d-177">Resource ID of the templateSpec to be deployed.</span></span>

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

### <span data-ttu-id="3bd8d-178">-TemplateUri</span><span class="sxs-lookup"><span data-stu-id="3bd8d-178">-TemplateUri</span></span>
<span data-ttu-id="3bd8d-179">範本檔案的 Uri。</span><span class="sxs-lookup"><span data-stu-id="3bd8d-179">Uri to the template file.</span></span>

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

### <span data-ttu-id="3bd8d-180">-WhatIfExcludeChangeType</span><span class="sxs-lookup"><span data-stu-id="3bd8d-180">-WhatIfExcludeChangeType</span></span>
<span data-ttu-id="3bd8d-181">要從 What-If 結果中排除的逗號分隔資源變更類型。</span><span class="sxs-lookup"><span data-stu-id="3bd8d-181">Comma-separated resource change types to be excluded from What-If results.</span></span> <span data-ttu-id="3bd8d-182">在設定了-WhatIf 或-Confirm 切換時適用。</span><span class="sxs-lookup"><span data-stu-id="3bd8d-182">Applicable when the -WhatIf or -Confirm switch is set.</span></span>

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

### <span data-ttu-id="3bd8d-183">-WhatIfResultFormat</span><span class="sxs-lookup"><span data-stu-id="3bd8d-183">-WhatIfResultFormat</span></span>
<span data-ttu-id="3bd8d-184">What-If 的結果格式。</span><span class="sxs-lookup"><span data-stu-id="3bd8d-184">The What-If result format.</span></span> <span data-ttu-id="3bd8d-185">在設定了-WhatIf 或-Confirm 切換時適用。</span><span class="sxs-lookup"><span data-stu-id="3bd8d-185">Applicable when the -WhatIf or -Confirm switch is set.</span></span>

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

### <span data-ttu-id="3bd8d-186">-確認</span><span class="sxs-lookup"><span data-stu-id="3bd8d-186">-Confirm</span></span>
<span data-ttu-id="3bd8d-187">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="3bd8d-187">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3bd8d-188">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3bd8d-188">-WhatIf</span></span>
<span data-ttu-id="3bd8d-189">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="3bd8d-189">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3bd8d-190">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="3bd8d-190">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3bd8d-191">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3bd8d-191">CommonParameters</span></span>
<span data-ttu-id="3bd8d-192">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="3bd8d-192">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3bd8d-193">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="3bd8d-193">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3bd8d-194">輸入</span><span class="sxs-lookup"><span data-stu-id="3bd8d-194">INPUTS</span></span>

### <span data-ttu-id="3bd8d-195">[System.object] 集合. Hashtable</span><span class="sxs-lookup"><span data-stu-id="3bd8d-195">System.Collections.Hashtable</span></span>

### <span data-ttu-id="3bd8d-196">System.object</span><span class="sxs-lookup"><span data-stu-id="3bd8d-196">System.String</span></span>

## <span data-ttu-id="3bd8d-197">輸出</span><span class="sxs-lookup"><span data-stu-id="3bd8d-197">OUTPUTS</span></span>

### <span data-ttu-id="3bd8d-198">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span><span class="sxs-lookup"><span data-stu-id="3bd8d-198">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="3bd8d-199">筆記</span><span class="sxs-lookup"><span data-stu-id="3bd8d-199">NOTES</span></span>

## <span data-ttu-id="3bd8d-200">相關連結</span><span class="sxs-lookup"><span data-stu-id="3bd8d-200">RELATED LINKS</span></span>
