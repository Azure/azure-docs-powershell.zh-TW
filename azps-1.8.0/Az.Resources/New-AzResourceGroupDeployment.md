---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 6E2F0D5E-E683-46F3-B48B-55C4864F3308
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-azresourcegroupdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzResourceGroupDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzResourceGroupDeployment.md
ms.openlocfilehash: 067faa4688f079d24f2fc79a4771c84f6c02d0c1
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93620822"
---
# <span data-ttu-id="45864-101">New-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="45864-101">New-AzResourceGroupDeployment</span></span>

## <span data-ttu-id="45864-102">摘要</span><span class="sxs-lookup"><span data-stu-id="45864-102">SYNOPSIS</span></span>
<span data-ttu-id="45864-103">新增 Azure 部署至資源群組。</span><span class="sxs-lookup"><span data-stu-id="45864-103">Adds an Azure deployment to a resource group.</span></span>

## <span data-ttu-id="45864-104">句法</span><span class="sxs-lookup"><span data-stu-id="45864-104">SYNTAX</span></span>

### <span data-ttu-id="45864-105">ByTemplateFileWithNoParameters (預設) </span><span class="sxs-lookup"><span data-stu-id="45864-105">ByTemplateFileWithNoParameters (Default)</span></span>
```
New-AzResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>] [-Force]
 [-AsJob] -TemplateFile <String> [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="45864-106">ByTemplateObjectAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="45864-106">ByTemplateObjectAndParameterObject</span></span>
```
New-AzResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>] [-Force]
 [-AsJob] -TemplateParameterObject <Hashtable> -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="45864-107">ByTemplateFileAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="45864-107">ByTemplateFileAndParameterObject</span></span>
```
New-AzResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>] [-Force]
 [-AsJob] -TemplateParameterObject <Hashtable> -TemplateFile <String> [-SkipTemplateParameterPrompt]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="45864-108">ByTemplateUriAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="45864-108">ByTemplateUriAndParameterObject</span></span>
```
New-AzResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>] [-Force]
 [-AsJob] -TemplateParameterObject <Hashtable> -TemplateUri <String> [-SkipTemplateParameterPrompt]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="45864-109">ByTemplateObjectAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="45864-109">ByTemplateObjectAndParameterFile</span></span>
```
New-AzResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>] [-Force]
 [-AsJob] -TemplateParameterFile <String> -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="45864-110">ByTemplateFileAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="45864-110">ByTemplateFileAndParameterFile</span></span>
```
New-AzResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>] [-Force]
 [-AsJob] -TemplateParameterFile <String> -TemplateFile <String> [-SkipTemplateParameterPrompt]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="45864-111">ByTemplateUriAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="45864-111">ByTemplateUriAndParameterFile</span></span>
```
New-AzResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>] [-Force]
 [-AsJob] -TemplateParameterFile <String> -TemplateUri <String> [-SkipTemplateParameterPrompt]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="45864-112">ByTemplateObjectAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="45864-112">ByTemplateObjectAndParameterUri</span></span>
```
New-AzResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>] [-Force]
 [-AsJob] -TemplateParameterUri <String> -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="45864-113">ByTemplateFileAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="45864-113">ByTemplateFileAndParameterUri</span></span>
```
New-AzResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>] [-Force]
 [-AsJob] -TemplateParameterUri <String> -TemplateFile <String> [-SkipTemplateParameterPrompt]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="45864-114">ByTemplateUriAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="45864-114">ByTemplateUriAndParameterUri</span></span>
```
New-AzResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>] [-Force]
 [-AsJob] -TemplateParameterUri <String> -TemplateUri <String> [-SkipTemplateParameterPrompt]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="45864-115">ByTemplateObjectWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="45864-115">ByTemplateObjectWithNoParameters</span></span>
```
New-AzResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>] [-Force]
 [-AsJob] -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="45864-116">ByTemplateUriWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="45864-116">ByTemplateUriWithNoParameters</span></span>
```
New-AzResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>] [-Force]
 [-AsJob] -TemplateUri <String> [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="45864-117">說明</span><span class="sxs-lookup"><span data-stu-id="45864-117">DESCRIPTION</span></span>
<span data-ttu-id="45864-118">**AzResourceGroupDeployment** Cmdlet 會將部署新增至現有的資源群組。</span><span class="sxs-lookup"><span data-stu-id="45864-118">The **New-AzResourceGroupDeployment** cmdlet adds a deployment to an existing resource group.</span></span>
<span data-ttu-id="45864-119">這包括部署所需的資源。</span><span class="sxs-lookup"><span data-stu-id="45864-119">This includes the resources that the deployment requires.</span></span>
<span data-ttu-id="45864-120">Azure 資源是使用者管理的 Azure 實體，例如資料庫伺服器、資料庫、網站、虛擬機器或儲存空間帳戶。</span><span class="sxs-lookup"><span data-stu-id="45864-120">An Azure resource is a user-managed Azure entity, such as a database server, database, website, virtual machine, or Storage account.</span></span>
<span data-ttu-id="45864-121">Azure 資源群組是一個以單位（例如網站、資料庫伺服器以及財務網站所需的資料庫）的形式來部署的 Azure 資源集合。</span><span class="sxs-lookup"><span data-stu-id="45864-121">An Azure resource group is a collection of Azure resources that are deployed as a unit, such as the website, database server, and databases that are required for a financial website.</span></span>
<span data-ttu-id="45864-122">資源群組部署使用範本將資源新增至資源群組，併發布資源，以便在 Azure 中使用它們。</span><span class="sxs-lookup"><span data-stu-id="45864-122">A resource group deployment uses a template to add resources to a resource group and publishes them so that they are available in Azure.</span></span>
<span data-ttu-id="45864-123">若要在不使用範本的情況下，將資源新增至資源群組，請使用 New-AzResource Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="45864-123">To add resources to a resource group without using a template, use the New-AzResource cmdlet.</span></span>
<span data-ttu-id="45864-124">若要新增資源群組部署，請指定現有資源群組和資源群組範本的名稱。</span><span class="sxs-lookup"><span data-stu-id="45864-124">To add a resource group deployment, specify the name of an existing resource group and a resource group template.</span></span>
<span data-ttu-id="45864-125">資源群組範本是一個 JSON 字串，代表複雜雲端服務（例如網頁入口網站）的資源群組。</span><span class="sxs-lookup"><span data-stu-id="45864-125">A resource group template is a JSON string that represents a resource group for a complex cloud-based service, such as a web portal.</span></span>
<span data-ttu-id="45864-126">範本包含必要資源的參數預留位置，以及可設定的屬性值，例如名稱和大小。</span><span class="sxs-lookup"><span data-stu-id="45864-126">The template includes parameter placeholders for required resources and configurable property values, such as names and sizes.</span></span>
<span data-ttu-id="45864-127">您可以在 Azure 範本庫中找到許多範本，或者您可以建立自己的範本。</span><span class="sxs-lookup"><span data-stu-id="45864-127">You can find many templates in the Azure template gallery or you can create your own templates.</span></span>
<span data-ttu-id="45864-128">您可以使用 **AzResourceGroupGalleryTemplate** Cmdlet 來尋找圖庫中的範本。</span><span class="sxs-lookup"><span data-stu-id="45864-128">You can use the **Get-AzResourceGroupGalleryTemplate** cmdlet to find a template in the gallery.</span></span>
<span data-ttu-id="45864-129">若要使用自訂範本來建立資源群組，請指定 *TemplateFile* 參數或 *TemplateUri* 參數。</span><span class="sxs-lookup"><span data-stu-id="45864-129">To use a custom template to create a resource group, specify the *TemplateFile* parameter or *TemplateUri* parameter.</span></span>
<span data-ttu-id="45864-130">每個範本都有可設定屬性的參數。</span><span class="sxs-lookup"><span data-stu-id="45864-130">Each template has parameters for configurable properties.</span></span>
<span data-ttu-id="45864-131">若要指定範本參數的值，請指定 *TemplateParameterFile* 參數或 *TemplateParameterObject* 參數。</span><span class="sxs-lookup"><span data-stu-id="45864-131">To specify values for the template parameters, specify the *TemplateParameterFile* parameter or the *TemplateParameterObject* parameter.</span></span>
<span data-ttu-id="45864-132">或者，您也可以使用在指定範本時動態新增到命令中的範本參數。</span><span class="sxs-lookup"><span data-stu-id="45864-132">Alternatively, you can use the template parameters that are dynamically added to the command when you specify a template.</span></span>
<span data-ttu-id="45864-133">若要使用動態參數，請在命令提示字元輸入，或輸入減號 ( ) 來指示參數，然後使用 Tab 鍵來迴圈顯示可用的參數。</span><span class="sxs-lookup"><span data-stu-id="45864-133">To use dynamic parameters, type them at the command prompt, or type a minus sign (-) to indicate a parameter and use the Tab key to cycle through available parameters.</span></span>
<span data-ttu-id="45864-134">您在命令提示字元中輸入的範本參數值會優先于範本參數物件或檔案中的值。</span><span class="sxs-lookup"><span data-stu-id="45864-134">Template parameter values that you enter at the command prompt take precedence over values in a template parameter object or file.</span></span>

## <span data-ttu-id="45864-135">示例</span><span class="sxs-lookup"><span data-stu-id="45864-135">EXAMPLES</span></span>

### <span data-ttu-id="45864-136">範例1：使用自訂範本和參數檔案建立部署</span><span class="sxs-lookup"><span data-stu-id="45864-136">Example 1: Use a custom template and parameter file to create a deployment</span></span>
```
PS C:\> New-AzResourceGroupDeployment -ResourceGroupName "ContosoEngineering" -TemplateFile "D:\Azure\Templates\EngineeringSite.json" -TemplateParameterFile "D:\Azure\Templates\EngSiteParms.json"
```

<span data-ttu-id="45864-137">這個命令會使用自訂範本與磁片上的範本檔案，建立新的部署。</span><span class="sxs-lookup"><span data-stu-id="45864-137">This command creates a new deployment by using a custom template and a template file on disk.</span></span>
<span data-ttu-id="45864-138">此命令會使用 *TemplateFile* 參數來指定範本和 *TemplateParameterFile* 參數，以指定包含參數和參數值的檔案。</span><span class="sxs-lookup"><span data-stu-id="45864-138">The command uses the *TemplateFile* parameter to specify the template and the *TemplateParameterFile* parameter to specify a file that contains parameters and parameter values.</span></span>

### <span data-ttu-id="45864-139">範例2：使用自訂範本物件與參數檔案建立部署</span><span class="sxs-lookup"><span data-stu-id="45864-139">Example 2: Use a custom template object and parameter file to create a deployment</span></span>
```
PS C:\> $TemplateFileText = [System.IO.File]::ReadAllText("D:\Azure\Templates\EngineeringSite.json")
PS C:\> $TemplateObject = ConvertFrom-Json $TemplateFileText -AsHashtable
PS C:\> New-AzResourceGroupDeployment -ResourceGroupName "ContosoEngineering" -TemplateObject $TemplateObject -TemplateParameterFile "D:\Azure\Templates\EngSiteParams.json"
```

<span data-ttu-id="45864-140">這個命令會在已轉換為記憶體中 hashtable 的磁片上使用自訂範本檔案，建立新的部署。</span><span class="sxs-lookup"><span data-stu-id="45864-140">This command creates a new deployment by using a custom and a template file on disk that has been converted to an in-memory hashtable.</span></span>
<span data-ttu-id="45864-141">前兩個命令會讀取磁片上範本檔案的文字，並將它轉換成記憶體中的 hashtable。</span><span class="sxs-lookup"><span data-stu-id="45864-141">The first two commands read the text for the template file on disk and convert it to an in-memory hashtable.</span></span>
<span data-ttu-id="45864-142">最後一個命令使用 *TemplateObject* 參數來指定 Hashtable 和 *TemplateParameterFile* 參數，以指定包含參數和參數值的檔案。</span><span class="sxs-lookup"><span data-stu-id="45864-142">The last command uses the *TemplateObject* parameter to specify the hashtable and the *TemplateParameterFile* parameter to specify a file that contains parameters and parameter values.</span></span>

## <span data-ttu-id="45864-143">參數</span><span class="sxs-lookup"><span data-stu-id="45864-143">PARAMETERS</span></span>

### <span data-ttu-id="45864-144">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="45864-144">-ApiVersion</span></span>
<span data-ttu-id="45864-145">指定資源提供者支援的 API 版本。</span><span class="sxs-lookup"><span data-stu-id="45864-145">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="45864-146">您可以指定不同于預設版本的版本。</span><span class="sxs-lookup"><span data-stu-id="45864-146">You can specify a different version than the default version.</span></span>

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

### <span data-ttu-id="45864-147">-AsJob</span><span class="sxs-lookup"><span data-stu-id="45864-147">-AsJob</span></span>
<span data-ttu-id="45864-148">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="45864-148">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="45864-149">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="45864-149">-DefaultProfile</span></span>
<span data-ttu-id="45864-150">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="45864-150">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="45864-151">-DeploymentDebugLogLevel</span><span class="sxs-lookup"><span data-stu-id="45864-151">-DeploymentDebugLogLevel</span></span>
<span data-ttu-id="45864-152">指定調試記錄層級。</span><span class="sxs-lookup"><span data-stu-id="45864-152">Specifies a debug log level.</span></span>
<span data-ttu-id="45864-153">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="45864-153">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="45864-154">RequestContent</span><span class="sxs-lookup"><span data-stu-id="45864-154">RequestContent</span></span>
- <span data-ttu-id="45864-155">ResponseContent</span><span class="sxs-lookup"><span data-stu-id="45864-155">ResponseContent</span></span>
- <span data-ttu-id="45864-156">同時</span><span class="sxs-lookup"><span data-stu-id="45864-156">All</span></span>
- <span data-ttu-id="45864-157">所有</span><span class="sxs-lookup"><span data-stu-id="45864-157">None</span></span>

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

### <span data-ttu-id="45864-158">-Force</span><span class="sxs-lookup"><span data-stu-id="45864-158">-Force</span></span>
<span data-ttu-id="45864-159">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="45864-159">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="45864-160">模式</span><span class="sxs-lookup"><span data-stu-id="45864-160">-Mode</span></span>
<span data-ttu-id="45864-161">指定部署模式。</span><span class="sxs-lookup"><span data-stu-id="45864-161">Specifies the deployment mode.</span></span> <span data-ttu-id="45864-162">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="45864-162">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="45864-163">完成：在完整模式中，資源管理員會刪除資源群組中存在但未在範本中指定的資源。</span><span class="sxs-lookup"><span data-stu-id="45864-163">Complete: In complete mode, Resource Manager deletes resources that exist in the resource group but are not specified in the template.</span></span> 
- <span data-ttu-id="45864-164">增量式：在增量模式中，資源管理器會保留資源群組中存在但未在範本中指定的未改動資源。</span><span class="sxs-lookup"><span data-stu-id="45864-164">Incremental: In incremental mode, Resource Manager leaves unchanged resources that exist in the resource group but are not specified in the template.</span></span>

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

### <span data-ttu-id="45864-165">-名稱</span><span class="sxs-lookup"><span data-stu-id="45864-165">-Name</span></span>
<span data-ttu-id="45864-166">指定要建立之資源群組部署的名稱。</span><span class="sxs-lookup"><span data-stu-id="45864-166">Specifies the name of the resource group deployment to create.</span></span>

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

### <span data-ttu-id="45864-167">-預先</span><span class="sxs-lookup"><span data-stu-id="45864-167">-Pre</span></span>
<span data-ttu-id="45864-168">表示此 Cmdlet 會在自動決定要使用哪個版本時，考慮預發行 API 版本。</span><span class="sxs-lookup"><span data-stu-id="45864-168">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="45864-169">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="45864-169">-ResourceGroupName</span></span>
<span data-ttu-id="45864-170">指定要部署之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="45864-170">Specifies the name of the resource group to deploy.</span></span>

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

### <span data-ttu-id="45864-171">-RollBackDeploymentName</span><span class="sxs-lookup"><span data-stu-id="45864-171">-RollBackDeploymentName</span></span>
<span data-ttu-id="45864-172">如果使用了-RollbackToLastDeployment，則會使用資源群組中的指定名稱回滾到成功的部署。</span><span class="sxs-lookup"><span data-stu-id="45864-172">Rollback to the successful deployment with the given name in the resource group, should not be used if -RollbackToLastDeployment is used.</span></span>

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

### <span data-ttu-id="45864-173">-RollbackToLastDeployment</span><span class="sxs-lookup"><span data-stu-id="45864-173">-RollbackToLastDeployment</span></span>
<span data-ttu-id="45864-174">如果使用-RollBackDeploymentName，則回退至 [資源] 群組中的最後一個成功部署。</span><span class="sxs-lookup"><span data-stu-id="45864-174">Rollback to the last successful deployment in the resource group, should not be present if -RollBackDeploymentName is used.</span></span>

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

### <span data-ttu-id="45864-175">-SkipTemplateParameterPrompt</span><span class="sxs-lookup"><span data-stu-id="45864-175">-SkipTemplateParameterPrompt</span></span>
<span data-ttu-id="45864-176">會跳過 PowerShell 動態參數處理，檢查提供的範本參數是否包含範本所使用的所有必要參數。</span><span class="sxs-lookup"><span data-stu-id="45864-176">Skips the PowerShell dynamic parameter processing that checks if the provided template parameter contains all necessary parameters used by the template.</span></span> <span data-ttu-id="45864-177">這項檢查會提示使用者提供缺少參數的值，但提供-SkipTemplateParameterPrompt 將會在範本中發現未系結的參數時，立即忽略此提示和錯誤。</span><span class="sxs-lookup"><span data-stu-id="45864-177">This check would prompt the user to provide a value for the missing parameters, but providing the -SkipTemplateParameterPrompt will ignore this prompt and error out immediately if a parameter was found not to be bound in the template.</span></span> <span data-ttu-id="45864-178">在非互動式腳本中，您可以提供 SkipTemplateParameterPrompt，以在不符合所有必要參數的情況下，提供較佳的錯誤訊息。</span><span class="sxs-lookup"><span data-stu-id="45864-178">For non-interactive scripts, -SkipTemplateParameterPrompt can be provided to provide a better error message in the case where not all required parameters are satisfied.</span></span>

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

### <span data-ttu-id="45864-179">-TemplateFile</span><span class="sxs-lookup"><span data-stu-id="45864-179">-TemplateFile</span></span>
<span data-ttu-id="45864-180">指定 JSON 範本檔的完整路徑。</span><span class="sxs-lookup"><span data-stu-id="45864-180">Specifies the full path of a JSON template file.</span></span>
<span data-ttu-id="45864-181">這可以是一種已儲存為 JSON 檔案的自訂範本或圖庫範本，例如使用 **AzResourceGroupGalleryTemplate** Cmdlet 建立的檔。</span><span class="sxs-lookup"><span data-stu-id="45864-181">This can be a custom template or a gallery template that is saved as a JSON file, such as one created by using the **Save-AzResourceGroupGalleryTemplate** cmdlet.</span></span>

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

### <span data-ttu-id="45864-182">-TemplateObject</span><span class="sxs-lookup"><span data-stu-id="45864-182">-TemplateObject</span></span>
<span data-ttu-id="45864-183">代表範本的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="45864-183">A hash table which represents the template.</span></span>

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

### <span data-ttu-id="45864-184">-TemplateParameterFile</span><span class="sxs-lookup"><span data-stu-id="45864-184">-TemplateParameterFile</span></span>
<span data-ttu-id="45864-185">指定包含範本參數之名稱和值的 JSON 檔案的完整路徑。</span><span class="sxs-lookup"><span data-stu-id="45864-185">Specifies the full path of a JSON file that contains the names and values of the template parameters.</span></span>
<span data-ttu-id="45864-186">如果範本有參數，您必須使用 *TemplateParameterFile* 參數或 *TemplateParameterObject* 參數指定參數值。</span><span class="sxs-lookup"><span data-stu-id="45864-186">If a template has parameters, you must specify the parameter values with the *TemplateParameterFile* parameter or the *TemplateParameterObject* parameter.</span></span>
<span data-ttu-id="45864-187">當您指定範本時，範本參數會動態新增到命令中。</span><span class="sxs-lookup"><span data-stu-id="45864-187">Template parameters are dynamically added to the command when you specify a template.</span></span>
<span data-ttu-id="45864-188">若要使用動態參數，請輸入減號， ( ) 來指示參數名稱，然後使用 Tab 鍵來迴圈顯示可用的參數。</span><span class="sxs-lookup"><span data-stu-id="45864-188">To use the dynamic parameters, type a minus sign (-) to indicate a parameter name and then use the Tab key to cycle through the available parameters.</span></span>

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

### <span data-ttu-id="45864-189">-TemplateParameterObject</span><span class="sxs-lookup"><span data-stu-id="45864-189">-TemplateParameterObject</span></span>
<span data-ttu-id="45864-190">指定範本參數名稱和值的雜湊表。</span><span class="sxs-lookup"><span data-stu-id="45864-190">Specifies a hash table of template parameter names and values.</span></span>
<span data-ttu-id="45864-191">如需有關 Windows PowerShell 中的雜湊資料表的說明，請輸入 `Get-Help about_Hash_Tables` 。</span><span class="sxs-lookup"><span data-stu-id="45864-191">For help with hash tables in Windows PowerShell, type `Get-Help about_Hash_Tables`.</span></span>
<span data-ttu-id="45864-192">如果範本有參數，您必須指定參數值。</span><span class="sxs-lookup"><span data-stu-id="45864-192">If a template has parameters, you must specify parameter values.</span></span>
<span data-ttu-id="45864-193">當您指定範本時，範本參數會動態新增到命令中。</span><span class="sxs-lookup"><span data-stu-id="45864-193">Template parameters are dynamically added to the command when you specify a template.</span></span>

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

### <span data-ttu-id="45864-194">-TemplateParameterUri</span><span class="sxs-lookup"><span data-stu-id="45864-194">-TemplateParameterUri</span></span>
<span data-ttu-id="45864-195">指定範本參數檔的 URI。</span><span class="sxs-lookup"><span data-stu-id="45864-195">Specifies the URI of a template parameters file.</span></span>

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

### <span data-ttu-id="45864-196">-TemplateUri</span><span class="sxs-lookup"><span data-stu-id="45864-196">-TemplateUri</span></span>
<span data-ttu-id="45864-197">指定 JSON 範本檔案的 URI。</span><span class="sxs-lookup"><span data-stu-id="45864-197">Specifies the URI of a JSON template file.</span></span>
<span data-ttu-id="45864-198">此檔案可以是另一個儲存為 JSON 檔案的自訂範本或圖庫範本，例如使用 **AzResourceGroupGalleryTemplate** 。</span><span class="sxs-lookup"><span data-stu-id="45864-198">This file can be a custom template or a gallery template that is saved as a JSON file, such as by using **Save-AzResourceGroupGalleryTemplate**.</span></span>

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

### <span data-ttu-id="45864-199">-確認</span><span class="sxs-lookup"><span data-stu-id="45864-199">-Confirm</span></span>
<span data-ttu-id="45864-200">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="45864-200">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="45864-201">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="45864-201">-WhatIf</span></span>
<span data-ttu-id="45864-202">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="45864-202">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="45864-203">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="45864-203">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="45864-204">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="45864-204">CommonParameters</span></span>
<span data-ttu-id="45864-205">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="45864-205">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="45864-206">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="45864-206">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="45864-207">輸入</span><span class="sxs-lookup"><span data-stu-id="45864-207">INPUTS</span></span>

### <span data-ttu-id="45864-208">System.object</span><span class="sxs-lookup"><span data-stu-id="45864-208">System.String</span></span>

### <span data-ttu-id="45864-209">DeploymentMode 中的 [管理]</span><span class="sxs-lookup"><span data-stu-id="45864-209">Microsoft.Azure.Management.ResourceManager.Models.DeploymentMode</span></span>

### <span data-ttu-id="45864-210">[System.object] 集合. Hashtable</span><span class="sxs-lookup"><span data-stu-id="45864-210">System.Collections.Hashtable</span></span>

## <span data-ttu-id="45864-211">輸出</span><span class="sxs-lookup"><span data-stu-id="45864-211">OUTPUTS</span></span>

### <span data-ttu-id="45864-212">PSResourceGroupDeployment 中的 SdkModels （）</span><span class="sxs-lookup"><span data-stu-id="45864-212">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceGroupDeployment</span></span>

## <span data-ttu-id="45864-213">筆記</span><span class="sxs-lookup"><span data-stu-id="45864-213">NOTES</span></span>

## <span data-ttu-id="45864-214">相關連結</span><span class="sxs-lookup"><span data-stu-id="45864-214">RELATED LINKS</span></span>

[<span data-ttu-id="45864-215">AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="45864-215">Get-AzResourceGroupDeployment</span></span>](./Get-AzResourceGroupDeployment.md)

[<span data-ttu-id="45864-216">新-AzResource</span><span class="sxs-lookup"><span data-stu-id="45864-216">New-AzResource</span></span>](./New-AzResource.md)

[<span data-ttu-id="45864-217">新-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="45864-217">New-AzResourceGroup</span></span>](./New-AzResourceGroup.md)

[<span data-ttu-id="45864-218">移除-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="45864-218">Remove-AzResourceGroupDeployment</span></span>](./Remove-AzResourceGroupDeployment.md)

[<span data-ttu-id="45864-219">停止 AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="45864-219">Stop-AzResourceGroupDeployment</span></span>](./Stop-AzResourceGroupDeployment.md)

[<span data-ttu-id="45864-220">Test-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="45864-220">Test-AzResourceGroupDeployment</span></span>](./Test-AzResourceGroupDeployment.md)


