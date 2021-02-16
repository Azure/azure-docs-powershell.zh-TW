---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 6E2F0D5E-E683-46F3-B48B-55C4864F3308
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-azresourcegroupdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzResourceGroupDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzResourceGroupDeployment.md
ms.openlocfilehash: 3e704885c4ce2df0aee2a9b890f768983f93d7bf
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100132215"
---
# <span data-ttu-id="0eb5f-101">New-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="0eb5f-101">New-AzResourceGroupDeployment</span></span>

## <span data-ttu-id="0eb5f-102">摘要</span><span class="sxs-lookup"><span data-stu-id="0eb5f-102">SYNOPSIS</span></span>
<span data-ttu-id="0eb5f-103">新增 Azure 部署至資源群組。</span><span class="sxs-lookup"><span data-stu-id="0eb5f-103">Adds an Azure deployment to a resource group.</span></span>

## <span data-ttu-id="0eb5f-104">句法</span><span class="sxs-lookup"><span data-stu-id="0eb5f-104">SYNTAX</span></span>

### <span data-ttu-id="0eb5f-105">ByTemplateFileWithNoParameters (預設) </span><span class="sxs-lookup"><span data-stu-id="0eb5f-105">ByTemplateFileWithNoParameters (Default)</span></span>
```
New-AzResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-Force]
 [-AsJob] [-QueryString <String>] -TemplateFile <String> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0eb5f-106">ByTemplateObjectAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="0eb5f-106">ByTemplateObjectAndParameterObject</span></span>
```
New-AzResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-Force]
 [-AsJob] [-QueryString <String>] -TemplateParameterObject <Hashtable> -TemplateObject <Hashtable>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="0eb5f-107">ByTemplateFileAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="0eb5f-107">ByTemplateFileAndParameterObject</span></span>
```
New-AzResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-Force]
 [-AsJob] [-QueryString <String>] -TemplateParameterObject <Hashtable> -TemplateFile <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="0eb5f-108">ByTemplateUriAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="0eb5f-108">ByTemplateUriAndParameterObject</span></span>
```
New-AzResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-Force]
 [-AsJob] [-QueryString <String>] -TemplateParameterObject <Hashtable> -TemplateUri <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="0eb5f-109">ByTemplateObjectAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="0eb5f-109">ByTemplateObjectAndParameterFile</span></span>
```
New-AzResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-Force]
 [-AsJob] [-QueryString <String>] -TemplateParameterFile <String> -TemplateObject <Hashtable>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="0eb5f-110">ByTemplateFileAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="0eb5f-110">ByTemplateFileAndParameterFile</span></span>
```
New-AzResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-Force]
 [-AsJob] [-QueryString <String>] -TemplateParameterFile <String> -TemplateFile <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="0eb5f-111">ByTemplateUriAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="0eb5f-111">ByTemplateUriAndParameterFile</span></span>
```
New-AzResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-Force]
 [-AsJob] [-QueryString <String>] -TemplateParameterFile <String> -TemplateUri <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="0eb5f-112">ByTemplateSpecResourceIdAndParams</span><span class="sxs-lookup"><span data-stu-id="0eb5f-112">ByTemplateSpecResourceIdAndParams</span></span>
```
New-AzResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-Force]
 [-AsJob] [-QueryString <String>] -TemplateParameterFile <String> -TemplateSpecId <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="0eb5f-113">ByTemplateObjectAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="0eb5f-113">ByTemplateObjectAndParameterUri</span></span>
```
New-AzResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-Force]
 [-AsJob] [-QueryString <String>] -TemplateParameterUri <String> -TemplateObject <Hashtable>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="0eb5f-114">ByTemplateFileAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="0eb5f-114">ByTemplateFileAndParameterUri</span></span>
```
New-AzResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-Force]
 [-AsJob] [-QueryString <String>] -TemplateParameterUri <String> -TemplateFile <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="0eb5f-115">ByTemplateUriAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="0eb5f-115">ByTemplateUriAndParameterUri</span></span>
```
New-AzResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-Force]
 [-AsJob] [-QueryString <String>] -TemplateParameterUri <String> -TemplateUri <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="0eb5f-116">ByTemplateSpecResourceIdAndParamsUri</span><span class="sxs-lookup"><span data-stu-id="0eb5f-116">ByTemplateSpecResourceIdAndParamsUri</span></span>
```
New-AzResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-Force]
 [-AsJob] [-QueryString <String>] -TemplateParameterUri <String> -TemplateSpecId <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="0eb5f-117">ByTemplateObjectWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="0eb5f-117">ByTemplateObjectWithNoParameters</span></span>
```
New-AzResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-Force]
 [-AsJob] [-QueryString <String>] -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0eb5f-118">ByTemplateUriWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="0eb5f-118">ByTemplateUriWithNoParameters</span></span>
```
New-AzResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-Force]
 [-AsJob] [-QueryString <String>] -TemplateUri <String> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0eb5f-119">ByTemplateSpecResourceId</span><span class="sxs-lookup"><span data-stu-id="0eb5f-119">ByTemplateSpecResourceId</span></span>
```
New-AzResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-Force]
 [-AsJob] [-QueryString <String>] -TemplateSpecId <String> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0eb5f-120">說明</span><span class="sxs-lookup"><span data-stu-id="0eb5f-120">DESCRIPTION</span></span>
<span data-ttu-id="0eb5f-121">**AzResourceGroupDeployment** Cmdlet 會將部署新增至現有的資源群組。</span><span class="sxs-lookup"><span data-stu-id="0eb5f-121">The **New-AzResourceGroupDeployment** cmdlet adds a deployment to an existing resource group.</span></span>
<span data-ttu-id="0eb5f-122">這包括部署所需的資源。</span><span class="sxs-lookup"><span data-stu-id="0eb5f-122">This includes the resources that the deployment requires.</span></span>
<span data-ttu-id="0eb5f-123">Azure 資源是使用者管理的 Azure 實體，例如資料庫伺服器、資料庫、網站、虛擬機器或儲存空間帳戶。</span><span class="sxs-lookup"><span data-stu-id="0eb5f-123">An Azure resource is a user-managed Azure entity, such as a database server, database, website, virtual machine, or Storage account.</span></span>
<span data-ttu-id="0eb5f-124">Azure 資源群組是一個以單位（例如網站、資料庫伺服器以及財務網站所需的資料庫）的形式來部署的 Azure 資源集合。</span><span class="sxs-lookup"><span data-stu-id="0eb5f-124">An Azure resource group is a collection of Azure resources that are deployed as a unit, such as the website, database server, and databases that are required for a financial website.</span></span>
<span data-ttu-id="0eb5f-125">資源群組部署使用範本將資源新增至資源群組，併發布資源，以便在 Azure 中使用它們。</span><span class="sxs-lookup"><span data-stu-id="0eb5f-125">A resource group deployment uses a template to add resources to a resource group and publishes them so that they are available in Azure.</span></span>
<span data-ttu-id="0eb5f-126">若要在不使用範本的情況下，將資源新增至資源群組，請使用 New-AzResource Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="0eb5f-126">To add resources to a resource group without using a template, use the New-AzResource cmdlet.</span></span>
<span data-ttu-id="0eb5f-127">若要新增資源群組部署，請指定現有資源群組和資源群組範本的名稱。</span><span class="sxs-lookup"><span data-stu-id="0eb5f-127">To add a resource group deployment, specify the name of an existing resource group and a resource group template.</span></span>
<span data-ttu-id="0eb5f-128">資源群組範本是一個 JSON 字串，代表複雜雲端服務（例如網頁入口網站）的資源群組。</span><span class="sxs-lookup"><span data-stu-id="0eb5f-128">A resource group template is a JSON string that represents a resource group for a complex cloud-based service, such as a web portal.</span></span>
<span data-ttu-id="0eb5f-129">範本包含必要資源的參數預留位置，以及可設定的屬性值，例如名稱和大小。</span><span class="sxs-lookup"><span data-stu-id="0eb5f-129">The template includes parameter placeholders for required resources and configurable property values, such as names and sizes.</span></span>
<span data-ttu-id="0eb5f-130">您可以在 Azure 範本庫中找到許多範本，或者您可以建立自己的範本。</span><span class="sxs-lookup"><span data-stu-id="0eb5f-130">You can find many templates in the Azure template gallery or you can create your own templates.</span></span>
<span data-ttu-id="0eb5f-131">若要使用自訂範本來建立資源群組，請指定 *TemplateFile* 參數或 *TemplateUri* 參數。</span><span class="sxs-lookup"><span data-stu-id="0eb5f-131">To use a custom template to create a resource group, specify the *TemplateFile* parameter or *TemplateUri* parameter.</span></span>
<span data-ttu-id="0eb5f-132">每個範本都有可設定屬性的參數。</span><span class="sxs-lookup"><span data-stu-id="0eb5f-132">Each template has parameters for configurable properties.</span></span>
<span data-ttu-id="0eb5f-133">若要指定範本參數的值，請指定 *TemplateParameterFile* 參數或 *TemplateParameterObject* 參數。</span><span class="sxs-lookup"><span data-stu-id="0eb5f-133">To specify values for the template parameters, specify the *TemplateParameterFile* parameter or the *TemplateParameterObject* parameter.</span></span>
<span data-ttu-id="0eb5f-134">或者，您也可以使用在指定範本時動態新增到命令中的範本參數。</span><span class="sxs-lookup"><span data-stu-id="0eb5f-134">Alternatively, you can use the template parameters that are dynamically added to the command when you specify a template.</span></span>
<span data-ttu-id="0eb5f-135">若要使用動態參數，請在命令提示字元輸入，或輸入減號 ( ) 來指示參數，然後使用 Tab 鍵來迴圈顯示可用的參數。</span><span class="sxs-lookup"><span data-stu-id="0eb5f-135">To use dynamic parameters, type them at the command prompt, or type a minus sign (-) to indicate a parameter and use the Tab key to cycle through available parameters.</span></span>
<span data-ttu-id="0eb5f-136">您在命令提示字元中輸入的範本參數值會優先于範本參數物件或檔案中的值。</span><span class="sxs-lookup"><span data-stu-id="0eb5f-136">Template parameter values that you enter at the command prompt take precedence over values in a template parameter object or file.</span></span>

## <span data-ttu-id="0eb5f-137">示例</span><span class="sxs-lookup"><span data-stu-id="0eb5f-137">EXAMPLES</span></span>

### <span data-ttu-id="0eb5f-138">範例1：使用自訂範本和參數檔案建立部署</span><span class="sxs-lookup"><span data-stu-id="0eb5f-138">Example 1: Use a custom template and parameter file to create a deployment</span></span>
```powershell
PS C:\> New-AzResourceGroupDeployment -ResourceGroupName "ContosoEngineering" -TemplateFile "D:\Azure\Templates\EngineeringSite.json" -TemplateParameterFile "D:\Azure\Templates\EngSiteParms.json" -Tag @{"key1"="value1"; "key2"="value2";}
```

<span data-ttu-id="0eb5f-139">這個命令會使用自訂範本與磁片上的範本檔案（含已定義的 tags 參數）來建立新的部署。</span><span class="sxs-lookup"><span data-stu-id="0eb5f-139">This command creates a new deployment by using a custom template and a template file on disk, with defined tags parameter.</span></span>
<span data-ttu-id="0eb5f-140">此命令會使用 *TemplateFile* 參數來指定範本和 *TemplateParameterFile* 參數，以指定包含參數和參數值的檔案。</span><span class="sxs-lookup"><span data-stu-id="0eb5f-140">The command uses the *TemplateFile* parameter to specify the template and the *TemplateParameterFile* parameter to specify a file that contains parameters and parameter values.</span></span>

### <span data-ttu-id="0eb5f-141">範例2：使用自訂範本物件與參數檔案建立部署</span><span class="sxs-lookup"><span data-stu-id="0eb5f-141">Example 2: Use a custom template object and parameter file to create a deployment</span></span>
```powershell
PS C:\> $TemplateFileText = [System.IO.File]::ReadAllText("D:\Azure\Templates\EngineeringSite.json")
PS C:\> $TemplateObject = ConvertFrom-Json $TemplateFileText -AsHashtable
PS C:\> New-AzResourceGroupDeployment -ResourceGroupName "ContosoEngineering" -TemplateObject $TemplateObject -TemplateParameterFile "D:\Azure\Templates\EngSiteParams.json"
```

<span data-ttu-id="0eb5f-142">這個命令會在已轉換為記憶體中 hashtable 的磁片上使用自訂範本檔案，建立新的部署。</span><span class="sxs-lookup"><span data-stu-id="0eb5f-142">This command creates a new deployment by using a custom and a template file on disk that has been converted to an in-memory hashtable.</span></span>
<span data-ttu-id="0eb5f-143">前兩個命令會讀取磁片上範本檔案的文字，並將它轉換成記憶體中的 hashtable。</span><span class="sxs-lookup"><span data-stu-id="0eb5f-143">The first two commands read the text for the template file on disk and convert it to an in-memory hashtable.</span></span>
<span data-ttu-id="0eb5f-144">最後一個命令使用 *TemplateObject* 參數來指定 Hashtable 和 *TemplateParameterFile* 參數，以指定包含參數和參數值的檔案。</span><span class="sxs-lookup"><span data-stu-id="0eb5f-144">The last command uses the *TemplateObject* parameter to specify the hashtable and the *TemplateParameterFile* parameter to specify a file that contains parameters and parameter values.</span></span>

### <span data-ttu-id="0eb5f-145">範例3</span><span class="sxs-lookup"><span data-stu-id="0eb5f-145">Example 3</span></span>

<span data-ttu-id="0eb5f-146">新增 Azure 部署至資源群組。</span><span class="sxs-lookup"><span data-stu-id="0eb5f-146">Adds an Azure deployment to a resource group.</span></span> <span data-ttu-id="0eb5f-147"> (自動生成) </span><span class="sxs-lookup"><span data-stu-id="0eb5f-147">(autogenerated)</span></span>

<!-- Aladdin Generated Example -->


```powershell
New-AzResourceGroupDeployment -DeploymentDebugLogLevel RequestContent -Name mynewstorageaccount -ResourceGroupName 'ContosoEngineering' -TemplateFile 'D:\Azure\Templates\EngineeringSite.json' -TemplateParameterObject <Hashtable>
```

### <span data-ttu-id="0eb5f-148">範例4：使用 uri 和 SAS 權杖部署儲存在非公用儲存空間帳戶的範本</span><span class="sxs-lookup"><span data-stu-id="0eb5f-148">Example 4: Deploy a template stored in a non public storage account using a uri and SAS token</span></span>
```powershell
PS C:\> New-AzResourceGroupDeployment -ResourceGroupName "RGName" -TemplateUri "https://example.com/example.json" -QueryString "foo"
```
<span data-ttu-id="0eb5f-149">這個命令會使用 TemplateUri 中的範本來建立新的部署，該範本不是公開的，而且需要權杖參數才能使用 QueryString 參數來提供存取。</span><span class="sxs-lookup"><span data-stu-id="0eb5f-149">This command creates a new deployment using the template in TemplateUri which is not public and requires a token parameter to access which would be provided using the QueryString parameter.</span></span>
<span data-ttu-id="0eb5f-150">執行此命令可有效地使用 url 存取範本 https://example.com/example.json?foo 。</span><span class="sxs-lookup"><span data-stu-id="0eb5f-150">Running this command effectively accesses the template using the url https://example.com/example.json?foo.</span></span>
<span data-ttu-id="0eb5f-151">如果您想要在儲存空間帳戶中使用範本，只要將 SAS 權杖提供為 QueryString，就可以使用此功能。</span><span class="sxs-lookup"><span data-stu-id="0eb5f-151">This can be used if you want to use a template in a storage account by providing the SAS token as the QueryString</span></span>
## <span data-ttu-id="0eb5f-152">參數</span><span class="sxs-lookup"><span data-stu-id="0eb5f-152">PARAMETERS</span></span>

### <span data-ttu-id="0eb5f-153">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0eb5f-153">-AsJob</span></span>
<span data-ttu-id="0eb5f-154">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="0eb5f-154">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="0eb5f-155">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0eb5f-155">-DefaultProfile</span></span>
<span data-ttu-id="0eb5f-156">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="0eb5f-156">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0eb5f-157">-DeploymentDebugLogLevel</span><span class="sxs-lookup"><span data-stu-id="0eb5f-157">-DeploymentDebugLogLevel</span></span>
<span data-ttu-id="0eb5f-158">指定調試記錄層級。</span><span class="sxs-lookup"><span data-stu-id="0eb5f-158">Specifies a debug log level.</span></span>
<span data-ttu-id="0eb5f-159">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="0eb5f-159">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="0eb5f-160">RequestContent</span><span class="sxs-lookup"><span data-stu-id="0eb5f-160">RequestContent</span></span>
- <span data-ttu-id="0eb5f-161">ResponseContent</span><span class="sxs-lookup"><span data-stu-id="0eb5f-161">ResponseContent</span></span>
- <span data-ttu-id="0eb5f-162">同時</span><span class="sxs-lookup"><span data-stu-id="0eb5f-162">All</span></span>
- <span data-ttu-id="0eb5f-163">所有</span><span class="sxs-lookup"><span data-stu-id="0eb5f-163">None</span></span>

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

### <span data-ttu-id="0eb5f-164">-Force</span><span class="sxs-lookup"><span data-stu-id="0eb5f-164">-Force</span></span>
<span data-ttu-id="0eb5f-165">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="0eb5f-165">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="0eb5f-166">模式</span><span class="sxs-lookup"><span data-stu-id="0eb5f-166">-Mode</span></span>
<span data-ttu-id="0eb5f-167">指定部署模式。</span><span class="sxs-lookup"><span data-stu-id="0eb5f-167">Specifies the deployment mode.</span></span> <span data-ttu-id="0eb5f-168">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="0eb5f-168">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="0eb5f-169">完成：在完整模式中，資源管理員會刪除資源群組中存在但未在範本中指定的資源。</span><span class="sxs-lookup"><span data-stu-id="0eb5f-169">Complete: In complete mode, Resource Manager deletes resources that exist in the resource group but are not specified in the template.</span></span> 
- <span data-ttu-id="0eb5f-170">增量式：在增量模式中，資源管理器會保留資源群組中存在但未在範本中指定的未改動資源。</span><span class="sxs-lookup"><span data-stu-id="0eb5f-170">Incremental: In incremental mode, Resource Manager leaves unchanged resources that exist in the resource group but are not specified in the template.</span></span>

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

### <span data-ttu-id="0eb5f-171">-名稱</span><span class="sxs-lookup"><span data-stu-id="0eb5f-171">-Name</span></span>
<span data-ttu-id="0eb5f-172">將要建立之部署的名稱。</span><span class="sxs-lookup"><span data-stu-id="0eb5f-172">The name of the deployment it's going to create.</span></span> <span data-ttu-id="0eb5f-173">如果未指定，則預設為提供範本檔時的範本檔案名;預設為提供範本物件的目前時間（例如 "20131223140835"）。</span><span class="sxs-lookup"><span data-stu-id="0eb5f-173">If not specified, defaults to the template file name when a template file is provided; defaults to the current time when a template object is provided, e.g. "20131223140835".</span></span>

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

### <span data-ttu-id="0eb5f-174">-預先</span><span class="sxs-lookup"><span data-stu-id="0eb5f-174">-Pre</span></span>
<span data-ttu-id="0eb5f-175">表示此 Cmdlet 會在自動決定要使用哪個版本時，考慮預發行 API 版本。</span><span class="sxs-lookup"><span data-stu-id="0eb5f-175">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="0eb5f-176">-QueryString</span><span class="sxs-lookup"><span data-stu-id="0eb5f-176">-QueryString</span></span>
<span data-ttu-id="0eb5f-177">查詢字串 (例如，要與 TemplateUri 參數搭配使用的 SAS 權杖) 。</span><span class="sxs-lookup"><span data-stu-id="0eb5f-177">The query string (for example, a SAS token) to be used with the TemplateUri parameter.</span></span> <span data-ttu-id="0eb5f-178">會在連結範本時使用</span><span class="sxs-lookup"><span data-stu-id="0eb5f-178">Would be used in case of linked templates</span></span>

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

### <span data-ttu-id="0eb5f-179">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0eb5f-179">-ResourceGroupName</span></span>
<span data-ttu-id="0eb5f-180">指定要部署之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="0eb5f-180">Specifies the name of the resource group to deploy.</span></span>

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

### <span data-ttu-id="0eb5f-181">-RollBackDeploymentName</span><span class="sxs-lookup"><span data-stu-id="0eb5f-181">-RollBackDeploymentName</span></span>
<span data-ttu-id="0eb5f-182">如果使用了-RollbackToLastDeployment，則會使用資源群組中的指定名稱回滾到成功的部署。</span><span class="sxs-lookup"><span data-stu-id="0eb5f-182">Rollback to the successful deployment with the given name in the resource group, should not be used if -RollbackToLastDeployment is used.</span></span>

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

### <span data-ttu-id="0eb5f-183">-RollbackToLastDeployment</span><span class="sxs-lookup"><span data-stu-id="0eb5f-183">-RollbackToLastDeployment</span></span>
<span data-ttu-id="0eb5f-184">如果使用-RollBackDeploymentName，則回退至 [資源] 群組中的最後一個成功部署。</span><span class="sxs-lookup"><span data-stu-id="0eb5f-184">Rollback to the last successful deployment in the resource group, should not be present if -RollBackDeploymentName is used.</span></span>

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

### <span data-ttu-id="0eb5f-185">-SkipTemplateParameterPrompt</span><span class="sxs-lookup"><span data-stu-id="0eb5f-185">-SkipTemplateParameterPrompt</span></span>
<span data-ttu-id="0eb5f-186">會跳過 PowerShell 動態參數處理，檢查提供的範本參數是否包含範本所使用的所有必要參數。</span><span class="sxs-lookup"><span data-stu-id="0eb5f-186">Skips the PowerShell dynamic parameter processing that checks if the provided template parameter contains all necessary parameters used by the template.</span></span> <span data-ttu-id="0eb5f-187">這項檢查會提示使用者提供缺少參數的值，但提供-SkipTemplateParameterPrompt 將會在範本中發現未系結的參數時，立即忽略此提示和錯誤。</span><span class="sxs-lookup"><span data-stu-id="0eb5f-187">This check would prompt the user to provide a value for the missing parameters, but providing the -SkipTemplateParameterPrompt will ignore this prompt and error out immediately if a parameter was found not to be bound in the template.</span></span> <span data-ttu-id="0eb5f-188">在非互動式腳本中，您可以提供 SkipTemplateParameterPrompt，以在不符合所有必要參數的情況下，提供較佳的錯誤訊息。</span><span class="sxs-lookup"><span data-stu-id="0eb5f-188">For non-interactive scripts, -SkipTemplateParameterPrompt can be provided to provide a better error message in the case where not all required parameters are satisfied.</span></span>

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

### <span data-ttu-id="0eb5f-189">-Tag</span><span class="sxs-lookup"><span data-stu-id="0eb5f-189">-Tag</span></span>
<span data-ttu-id="0eb5f-190">要放在部署上的標記。</span><span class="sxs-lookup"><span data-stu-id="0eb5f-190">The tags to put on the deployment.</span></span>

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

### <span data-ttu-id="0eb5f-191">-TemplateFile</span><span class="sxs-lookup"><span data-stu-id="0eb5f-191">-TemplateFile</span></span>
<span data-ttu-id="0eb5f-192">指定 JSON 範本檔的完整路徑。</span><span class="sxs-lookup"><span data-stu-id="0eb5f-192">Specifies the full path of a JSON template file.</span></span>
<span data-ttu-id="0eb5f-193">這可以是一種已儲存為 JSON 檔案的自訂範本或圖庫範本，例如使用 **AzResourceGroupGalleryTemplate** Cmdlet 建立的檔。</span><span class="sxs-lookup"><span data-stu-id="0eb5f-193">This can be a custom template or a gallery template that is saved as a JSON file, such as one created by using the **Save-AzResourceGroupGalleryTemplate** cmdlet.</span></span>

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

### <span data-ttu-id="0eb5f-194">-TemplateObject</span><span class="sxs-lookup"><span data-stu-id="0eb5f-194">-TemplateObject</span></span>
<span data-ttu-id="0eb5f-195">代表範本的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="0eb5f-195">A hash table which represents the template.</span></span>

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

### <span data-ttu-id="0eb5f-196">-TemplateParameterFile</span><span class="sxs-lookup"><span data-stu-id="0eb5f-196">-TemplateParameterFile</span></span>
<span data-ttu-id="0eb5f-197">指定包含範本參數之名稱和值的 JSON 檔案的完整路徑。</span><span class="sxs-lookup"><span data-stu-id="0eb5f-197">Specifies the full path of a JSON file that contains the names and values of the template parameters.</span></span>
<span data-ttu-id="0eb5f-198">如果範本有參數，您必須使用 *TemplateParameterFile* 參數或 *TemplateParameterObject* 參數指定參數值。</span><span class="sxs-lookup"><span data-stu-id="0eb5f-198">If a template has parameters, you must specify the parameter values with the *TemplateParameterFile* parameter or the *TemplateParameterObject* parameter.</span></span>
<span data-ttu-id="0eb5f-199">當您指定範本時，範本參數會動態新增到命令中。</span><span class="sxs-lookup"><span data-stu-id="0eb5f-199">Template parameters are dynamically added to the command when you specify a template.</span></span>
<span data-ttu-id="0eb5f-200">若要使用動態參數，請輸入減號， ( ) 來指示參數名稱，然後使用 Tab 鍵來迴圈顯示可用的參數。</span><span class="sxs-lookup"><span data-stu-id="0eb5f-200">To use the dynamic parameters, type a minus sign (-) to indicate a parameter name and then use the Tab key to cycle through the available parameters.</span></span>

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

### <span data-ttu-id="0eb5f-201">-TemplateParameterObject</span><span class="sxs-lookup"><span data-stu-id="0eb5f-201">-TemplateParameterObject</span></span>
<span data-ttu-id="0eb5f-202">指定範本參數名稱和值的雜湊表。</span><span class="sxs-lookup"><span data-stu-id="0eb5f-202">Specifies a hash table of template parameter names and values.</span></span>
<span data-ttu-id="0eb5f-203">如需有關 Windows PowerShell 中的雜湊資料表的說明，請輸入 `Get-Help about_Hash_Tables` 。</span><span class="sxs-lookup"><span data-stu-id="0eb5f-203">For help with hash tables in Windows PowerShell, type `Get-Help about_Hash_Tables`.</span></span>
<span data-ttu-id="0eb5f-204">如果範本有參數，您必須指定參數值。</span><span class="sxs-lookup"><span data-stu-id="0eb5f-204">If a template has parameters, you must specify parameter values.</span></span>
<span data-ttu-id="0eb5f-205">當您指定範本時，範本參數會動態新增到命令中。</span><span class="sxs-lookup"><span data-stu-id="0eb5f-205">Template parameters are dynamically added to the command when you specify a template.</span></span>

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

### <span data-ttu-id="0eb5f-206">-TemplateParameterUri</span><span class="sxs-lookup"><span data-stu-id="0eb5f-206">-TemplateParameterUri</span></span>
<span data-ttu-id="0eb5f-207">指定範本參數檔的 URI。</span><span class="sxs-lookup"><span data-stu-id="0eb5f-207">Specifies the URI of a template parameters file.</span></span>

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

### <span data-ttu-id="0eb5f-208">-TemplateSpecId</span><span class="sxs-lookup"><span data-stu-id="0eb5f-208">-TemplateSpecId</span></span>
<span data-ttu-id="0eb5f-209">要部署之 templateSpec 的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="0eb5f-209">Resource ID of the templateSpec to be deployed.</span></span>

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

### <span data-ttu-id="0eb5f-210">-TemplateUri</span><span class="sxs-lookup"><span data-stu-id="0eb5f-210">-TemplateUri</span></span>
<span data-ttu-id="0eb5f-211">指定 JSON 範本檔案的 URI。</span><span class="sxs-lookup"><span data-stu-id="0eb5f-211">Specifies the URI of a JSON template file.</span></span>
<span data-ttu-id="0eb5f-212">此檔案可以是另一個儲存為 JSON 檔案的自訂範本或圖庫範本，例如使用 **AzResourceGroupGalleryTemplate**。</span><span class="sxs-lookup"><span data-stu-id="0eb5f-212">This file can be a custom template or a gallery template that is saved as a JSON file, such as by using **Save-AzResourceGroupGalleryTemplate**.</span></span>

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

### <span data-ttu-id="0eb5f-213">-WhatIfExcludeChangeType</span><span class="sxs-lookup"><span data-stu-id="0eb5f-213">-WhatIfExcludeChangeType</span></span>
<span data-ttu-id="0eb5f-214">要從 What-If 結果中排除的逗號分隔資源變更類型。</span><span class="sxs-lookup"><span data-stu-id="0eb5f-214">Comma-separated resource change types to be excluded from What-If results.</span></span> <span data-ttu-id="0eb5f-215">在設定了-WhatIf 或-Confirm 切換時適用。</span><span class="sxs-lookup"><span data-stu-id="0eb5f-215">Applicable when the -WhatIf or -Confirm switch is set.</span></span>

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

### <span data-ttu-id="0eb5f-216">-WhatIfResultFormat</span><span class="sxs-lookup"><span data-stu-id="0eb5f-216">-WhatIfResultFormat</span></span>
<span data-ttu-id="0eb5f-217">What-If 的結果格式。</span><span class="sxs-lookup"><span data-stu-id="0eb5f-217">The What-If result format.</span></span>

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

### <span data-ttu-id="0eb5f-218">-確認</span><span class="sxs-lookup"><span data-stu-id="0eb5f-218">-Confirm</span></span>
<span data-ttu-id="0eb5f-219">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="0eb5f-219">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0eb5f-220">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0eb5f-220">-WhatIf</span></span>
<span data-ttu-id="0eb5f-221">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="0eb5f-221">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0eb5f-222">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="0eb5f-222">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0eb5f-223">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0eb5f-223">CommonParameters</span></span>
<span data-ttu-id="0eb5f-224">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="0eb5f-224">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0eb5f-225">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="0eb5f-225">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0eb5f-226">輸入</span><span class="sxs-lookup"><span data-stu-id="0eb5f-226">INPUTS</span></span>

### <span data-ttu-id="0eb5f-227">System.object</span><span class="sxs-lookup"><span data-stu-id="0eb5f-227">System.String</span></span>

### <span data-ttu-id="0eb5f-228">DeploymentMode 中的 [管理]</span><span class="sxs-lookup"><span data-stu-id="0eb5f-228">Microsoft.Azure.Management.ResourceManager.Models.DeploymentMode</span></span>

### <span data-ttu-id="0eb5f-229">[System.object] 集合. Hashtable</span><span class="sxs-lookup"><span data-stu-id="0eb5f-229">System.Collections.Hashtable</span></span>

## <span data-ttu-id="0eb5f-230">輸出</span><span class="sxs-lookup"><span data-stu-id="0eb5f-230">OUTPUTS</span></span>

### <span data-ttu-id="0eb5f-231">PSResourceGroupDeployment 中的 SdkModels （）</span><span class="sxs-lookup"><span data-stu-id="0eb5f-231">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceGroupDeployment</span></span>

## <span data-ttu-id="0eb5f-232">筆記</span><span class="sxs-lookup"><span data-stu-id="0eb5f-232">NOTES</span></span>

## <span data-ttu-id="0eb5f-233">相關連結</span><span class="sxs-lookup"><span data-stu-id="0eb5f-233">RELATED LINKS</span></span>

[<span data-ttu-id="0eb5f-234">AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="0eb5f-234">Get-AzResourceGroupDeployment</span></span>](./Get-AzResourceGroupDeployment.md)

[<span data-ttu-id="0eb5f-235">新-AzResource</span><span class="sxs-lookup"><span data-stu-id="0eb5f-235">New-AzResource</span></span>](./New-AzResource.md)

[<span data-ttu-id="0eb5f-236">新-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="0eb5f-236">New-AzResourceGroup</span></span>](./New-AzResourceGroup.md)

[<span data-ttu-id="0eb5f-237">移除-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="0eb5f-237">Remove-AzResourceGroupDeployment</span></span>](./Remove-AzResourceGroupDeployment.md)

[<span data-ttu-id="0eb5f-238">停止 AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="0eb5f-238">Stop-AzResourceGroupDeployment</span></span>](./Stop-AzResourceGroupDeployment.md)

[<span data-ttu-id="0eb5f-239">Test-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="0eb5f-239">Test-AzResourceGroupDeployment</span></span>](./Test-AzResourceGroupDeployment.md)