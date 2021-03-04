---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/powershell/module/az.resources/new-azmanagementgroupdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzManagementGroupDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzManagementGroupDeployment.md
ms.openlocfilehash: da2a2bc6d7c35f6d7f092123dce08496f491655b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101915234"
---
# <span data-ttu-id="1e530-101">New-AzManagementGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="1e530-101">New-AzManagementGroupDeployment</span></span>

## <span data-ttu-id="1e530-102">簡介</span><span class="sxs-lookup"><span data-stu-id="1e530-102">SYNOPSIS</span></span>
<span data-ttu-id="1e530-103">在管理群組建立部署</span><span class="sxs-lookup"><span data-stu-id="1e530-103">Create a deployment at a management group</span></span>

## <span data-ttu-id="1e530-104">語法</span><span class="sxs-lookup"><span data-stu-id="1e530-104">SYNTAX</span></span>

### <span data-ttu-id="1e530-105">ByTemplateFileWithNoParameters (預設) </span><span class="sxs-lookup"><span data-stu-id="1e530-105">ByTemplateFileWithNoParameters (Default)</span></span>
```
New-AzManagementGroupDeployment [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>]
 [-WhatIfExcludeChangeType <String[]>] [-AsJob] [-QueryString <String>] -TemplateFile <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="1e530-106">ByTemplateObjectAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="1e530-106">ByTemplateObjectAndParameterObject</span></span>
```
New-AzManagementGroupDeployment [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>]
 [-WhatIfExcludeChangeType <String[]>] [-AsJob] [-QueryString <String>] -TemplateParameterObject <Hashtable>
 -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1e530-107">ByTemplateFileAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="1e530-107">ByTemplateFileAndParameterObject</span></span>
```
New-AzManagementGroupDeployment [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>]
 [-WhatIfExcludeChangeType <String[]>] [-AsJob] [-QueryString <String>] -TemplateParameterObject <Hashtable>
 -TemplateFile <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1e530-108">ByTemplateUriAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="1e530-108">ByTemplateUriAndParameterObject</span></span>
```
New-AzManagementGroupDeployment [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>]
 [-WhatIfExcludeChangeType <String[]>] [-AsJob] [-QueryString <String>] -TemplateParameterObject <Hashtable>
 -TemplateUri <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1e530-109">ByTemplateSpecResourceIdAndParamsObject</span><span class="sxs-lookup"><span data-stu-id="1e530-109">ByTemplateSpecResourceIdAndParamsObject</span></span>
```
New-AzManagementGroupDeployment [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>]
 [-WhatIfExcludeChangeType <String[]>] [-AsJob] [-QueryString <String>] -TemplateParameterObject <Hashtable>
 -TemplateSpecId <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1e530-110">ByTemplateObjectAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="1e530-110">ByTemplateObjectAndParameterFile</span></span>
```
New-AzManagementGroupDeployment [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>]
 [-WhatIfExcludeChangeType <String[]>] [-AsJob] [-QueryString <String>] -TemplateParameterFile <String>
 -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1e530-111">ByTemplateFileAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="1e530-111">ByTemplateFileAndParameterFile</span></span>
```
New-AzManagementGroupDeployment [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>]
 [-WhatIfExcludeChangeType <String[]>] [-AsJob] [-QueryString <String>] -TemplateParameterFile <String>
 -TemplateFile <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1e530-112">ByTemplateUriAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="1e530-112">ByTemplateUriAndParameterFile</span></span>
```
New-AzManagementGroupDeployment [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>]
 [-WhatIfExcludeChangeType <String[]>] [-AsJob] [-QueryString <String>] -TemplateParameterFile <String>
 -TemplateUri <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1e530-113">ByTemplateSpecResourceIdAndParams</span><span class="sxs-lookup"><span data-stu-id="1e530-113">ByTemplateSpecResourceIdAndParams</span></span>
```
New-AzManagementGroupDeployment [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>]
 [-WhatIfExcludeChangeType <String[]>] [-AsJob] [-QueryString <String>] -TemplateParameterFile <String>
 -TemplateSpecId <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1e530-114">ByTemplateObjectAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="1e530-114">ByTemplateObjectAndParameterUri</span></span>
```
New-AzManagementGroupDeployment [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>]
 [-WhatIfExcludeChangeType <String[]>] [-AsJob] [-QueryString <String>] -TemplateParameterUri <String>
 -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1e530-115">ByTemplateFileAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="1e530-115">ByTemplateFileAndParameterUri</span></span>
```
New-AzManagementGroupDeployment [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>]
 [-WhatIfExcludeChangeType <String[]>] [-AsJob] [-QueryString <String>] -TemplateParameterUri <String>
 -TemplateFile <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1e530-116">ByTemplateUriAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="1e530-116">ByTemplateUriAndParameterUri</span></span>
```
New-AzManagementGroupDeployment [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>]
 [-WhatIfExcludeChangeType <String[]>] [-AsJob] [-QueryString <String>] -TemplateParameterUri <String>
 -TemplateUri <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1e530-117">ByTemplateSpecResourceIdAndParamsUri</span><span class="sxs-lookup"><span data-stu-id="1e530-117">ByTemplateSpecResourceIdAndParamsUri</span></span>
```
New-AzManagementGroupDeployment [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>]
 [-WhatIfExcludeChangeType <String[]>] [-AsJob] [-QueryString <String>] -TemplateParameterUri <String>
 -TemplateSpecId <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1e530-118">ByTemplateObjectWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="1e530-118">ByTemplateObjectWithNoParameters</span></span>
```
New-AzManagementGroupDeployment [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>]
 [-WhatIfExcludeChangeType <String[]>] [-AsJob] [-QueryString <String>] -TemplateObject <Hashtable>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="1e530-119">ByTemplateUriWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="1e530-119">ByTemplateUriWithNoParameters</span></span>
```
New-AzManagementGroupDeployment [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>]
 [-WhatIfExcludeChangeType <String[]>] [-AsJob] [-QueryString <String>] -TemplateUri <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="1e530-120">ByTemplateSpecResourceId</span><span class="sxs-lookup"><span data-stu-id="1e530-120">ByTemplateSpecResourceId</span></span>
```
New-AzManagementGroupDeployment [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>]
 [-WhatIfExcludeChangeType <String[]>] [-AsJob] [-QueryString <String>] -TemplateSpecId <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="1e530-121">描述</span><span class="sxs-lookup"><span data-stu-id="1e530-121">DESCRIPTION</span></span>
<span data-ttu-id="1e530-122">**New-AzManagementGroupDeployment** Cmdlet 會新增管理群組的部署。</span><span class="sxs-lookup"><span data-stu-id="1e530-122">The **New-AzManagementGroupDeployment** cmdlet adds a deployment at a management group.</span></span>

<span data-ttu-id="1e530-123">若要在管理群組新增部署，請指定管理群組、位置和範本。</span><span class="sxs-lookup"><span data-stu-id="1e530-123">To add a deployment at a management group, specify the management group, location and a template.</span></span>
<span data-ttu-id="1e530-124">位置會告知 Azure Resource Manager 要儲存部署資料的位置。</span><span class="sxs-lookup"><span data-stu-id="1e530-124">The location tells Azure Resource Manager where to store the deployment data.</span></span> <span data-ttu-id="1e530-125">範本是 JSON 字串，其中包含要部署的個別資源。</span><span class="sxs-lookup"><span data-stu-id="1e530-125">The template is a JSON string that contains individual resources to be deployed.</span></span>
<span data-ttu-id="1e530-126">範本包含所需資源的參數預留位置，以及可設定屬性值 ，例如名稱和大小。</span><span class="sxs-lookup"><span data-stu-id="1e530-126">The template includes parameter placeholders for required resources and configurable property values, such as names and sizes.</span></span>

<span data-ttu-id="1e530-127">若要使用自訂範本進行部署，請指定 *TemplateFile* 參數或 *TemplateUri* 參數。</span><span class="sxs-lookup"><span data-stu-id="1e530-127">To use a custom template for the deployment, specify the *TemplateFile* parameter or *TemplateUri* parameter.</span></span>
<span data-ttu-id="1e530-128">每個範本都有可設定屬性的參數。</span><span class="sxs-lookup"><span data-stu-id="1e530-128">Each template has parameters for configurable properties.</span></span>
<span data-ttu-id="1e530-129">若要指定範本參數的值，請指定 *TemplateParameterFile* 參數或 *TemplateParameterObject* 參數。</span><span class="sxs-lookup"><span data-stu-id="1e530-129">To specify values for the template parameters, specify the *TemplateParameterFile* parameter or the *TemplateParameterObject* parameter.</span></span>
<span data-ttu-id="1e530-130">或者，您也可以使用指定範本時動態新加入命令的範本參數。</span><span class="sxs-lookup"><span data-stu-id="1e530-130">Alternatively, you can use the template parameters that are dynamically added to the command when you specify a template.</span></span>
<span data-ttu-id="1e530-131">若要使用動態參數，請于命令提示文字輸入參數，或輸入減號 (-) 來表示參數，並使用 Tab 鍵迴圈流覽可用的參數。</span><span class="sxs-lookup"><span data-stu-id="1e530-131">To use dynamic parameters, type them at the command prompt, or type a minus sign (-) to indicate a parameter and use the Tab key to cycle through available parameters.</span></span>
<span data-ttu-id="1e530-132">在命令提示提示輸入的範本參數值優先于範本參數物件或檔案中的值。</span><span class="sxs-lookup"><span data-stu-id="1e530-132">Template parameter values that you enter at the command prompt take precedence over values in a template parameter object or file.</span></span>

<span data-ttu-id="1e530-133">若要新增資源至資源群組，請使用 **New-AzResourceGroupDeployment，** 在資源群組中建立部署。</span><span class="sxs-lookup"><span data-stu-id="1e530-133">To add resources to a resource group, use the **New-AzResourceGroupDeployment** which creates a deployment at a resource group.</span></span>
<span data-ttu-id="1e530-134">若要新增資源至訂閱，請使用 **New-AzSubscriptionDeployment，** 在訂閱範圍中建立部署，以部署訂閱層級資源。</span><span class="sxs-lookup"><span data-stu-id="1e530-134">To add resources to a subscription, use the **New-AzSubscriptionDeployment** which creates a deployment at subscription scope, which deploys subscription level resources.</span></span>
<span data-ttu-id="1e530-135">若要在租使用者範圍中新增資源，請使用 **New-AzTenantDeployment，** 在租使用者範圍中建立部署。</span><span class="sxs-lookup"><span data-stu-id="1e530-135">To add resources at tenant scope, use the **New-AzTenantDeployment** which creates a deployment at tenant scope.</span></span>

## <span data-ttu-id="1e530-136">例子</span><span class="sxs-lookup"><span data-stu-id="1e530-136">EXAMPLES</span></span>

### <span data-ttu-id="1e530-137">範例 1：使用自訂範本和參數檔案建立部署</span><span class="sxs-lookup"><span data-stu-id="1e530-137">Example 1: Use a custom template and parameter file to create a deployment</span></span>
```
PS C:\> New-AzManagementGroupDeployment -ManagementGroupId "myMG" -Location "West US" -TemplateFile "D:\Azure\Templates\OrgSetup.json" -TemplateParameterFile "D:\Azure\Templates\OrgParms.json" -Tag @{"key1"="value1"; "key2"="value2";}
```

<span data-ttu-id="1e530-138">此命令會使用自訂範本和磁片上的範本檔案，以及已定義的標籤參數，在管理群組 「myMG」建立新部署。</span><span class="sxs-lookup"><span data-stu-id="1e530-138">This command creates a new deployment at the management group "myMG" by using a custom template and a template file on disk, with defined tags parameter.</span></span>
<span data-ttu-id="1e530-139">該命令使用 *TemplateFile* 參數來指定範本，而 *TemplateParameterFile* 參數則指定包含參數和參數值的檔案。</span><span class="sxs-lookup"><span data-stu-id="1e530-139">The command uses the *TemplateFile* parameter to specify the template and the *TemplateParameterFile* parameter to specify a file that contains parameters and parameter values.</span></span>

### <span data-ttu-id="1e530-140">範例 2：使用 uri 和 SAS 權杖部署儲存在非公用儲存帳戶中的範本</span><span class="sxs-lookup"><span data-stu-id="1e530-140">Example 2: Deploy a template stored in a non public storage account using a uri and SAS token</span></span>
```
PS C:\> New-AzManagementGroupDeployment -ManagementGroupId "myMG" -Location "West US" -TemplateUri "https://example.com/example.json" -QueryString "foo"
```

<span data-ttu-id="1e530-141">此命令會使用 TemplateUri 中的範本建立新部署，範本不是公用的，而且需要權杖參數來存取，這會使用 QueryString 參數提供。</span><span class="sxs-lookup"><span data-stu-id="1e530-141">This command creates a new deployment using the template in TemplateUri which is not public and requires a token parameter to access which would be provided using the QueryString parameter.</span></span>
<span data-ttu-id="1e530-142">執行此命令會使用 URL 有效地存取範本 https://example.com/example.json?foo 。</span><span class="sxs-lookup"><span data-stu-id="1e530-142">Running this command effectively accesses the template using the url https://example.com/example.json?foo.</span></span>
<span data-ttu-id="1e530-143">如果您想要在儲存帳戶中使用範本，請使用此功能，方法為提供 SAS 權杖做為 QueryString</span><span class="sxs-lookup"><span data-stu-id="1e530-143">This can be used if you want to use a template in a storage account by providing the SAS token as the QueryString</span></span>

### <span data-ttu-id="1e530-144">範例 3：使用自訂範本物件和參數檔案建立部署</span><span class="sxs-lookup"><span data-stu-id="1e530-144">Example 3: Use a custom template object and parameter file to create a deployment</span></span>
```
PS C:\> $TemplateFileText = [System.IO.File]::ReadAllText("D:\Azure\Templates\OrgSetup.json")
PS C:\> $TemplateObject = ConvertFrom-Json $TemplateFileText -AsHashtable
PS C:\> New-AzManagementGroupDeployment -ManagementGroupId "myMG" -Location "West US" -TemplateObject $TemplateObject -TemplateParameterFile "D:\Azure\Templates\OrgParams.json"
```

<span data-ttu-id="1e530-145">此命令會使用自訂範本和磁片上已轉換成記憶體雜湊表的範本檔案，在管理群組 「myMG」建立新部署。</span><span class="sxs-lookup"><span data-stu-id="1e530-145">This command creates a new deployment at the management group "myMG" by using a custom template and a template file on disk that has been converted to an in-memory hashtable.</span></span>
<span data-ttu-id="1e530-146">前兩個命令會讀取磁片上範本檔案的文字，並將它轉換成記憶體內雜湊表。</span><span class="sxs-lookup"><span data-stu-id="1e530-146">The first two commands read the text for the template file on disk and convert it to an in-memory hashtable.</span></span>
<span data-ttu-id="1e530-147">最後一個命令使用 *TemplateObject* 參數來指定此雜湊表，而 *TemplateParameterFile* 參數則指定包含參數和參數值的檔案。</span><span class="sxs-lookup"><span data-stu-id="1e530-147">The last command uses the *TemplateObject* parameter to specify this hashtable and the *TemplateParameterFile* parameter to specify a file that contains parameters and parameter values.</span></span>

## <span data-ttu-id="1e530-148">參數</span><span class="sxs-lookup"><span data-stu-id="1e530-148">PARAMETERS</span></span>

### <span data-ttu-id="1e530-149">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1e530-149">-AsJob</span></span>
<span data-ttu-id="1e530-150">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="1e530-150">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="1e530-151">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1e530-151">-DefaultProfile</span></span>
<span data-ttu-id="1e530-152">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="1e530-152">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1e530-153">-DeploymentDelogLogLevel</span><span class="sxs-lookup"><span data-stu-id="1e530-153">-DeploymentDebugLogLevel</span></span>
<span data-ttu-id="1e530-154">部署 Debug 記錄層級。</span><span class="sxs-lookup"><span data-stu-id="1e530-154">The deployment debug log level.</span></span>

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

### <span data-ttu-id="1e530-155">-位置</span><span class="sxs-lookup"><span data-stu-id="1e530-155">-Location</span></span>
<span data-ttu-id="1e530-156">儲存部署資料的位置。</span><span class="sxs-lookup"><span data-stu-id="1e530-156">The location to store deployment data.</span></span>

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

### <span data-ttu-id="1e530-157">-ManagementGroupId</span><span class="sxs-lookup"><span data-stu-id="1e530-157">-ManagementGroupId</span></span>
<span data-ttu-id="1e530-158">管理群組識別碼。</span><span class="sxs-lookup"><span data-stu-id="1e530-158">The management group ID.</span></span>

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

### <span data-ttu-id="1e530-159">-名稱</span><span class="sxs-lookup"><span data-stu-id="1e530-159">-Name</span></span>
<span data-ttu-id="1e530-160">要建立之部署的名稱。</span><span class="sxs-lookup"><span data-stu-id="1e530-160">The name of the deployment it's going to create.</span></span> <span data-ttu-id="1e530-161">如果未指定，則提供範本檔案時預設為範本檔案名;預設為提供範本物件的目前時間，例如"20131223140835"。</span><span class="sxs-lookup"><span data-stu-id="1e530-161">If not specified, defaults to the template file name when a template file is provided; defaults to the current time when a template object is provided, e.g. "20131223140835".</span></span>

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

### <span data-ttu-id="1e530-162">-Pre</span><span class="sxs-lookup"><span data-stu-id="1e530-162">-Pre</span></span>
<span data-ttu-id="1e530-163">設定之後，表示當系統自動決定要使用哪個版本時，Cmdlet 應該使用測試版 API 版本。</span><span class="sxs-lookup"><span data-stu-id="1e530-163">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="1e530-164">-QueryString</span><span class="sxs-lookup"><span data-stu-id="1e530-164">-QueryString</span></span>
<span data-ttu-id="1e530-165">查詢字串 (例如，一個 SAS 權杖) TemplateUri 參數一起使用。</span><span class="sxs-lookup"><span data-stu-id="1e530-165">The query string (for example, a SAS token) to be used with the TemplateUri parameter.</span></span> <span data-ttu-id="1e530-166">會用於連結範本的情況</span><span class="sxs-lookup"><span data-stu-id="1e530-166">Would be used in case of linked templates</span></span>

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

### <span data-ttu-id="1e530-167">-SkipTemplateParameterPrompt</span><span class="sxs-lookup"><span data-stu-id="1e530-167">-SkipTemplateParameterPrompt</span></span>
<span data-ttu-id="1e530-168">跳過 PowerShell 動態參數處理，檢查所提供的範本參數是否包含範本使用的所有必要參數。</span><span class="sxs-lookup"><span data-stu-id="1e530-168">Skips the PowerShell dynamic parameter processing that checks if the provided template parameter contains all necessary parameters used by the template.</span></span>
<span data-ttu-id="1e530-169">這項檢查會提示使用者提供遺失參數的值，但若發現參數未系在範本中，則提供 -SkipTemplateParameterPrompt 會忽略此提示並立即錯誤。</span><span class="sxs-lookup"><span data-stu-id="1e530-169">This check would prompt the user to provide a value for the missing parameters, but providing the -SkipTemplateParameterPrompt will ignore this prompt and error out immediately if a parameter was found not to be bound in the template.</span></span>
<span data-ttu-id="1e530-170">針對非互動式腳本，您可以提供 -SkipTemplateParameterPrompt，以在未滿足所有所需參數的情況下提供更佳的錯誤訊息。</span><span class="sxs-lookup"><span data-stu-id="1e530-170">For non-interactive scripts, -SkipTemplateParameterPrompt can be provided to provide a better error message in the case where not all required parameters are satisfied.</span></span>

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

### <span data-ttu-id="1e530-171">-標記</span><span class="sxs-lookup"><span data-stu-id="1e530-171">-Tag</span></span>
<span data-ttu-id="1e530-172">要放在部署的標記。</span><span class="sxs-lookup"><span data-stu-id="1e530-172">The tags to put on the deployment.</span></span>

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

### <span data-ttu-id="1e530-173">-TemplateFile</span><span class="sxs-lookup"><span data-stu-id="1e530-173">-TemplateFile</span></span>
<span data-ttu-id="1e530-174">範本檔案的當地路徑。</span><span class="sxs-lookup"><span data-stu-id="1e530-174">Local path to the template file.</span></span> <span data-ttu-id="1e530-175">支援的範本檔案類型：json 和 bicep。</span><span class="sxs-lookup"><span data-stu-id="1e530-175">Supported template file type: json and bicep.</span></span>

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

### <span data-ttu-id="1e530-176">-TemplateObject</span><span class="sxs-lookup"><span data-stu-id="1e530-176">-TemplateObject</span></span>
<span data-ttu-id="1e530-177">代表範本的雜湊表格。</span><span class="sxs-lookup"><span data-stu-id="1e530-177">A hash table which represents the template.</span></span>

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

### <span data-ttu-id="1e530-178">-TemplateParameterFile</span><span class="sxs-lookup"><span data-stu-id="1e530-178">-TemplateParameterFile</span></span>
<span data-ttu-id="1e530-179">具有範本參數的檔案。</span><span class="sxs-lookup"><span data-stu-id="1e530-179">A file that has the template parameters.</span></span>

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

### <span data-ttu-id="1e530-180">-TemplateParameterObject</span><span class="sxs-lookup"><span data-stu-id="1e530-180">-TemplateParameterObject</span></span>
<span data-ttu-id="1e530-181">代表參數的雜湊表格。</span><span class="sxs-lookup"><span data-stu-id="1e530-181">A hash table which represents the parameters.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: ByTemplateObjectAndParameterObject, ByTemplateFileAndParameterObject, ByTemplateUriAndParameterObject, ByTemplateSpecResourceIdAndParamsObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1e530-182">-TemplateParameterUri</span><span class="sxs-lookup"><span data-stu-id="1e530-182">-TemplateParameterUri</span></span>
<span data-ttu-id="1e530-183">Uri 到範本參數檔案。</span><span class="sxs-lookup"><span data-stu-id="1e530-183">Uri to the template parameter file.</span></span>

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

### <span data-ttu-id="1e530-184">-TemplateSpecId</span><span class="sxs-lookup"><span data-stu-id="1e530-184">-TemplateSpecId</span></span>
<span data-ttu-id="1e530-185">要部署的 templateSpec 資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="1e530-185">Resource ID of the templateSpec to be deployed.</span></span>

```yaml
Type: System.String
Parameter Sets: ByTemplateSpecResourceIdAndParamsObject, ByTemplateSpecResourceIdAndParams, ByTemplateSpecResourceIdAndParamsUri, ByTemplateSpecResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1e530-186">-TemplateUri</span><span class="sxs-lookup"><span data-stu-id="1e530-186">-TemplateUri</span></span>
<span data-ttu-id="1e530-187">Uri 到範本檔案。</span><span class="sxs-lookup"><span data-stu-id="1e530-187">Uri to the template file.</span></span>

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

### <span data-ttu-id="1e530-188">-WhatIfExcludeChangeType</span><span class="sxs-lookup"><span data-stu-id="1e530-188">-WhatIfExcludeChangeType</span></span>
<span data-ttu-id="1e530-189">將逗號分隔的資源變更類型排除在What-If結果。</span><span class="sxs-lookup"><span data-stu-id="1e530-189">Comma-separated resource change types to be excluded from What-If results.</span></span> <span data-ttu-id="1e530-190">適用于設定 -WhatIf 或 -Confirm 開關時。</span><span class="sxs-lookup"><span data-stu-id="1e530-190">Applicable when the -WhatIf or -Confirm switch is set.</span></span>

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

### <span data-ttu-id="1e530-191">-WhatIfResultFormat</span><span class="sxs-lookup"><span data-stu-id="1e530-191">-WhatIfResultFormat</span></span>
<span data-ttu-id="1e530-192">此What-If格式。</span><span class="sxs-lookup"><span data-stu-id="1e530-192">The What-If result format.</span></span> <span data-ttu-id="1e530-193">適用于設定 -WhatIf 或 -Confirm 開關時。</span><span class="sxs-lookup"><span data-stu-id="1e530-193">Applicable when the -WhatIf or -Confirm switch is set.</span></span>

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

### <span data-ttu-id="1e530-194">-確認</span><span class="sxs-lookup"><span data-stu-id="1e530-194">-Confirm</span></span>
<span data-ttu-id="1e530-195">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="1e530-195">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1e530-196">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1e530-196">-WhatIf</span></span>
<span data-ttu-id="1e530-197">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="1e530-197">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1e530-198">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="1e530-198">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1e530-199">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1e530-199">CommonParameters</span></span>
<span data-ttu-id="1e530-200">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="1e530-200">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1e530-201">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1e530-201">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1e530-202">輸入</span><span class="sxs-lookup"><span data-stu-id="1e530-202">INPUTS</span></span>

### <span data-ttu-id="1e530-203">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="1e530-203">System.Collections.Hashtable</span></span>

### <span data-ttu-id="1e530-204">System.String</span><span class="sxs-lookup"><span data-stu-id="1e530-204">System.String</span></span>

## <span data-ttu-id="1e530-205">輸出</span><span class="sxs-lookup"><span data-stu-id="1e530-205">OUTPUTS</span></span>

### <span data-ttu-id="1e530-206">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span><span class="sxs-lookup"><span data-stu-id="1e530-206">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="1e530-207">筆記</span><span class="sxs-lookup"><span data-stu-id="1e530-207">NOTES</span></span>

## <span data-ttu-id="1e530-208">相關連結</span><span class="sxs-lookup"><span data-stu-id="1e530-208">RELATED LINKS</span></span>
