---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 6E2F0D5E-E683-46F3-B48B-55C4864F3308
online version: https://docs.microsoft.com/powershell/module/az.resources/new-azresourcegroupdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzResourceGroupDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzResourceGroupDeployment.md
ms.openlocfilehash: 3403900fafae1615f8253b4d5671e497a1d507f3
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101908461"
---
# <span data-ttu-id="64992-101">New-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="64992-101">New-AzResourceGroupDeployment</span></span>

## <span data-ttu-id="64992-102">簡介</span><span class="sxs-lookup"><span data-stu-id="64992-102">SYNOPSIS</span></span>
<span data-ttu-id="64992-103">新增 Azure 部署至資源群組。</span><span class="sxs-lookup"><span data-stu-id="64992-103">Adds an Azure deployment to a resource group.</span></span>

## <span data-ttu-id="64992-104">語法</span><span class="sxs-lookup"><span data-stu-id="64992-104">SYNTAX</span></span>

### <span data-ttu-id="64992-105">ByTemplateFileWithNoParameters (預設) </span><span class="sxs-lookup"><span data-stu-id="64992-105">ByTemplateFileWithNoParameters (Default)</span></span>
```
New-AzResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-Force]
 [-AsJob] [-QueryString <String>] -TemplateFile <String> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="64992-106">ByTemplateObjectAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="64992-106">ByTemplateObjectAndParameterObject</span></span>
```
New-AzResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-Force]
 [-AsJob] [-QueryString <String>] -TemplateParameterObject <Hashtable> -TemplateObject <Hashtable>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="64992-107">ByTemplateFileAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="64992-107">ByTemplateFileAndParameterObject</span></span>
```
New-AzResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-Force]
 [-AsJob] [-QueryString <String>] -TemplateParameterObject <Hashtable> -TemplateFile <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="64992-108">ByTemplateUriAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="64992-108">ByTemplateUriAndParameterObject</span></span>
```
New-AzResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-Force]
 [-AsJob] [-QueryString <String>] -TemplateParameterObject <Hashtable> -TemplateUri <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="64992-109">ByTemplateSpecResourceIdAndParamsObject</span><span class="sxs-lookup"><span data-stu-id="64992-109">ByTemplateSpecResourceIdAndParamsObject</span></span>
```
New-AzResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-Force]
 [-AsJob] [-QueryString <String>] -TemplateParameterObject <Hashtable> -TemplateSpecId <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="64992-110">ByTemplateObjectAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="64992-110">ByTemplateObjectAndParameterFile</span></span>
```
New-AzResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-Force]
 [-AsJob] [-QueryString <String>] -TemplateParameterFile <String> -TemplateObject <Hashtable>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="64992-111">ByTemplateFileAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="64992-111">ByTemplateFileAndParameterFile</span></span>
```
New-AzResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-Force]
 [-AsJob] [-QueryString <String>] -TemplateParameterFile <String> -TemplateFile <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="64992-112">ByTemplateUriAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="64992-112">ByTemplateUriAndParameterFile</span></span>
```
New-AzResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-Force]
 [-AsJob] [-QueryString <String>] -TemplateParameterFile <String> -TemplateUri <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="64992-113">ByTemplateSpecResourceIdAndParams</span><span class="sxs-lookup"><span data-stu-id="64992-113">ByTemplateSpecResourceIdAndParams</span></span>
```
New-AzResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-Force]
 [-AsJob] [-QueryString <String>] -TemplateParameterFile <String> -TemplateSpecId <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="64992-114">ByTemplateObjectAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="64992-114">ByTemplateObjectAndParameterUri</span></span>
```
New-AzResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-Force]
 [-AsJob] [-QueryString <String>] -TemplateParameterUri <String> -TemplateObject <Hashtable>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="64992-115">ByTemplateFileAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="64992-115">ByTemplateFileAndParameterUri</span></span>
```
New-AzResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-Force]
 [-AsJob] [-QueryString <String>] -TemplateParameterUri <String> -TemplateFile <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="64992-116">ByTemplateUriAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="64992-116">ByTemplateUriAndParameterUri</span></span>
```
New-AzResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-Force]
 [-AsJob] [-QueryString <String>] -TemplateParameterUri <String> -TemplateUri <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="64992-117">ByTemplateSpecResourceIdAndParamsUri</span><span class="sxs-lookup"><span data-stu-id="64992-117">ByTemplateSpecResourceIdAndParamsUri</span></span>
```
New-AzResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-Force]
 [-AsJob] [-QueryString <String>] -TemplateParameterUri <String> -TemplateSpecId <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="64992-118">ByTemplateObjectWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="64992-118">ByTemplateObjectWithNoParameters</span></span>
```
New-AzResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-Force]
 [-AsJob] [-QueryString <String>] -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="64992-119">ByTemplateUriWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="64992-119">ByTemplateUriWithNoParameters</span></span>
```
New-AzResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-Force]
 [-AsJob] [-QueryString <String>] -TemplateUri <String> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="64992-120">ByTemplateSpecResourceId</span><span class="sxs-lookup"><span data-stu-id="64992-120">ByTemplateSpecResourceId</span></span>
```
New-AzResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-Force]
 [-AsJob] [-QueryString <String>] -TemplateSpecId <String> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="64992-121">描述</span><span class="sxs-lookup"><span data-stu-id="64992-121">DESCRIPTION</span></span>
<span data-ttu-id="64992-122">**New-AzResourceGroupDeployment** Cmdlet 會將部署新增到現有的資源群組。</span><span class="sxs-lookup"><span data-stu-id="64992-122">The **New-AzResourceGroupDeployment** cmdlet adds a deployment to an existing resource group.</span></span>
<span data-ttu-id="64992-123">這包括部署所需的資源。</span><span class="sxs-lookup"><span data-stu-id="64992-123">This includes the resources that the deployment requires.</span></span>
<span data-ttu-id="64992-124">Azure 資源是使用者管理的 Azure 實體，例如資料庫伺服器、資料庫、網站、虛擬機器或儲存空間帳戶。</span><span class="sxs-lookup"><span data-stu-id="64992-124">An Azure resource is a user-managed Azure entity, such as a database server, database, website, virtual machine, or Storage account.</span></span>
<span data-ttu-id="64992-125">Azure 資源群組是部署為一個單位的 Azure 資源集合，例如財務網站所需的網站、資料庫伺服器和資料庫。</span><span class="sxs-lookup"><span data-stu-id="64992-125">An Azure resource group is a collection of Azure resources that are deployed as a unit, such as the website, database server, and databases that are required for a financial website.</span></span>
<span data-ttu-id="64992-126">資源群組部署會使用範本將資源新增到資源群組，併發布資源，讓資源在 Azure 中可供使用。</span><span class="sxs-lookup"><span data-stu-id="64992-126">A resource group deployment uses a template to add resources to a resource group and publishes them so that they are available in Azure.</span></span>
<span data-ttu-id="64992-127">若要在不使用範本的情況下將資源新增到資源群組，請使用 New-AzResource Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="64992-127">To add resources to a resource group without using a template, use the New-AzResource cmdlet.</span></span>
<span data-ttu-id="64992-128">若要新增資源群組部署，請指定現有資源組的名稱和資源群組範本。</span><span class="sxs-lookup"><span data-stu-id="64992-128">To add a resource group deployment, specify the name of an existing resource group and a resource group template.</span></span>
<span data-ttu-id="64992-129">資源群組範本是 JSON 字串，代表複雜雲端式服務的資源群組，例如網頁入口網站。</span><span class="sxs-lookup"><span data-stu-id="64992-129">A resource group template is a JSON string that represents a resource group for a complex cloud-based service, such as a web portal.</span></span>
<span data-ttu-id="64992-130">範本包含所需資源的參數預留位置，以及可設定屬性值 ，例如名稱和大小。</span><span class="sxs-lookup"><span data-stu-id="64992-130">The template includes parameter placeholders for required resources and configurable property values, such as names and sizes.</span></span>
<span data-ttu-id="64992-131">您可以在 Azure 範本庫中找到許多範本，也可以建立自己的範本。</span><span class="sxs-lookup"><span data-stu-id="64992-131">You can find many templates in the Azure template gallery or you can create your own templates.</span></span>
<span data-ttu-id="64992-132">若要使用自訂範本建立資源群組，請指定 *TemplateFile* 參數或 *TemplateUri* 參數。</span><span class="sxs-lookup"><span data-stu-id="64992-132">To use a custom template to create a resource group, specify the *TemplateFile* parameter or *TemplateUri* parameter.</span></span>
<span data-ttu-id="64992-133">每個範本都有可設定屬性的參數。</span><span class="sxs-lookup"><span data-stu-id="64992-133">Each template has parameters for configurable properties.</span></span>
<span data-ttu-id="64992-134">若要指定範本參數的值，請指定 *TemplateParameterFile* 參數或 *TemplateParameterObject* 參數。</span><span class="sxs-lookup"><span data-stu-id="64992-134">To specify values for the template parameters, specify the *TemplateParameterFile* parameter or the *TemplateParameterObject* parameter.</span></span>
<span data-ttu-id="64992-135">或者，您也可以使用指定範本時動態新加入命令的範本參數。</span><span class="sxs-lookup"><span data-stu-id="64992-135">Alternatively, you can use the template parameters that are dynamically added to the command when you specify a template.</span></span>
<span data-ttu-id="64992-136">若要使用動態參數，請于命令提示文字輸入參數，或輸入減號 (-) 來表示參數，並使用 Tab 鍵迴圈流覽可用的參數。</span><span class="sxs-lookup"><span data-stu-id="64992-136">To use dynamic parameters, type them at the command prompt, or type a minus sign (-) to indicate a parameter and use the Tab key to cycle through available parameters.</span></span>
<span data-ttu-id="64992-137">在命令提示提示輸入的範本參數值優先于範本參數物件或檔案中的值。</span><span class="sxs-lookup"><span data-stu-id="64992-137">Template parameter values that you enter at the command prompt take precedence over values in a template parameter object or file.</span></span>

## <span data-ttu-id="64992-138">例子</span><span class="sxs-lookup"><span data-stu-id="64992-138">EXAMPLES</span></span>

### <span data-ttu-id="64992-139">範例 1：使用自訂範本和參數檔案建立部署</span><span class="sxs-lookup"><span data-stu-id="64992-139">Example 1: Use a custom template and parameter file to create a deployment</span></span>
```powershell
PS C:\> New-AzResourceGroupDeployment -ResourceGroupName "ContosoEngineering" -TemplateFile "D:\Azure\Templates\EngineeringSite.json" -TemplateParameterFile "D:\Azure\Templates\EngSiteParms.json" -Tag @{"key1"="value1"; "key2"="value2";}
```

<span data-ttu-id="64992-140">此命令會使用自訂範本和磁片上具有已定義之標籤參數的範本檔案來建立新部署。</span><span class="sxs-lookup"><span data-stu-id="64992-140">This command creates a new deployment by using a custom template and a template file on disk, with defined tags parameter.</span></span>
<span data-ttu-id="64992-141">該命令使用 *TemplateFile* 參數來指定範本，而 *TemplateParameterFile* 參數則指定包含參數和參數值的檔案。</span><span class="sxs-lookup"><span data-stu-id="64992-141">The command uses the *TemplateFile* parameter to specify the template and the *TemplateParameterFile* parameter to specify a file that contains parameters and parameter values.</span></span>

### <span data-ttu-id="64992-142">範例 2：使用自訂範本物件和參數檔案建立部署</span><span class="sxs-lookup"><span data-stu-id="64992-142">Example 2: Use a custom template object and parameter file to create a deployment</span></span>
```powershell
PS C:\> $TemplateFileText = [System.IO.File]::ReadAllText("D:\Azure\Templates\EngineeringSite.json")
PS C:\> $TemplateObject = ConvertFrom-Json $TemplateFileText -AsHashtable
PS C:\> New-AzResourceGroupDeployment -ResourceGroupName "ContosoEngineering" -TemplateObject $TemplateObject -TemplateParameterFile "D:\Azure\Templates\EngSiteParams.json"
```

<span data-ttu-id="64992-143">此命令會使用已轉換成記憶體雜湊表的自訂和範本檔案來建立新部署。</span><span class="sxs-lookup"><span data-stu-id="64992-143">This command creates a new deployment by using a custom and a template file on disk that has been converted to an in-memory hashtable.</span></span>
<span data-ttu-id="64992-144">前兩個命令會讀取磁片上範本檔案的文字，並將它轉換成記憶體內雜湊表。</span><span class="sxs-lookup"><span data-stu-id="64992-144">The first two commands read the text for the template file on disk and convert it to an in-memory hashtable.</span></span>
<span data-ttu-id="64992-145">最後一個命令使用 *TemplateObject* 參數來指定雜湊表，而 *TemplateParameterFile* 參數則指定包含參數和參數值的檔案。</span><span class="sxs-lookup"><span data-stu-id="64992-145">The last command uses the *TemplateObject* parameter to specify the hashtable and the *TemplateParameterFile* parameter to specify a file that contains parameters and parameter values.</span></span>

### <span data-ttu-id="64992-146">範例 3</span><span class="sxs-lookup"><span data-stu-id="64992-146">Example 3</span></span>

<span data-ttu-id="64992-147">新增 Azure 部署至資源群組。</span><span class="sxs-lookup"><span data-stu-id="64992-147">Adds an Azure deployment to a resource group.</span></span> <span data-ttu-id="64992-148"> (自動) </span><span class="sxs-lookup"><span data-stu-id="64992-148">(autogenerated)</span></span>

<!-- Aladdin Generated Example -->


```powershell
New-AzResourceGroupDeployment -DeploymentDebugLogLevel RequestContent -Name mynewstorageaccount -ResourceGroupName 'ContosoEngineering' -TemplateFile 'D:\Azure\Templates\EngineeringSite.json' -TemplateParameterObject <Hashtable>
```

### <span data-ttu-id="64992-149">範例 4：使用 uri 和 SAS 權杖部署儲存在非公用儲存帳戶中的範本</span><span class="sxs-lookup"><span data-stu-id="64992-149">Example 4: Deploy a template stored in a non public storage account using a uri and SAS token</span></span>
```powershell
PS C:\> New-AzResourceGroupDeployment -ResourceGroupName "RGName" -TemplateUri "https://example.com/example.json" -QueryString "foo"
```

<span data-ttu-id="64992-150">此命令會使用 TemplateUri 中的範本建立新部署，範本不是公用的，而且需要權杖參數來存取，這會使用 QueryString 參數提供。</span><span class="sxs-lookup"><span data-stu-id="64992-150">This command creates a new deployment using the template in TemplateUri which is not public and requires a token parameter to access which would be provided using the QueryString parameter.</span></span>
<span data-ttu-id="64992-151">執行此命令會使用 URL 有效地存取範本 https://example.com/example.json?foo 。</span><span class="sxs-lookup"><span data-stu-id="64992-151">Running this command effectively accesses the template using the url https://example.com/example.json?foo.</span></span>
<span data-ttu-id="64992-152">如果您想要在儲存帳戶中使用範本，請使用此功能，方法為提供 SAS 權杖做為 QueryString</span><span class="sxs-lookup"><span data-stu-id="64992-152">This can be used if you want to use a template in a storage account by providing the SAS token as the QueryString</span></span>

## <span data-ttu-id="64992-153">參數</span><span class="sxs-lookup"><span data-stu-id="64992-153">PARAMETERS</span></span>

### <span data-ttu-id="64992-154">-AsJob</span><span class="sxs-lookup"><span data-stu-id="64992-154">-AsJob</span></span>
<span data-ttu-id="64992-155">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="64992-155">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="64992-156">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="64992-156">-DefaultProfile</span></span>
<span data-ttu-id="64992-157">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="64992-157">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="64992-158">-DeploymentDelogLogLevel</span><span class="sxs-lookup"><span data-stu-id="64992-158">-DeploymentDebugLogLevel</span></span>
<span data-ttu-id="64992-159">指定一個錯誤記錄層級。</span><span class="sxs-lookup"><span data-stu-id="64992-159">Specifies a debug log level.</span></span>
<span data-ttu-id="64992-160">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="64992-160">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="64992-161">RequestContent</span><span class="sxs-lookup"><span data-stu-id="64992-161">RequestContent</span></span>
- <span data-ttu-id="64992-162">ResponseContent</span><span class="sxs-lookup"><span data-stu-id="64992-162">ResponseContent</span></span>
- <span data-ttu-id="64992-163">所有</span><span class="sxs-lookup"><span data-stu-id="64992-163">All</span></span>
- <span data-ttu-id="64992-164">沒有</span><span class="sxs-lookup"><span data-stu-id="64992-164">None</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: RequestContent, ResponseContent, All, None

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="64992-165">-強制</span><span class="sxs-lookup"><span data-stu-id="64992-165">-Force</span></span>
<span data-ttu-id="64992-166">強制執行命令，但不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="64992-166">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="64992-167">-模式</span><span class="sxs-lookup"><span data-stu-id="64992-167">-Mode</span></span>
<span data-ttu-id="64992-168">指定部署模式。</span><span class="sxs-lookup"><span data-stu-id="64992-168">Specifies the deployment mode.</span></span> <span data-ttu-id="64992-169">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="64992-169">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="64992-170">完成：在完整模式中，Resource Manager 會刪除存在於資源群組中，但在範本中未指定的資源。</span><span class="sxs-lookup"><span data-stu-id="64992-170">Complete: In complete mode, Resource Manager deletes resources that exist in the resource group but are not specified in the template.</span></span> 
- <span data-ttu-id="64992-171">增量：在增量模式中，Resource Manager 會保留存在於資源群組中但不在範本中指定的未變動資源。</span><span class="sxs-lookup"><span data-stu-id="64992-171">Incremental: In incremental mode, Resource Manager leaves unchanged resources that exist in the resource group but are not specified in the template.</span></span>

```yaml
Type: Microsoft.Azure.Management.ResourceManager.Models.DeploymentMode
Parameter Sets: (All)
Aliases:
Accepted values: Incremental, Complete

Required: False
Position: Named
Default value: Incremental
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="64992-172">-名稱</span><span class="sxs-lookup"><span data-stu-id="64992-172">-Name</span></span>
<span data-ttu-id="64992-173">要建立之部署的名稱。</span><span class="sxs-lookup"><span data-stu-id="64992-173">The name of the deployment it's going to create.</span></span> <span data-ttu-id="64992-174">如果未指定，則提供範本檔案時預設為範本檔案名;預設為提供範本物件的目前時間，例如"20131223140835"。</span><span class="sxs-lookup"><span data-stu-id="64992-174">If not specified, defaults to the template file name when a template file is provided; defaults to the current time when a template object is provided, e.g. "20131223140835".</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: DeploymentName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="64992-175">-Pre</span><span class="sxs-lookup"><span data-stu-id="64992-175">-Pre</span></span>
<span data-ttu-id="64992-176">表示此 Cmdlet 會在自動決定要使用哪個版本時，考慮測試版 API 版本。</span><span class="sxs-lookup"><span data-stu-id="64992-176">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="64992-177">-QueryString</span><span class="sxs-lookup"><span data-stu-id="64992-177">-QueryString</span></span>
<span data-ttu-id="64992-178">查詢字串 (例如，一個 SAS 權杖) TemplateUri 參數一起使用。</span><span class="sxs-lookup"><span data-stu-id="64992-178">The query string (for example, a SAS token) to be used with the TemplateUri parameter.</span></span> <span data-ttu-id="64992-179">會用於連結範本的情況</span><span class="sxs-lookup"><span data-stu-id="64992-179">Would be used in case of linked templates</span></span>

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

### <span data-ttu-id="64992-180">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="64992-180">-ResourceGroupName</span></span>
<span data-ttu-id="64992-181">指定要部署的資源組名。</span><span class="sxs-lookup"><span data-stu-id="64992-181">Specifies the name of the resource group to deploy.</span></span>

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

### <span data-ttu-id="64992-182">-RollBackDeploymentName</span><span class="sxs-lookup"><span data-stu-id="64992-182">-RollBackDeploymentName</span></span>
<span data-ttu-id="64992-183">如果使用 -RollbackToLastDeployment，則不應該使用資源群組中具有指定名稱的成功部署。</span><span class="sxs-lookup"><span data-stu-id="64992-183">Rollback to the successful deployment with the given name in the resource group, should not be used if -RollbackToLastDeployment is used.</span></span>

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

### <span data-ttu-id="64992-184">-RollbackToLastDeployment</span><span class="sxs-lookup"><span data-stu-id="64992-184">-RollbackToLastDeployment</span></span>
<span data-ttu-id="64992-185">如果使用 -RollBackDeploymentName，則不應該出現資源群組中最後一個成功部署的卷回。</span><span class="sxs-lookup"><span data-stu-id="64992-185">Rollback to the last successful deployment in the resource group, should not be present if -RollBackDeploymentName is used.</span></span>

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

### <span data-ttu-id="64992-186">-SkipTemplateParameterPrompt</span><span class="sxs-lookup"><span data-stu-id="64992-186">-SkipTemplateParameterPrompt</span></span>
<span data-ttu-id="64992-187">跳過 PowerShell 動態參數處理，檢查所提供的範本參數是否包含範本使用的所有必要參數。</span><span class="sxs-lookup"><span data-stu-id="64992-187">Skips the PowerShell dynamic parameter processing that checks if the provided template parameter contains all necessary parameters used by the template.</span></span> <span data-ttu-id="64992-188">這項檢查會提示使用者提供遺失參數的值，但若發現參數未系在範本中，則提供 -SkipTemplateParameterPrompt 會忽略此提示並立即錯誤。</span><span class="sxs-lookup"><span data-stu-id="64992-188">This check would prompt the user to provide a value for the missing parameters, but providing the -SkipTemplateParameterPrompt will ignore this prompt and error out immediately if a parameter was found not to be bound in the template.</span></span> <span data-ttu-id="64992-189">針對非互動式腳本，您可以提供 -SkipTemplateParameterPrompt，以在未滿足所有所需參數的情況下提供更佳的錯誤訊息。</span><span class="sxs-lookup"><span data-stu-id="64992-189">For non-interactive scripts, -SkipTemplateParameterPrompt can be provided to provide a better error message in the case where not all required parameters are satisfied.</span></span>

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

### <span data-ttu-id="64992-190">-標記</span><span class="sxs-lookup"><span data-stu-id="64992-190">-Tag</span></span>
<span data-ttu-id="64992-191">要放在部署的標記。</span><span class="sxs-lookup"><span data-stu-id="64992-191">The tags to put on the deployment.</span></span>

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

### <span data-ttu-id="64992-192">-TemplateFile</span><span class="sxs-lookup"><span data-stu-id="64992-192">-TemplateFile</span></span>
<span data-ttu-id="64992-193">指定範本檔案的完整路徑。</span><span class="sxs-lookup"><span data-stu-id="64992-193">Specifies the full path of a template file.</span></span> <span data-ttu-id="64992-194">支援的範本檔案類型：json 和 bicep。</span><span class="sxs-lookup"><span data-stu-id="64992-194">Supported template file type: json and bicep.</span></span>
<span data-ttu-id="64992-195">這可以是儲存為 JSON 檔案的自訂範本或圖庫範本，例如使用 **Save-AzResourceGroupGalleryTemplate** Cmdlet 所建立。</span><span class="sxs-lookup"><span data-stu-id="64992-195">This can be a custom template or a gallery template that is saved as a JSON file, such as one created by using the **Save-AzResourceGroupGalleryTemplate** cmdlet.</span></span>

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

### <span data-ttu-id="64992-196">-TemplateObject</span><span class="sxs-lookup"><span data-stu-id="64992-196">-TemplateObject</span></span>
<span data-ttu-id="64992-197">代表範本的雜湊表格。</span><span class="sxs-lookup"><span data-stu-id="64992-197">A hash table which represents the template.</span></span>

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

### <span data-ttu-id="64992-198">-TemplateParameterFile</span><span class="sxs-lookup"><span data-stu-id="64992-198">-TemplateParameterFile</span></span>
<span data-ttu-id="64992-199">指定包含範本參數名稱和值的 JSON 檔案完整路徑。</span><span class="sxs-lookup"><span data-stu-id="64992-199">Specifies the full path of a JSON file that contains the names and values of the template parameters.</span></span>
<span data-ttu-id="64992-200">如果範本有參數，則必須使用 *TemplateParameterFile* 參數或 *TemplateParameterObject* 參數指定參數值。</span><span class="sxs-lookup"><span data-stu-id="64992-200">If a template has parameters, you must specify the parameter values with the *TemplateParameterFile* parameter or the *TemplateParameterObject* parameter.</span></span>
<span data-ttu-id="64992-201">當您指定範本時，範本參數會動態新增到命令中。</span><span class="sxs-lookup"><span data-stu-id="64992-201">Template parameters are dynamically added to the command when you specify a template.</span></span>
<span data-ttu-id="64992-202">若要使用動態參數，請輸入減號 (-) 以指出參數名稱，然後使用 Tab 鍵迴圈流覽可用的參數。</span><span class="sxs-lookup"><span data-stu-id="64992-202">To use the dynamic parameters, type a minus sign (-) to indicate a parameter name and then use the Tab key to cycle through the available parameters.</span></span>

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

### <span data-ttu-id="64992-203">-TemplateParameterObject</span><span class="sxs-lookup"><span data-stu-id="64992-203">-TemplateParameterObject</span></span>
<span data-ttu-id="64992-204">指定範本參數名稱和值的雜湊表格。</span><span class="sxs-lookup"><span data-stu-id="64992-204">Specifies a hash table of template parameter names and values.</span></span>
<span data-ttu-id="64992-205">有關 Windows PowerShell 中雜湊表格的協助，請鍵入 `Get-Help about_Hash_Tables` 。</span><span class="sxs-lookup"><span data-stu-id="64992-205">For help with hash tables in Windows PowerShell, type `Get-Help about_Hash_Tables`.</span></span>
<span data-ttu-id="64992-206">如果範本有參數，則必須指定參數值。</span><span class="sxs-lookup"><span data-stu-id="64992-206">If a template has parameters, you must specify parameter values.</span></span>
<span data-ttu-id="64992-207">當您指定範本時，範本參數會動態新增到命令中。</span><span class="sxs-lookup"><span data-stu-id="64992-207">Template parameters are dynamically added to the command when you specify a template.</span></span>

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

### <span data-ttu-id="64992-208">-TemplateParameterUri</span><span class="sxs-lookup"><span data-stu-id="64992-208">-TemplateParameterUri</span></span>
<span data-ttu-id="64992-209">指定範本參數檔案的 URI。</span><span class="sxs-lookup"><span data-stu-id="64992-209">Specifies the URI of a template parameters file.</span></span>

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

### <span data-ttu-id="64992-210">-TemplateSpecId</span><span class="sxs-lookup"><span data-stu-id="64992-210">-TemplateSpecId</span></span>
<span data-ttu-id="64992-211">要部署的 templateSpec 資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="64992-211">Resource ID of the templateSpec to be deployed.</span></span>

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

### <span data-ttu-id="64992-212">-TemplateUri</span><span class="sxs-lookup"><span data-stu-id="64992-212">-TemplateUri</span></span>
<span data-ttu-id="64992-213">指定範本檔案的 URI。</span><span class="sxs-lookup"><span data-stu-id="64992-213">Specifies the URI of a template file.</span></span>
<span data-ttu-id="64992-214">此檔案可以是儲存為 JSON 檔案的自訂範本或圖庫範本，例如使用 **Save-AzResourceGroupGalleryTemplate。**</span><span class="sxs-lookup"><span data-stu-id="64992-214">This file can be a custom template or a gallery template that is saved as a JSON file, such as by using **Save-AzResourceGroupGalleryTemplate**.</span></span>

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

### <span data-ttu-id="64992-215">-WhatIfExcludeChangeType</span><span class="sxs-lookup"><span data-stu-id="64992-215">-WhatIfExcludeChangeType</span></span>
<span data-ttu-id="64992-216">將逗號分隔的資源變更類型排除在What-If結果。</span><span class="sxs-lookup"><span data-stu-id="64992-216">Comma-separated resource change types to be excluded from What-If results.</span></span> <span data-ttu-id="64992-217">適用于設定 -WhatIf 或 -Confirm 開關時。</span><span class="sxs-lookup"><span data-stu-id="64992-217">Applicable when the -WhatIf or -Confirm switch is set.</span></span>

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

### <span data-ttu-id="64992-218">-WhatIfResultFormat</span><span class="sxs-lookup"><span data-stu-id="64992-218">-WhatIfResultFormat</span></span>
<span data-ttu-id="64992-219">此What-If格式。</span><span class="sxs-lookup"><span data-stu-id="64992-219">The What-If result format.</span></span>

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

### <span data-ttu-id="64992-220">-確認</span><span class="sxs-lookup"><span data-stu-id="64992-220">-Confirm</span></span>
<span data-ttu-id="64992-221">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="64992-221">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64992-222">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="64992-222">-WhatIf</span></span>
<span data-ttu-id="64992-223">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="64992-223">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="64992-224">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="64992-224">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64992-225">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="64992-225">CommonParameters</span></span>
<span data-ttu-id="64992-226">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="64992-226">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="64992-227">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="64992-227">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="64992-228">輸入</span><span class="sxs-lookup"><span data-stu-id="64992-228">INPUTS</span></span>

### <span data-ttu-id="64992-229">System.String</span><span class="sxs-lookup"><span data-stu-id="64992-229">System.String</span></span>

### <span data-ttu-id="64992-230">Microsoft.Azure.management.ResourceManager.models.DeploymentMode</span><span class="sxs-lookup"><span data-stu-id="64992-230">Microsoft.Azure.Management.ResourceManager.Models.DeploymentMode</span></span>

### <span data-ttu-id="64992-231">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="64992-231">System.Collections.Hashtable</span></span>

## <span data-ttu-id="64992-232">輸出</span><span class="sxs-lookup"><span data-stu-id="64992-232">OUTPUTS</span></span>

### <span data-ttu-id="64992-233">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="64992-233">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceGroupDeployment</span></span>

## <span data-ttu-id="64992-234">筆記</span><span class="sxs-lookup"><span data-stu-id="64992-234">NOTES</span></span>

## <span data-ttu-id="64992-235">相關連結</span><span class="sxs-lookup"><span data-stu-id="64992-235">RELATED LINKS</span></span>

[<span data-ttu-id="64992-236">Get-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="64992-236">Get-AzResourceGroupDeployment</span></span>](./Get-AzResourceGroupDeployment.md)

[<span data-ttu-id="64992-237">New-AzResource</span><span class="sxs-lookup"><span data-stu-id="64992-237">New-AzResource</span></span>](./New-AzResource.md)

[<span data-ttu-id="64992-238">New-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="64992-238">New-AzResourceGroup</span></span>](./New-AzResourceGroup.md)

[<span data-ttu-id="64992-239">Remove-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="64992-239">Remove-AzResourceGroupDeployment</span></span>](./Remove-AzResourceGroupDeployment.md)

[<span data-ttu-id="64992-240">Stop-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="64992-240">Stop-AzResourceGroupDeployment</span></span>](./Stop-AzResourceGroupDeployment.md)

[<span data-ttu-id="64992-241">Test-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="64992-241">Test-AzResourceGroupDeployment</span></span>](./Test-AzResourceGroupDeployment.md)