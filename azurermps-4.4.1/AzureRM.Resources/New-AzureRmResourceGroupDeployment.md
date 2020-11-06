---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 6E2F0D5E-E683-46F3-B48B-55C4864F3308
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmResourceGroupDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmResourceGroupDeployment.md
ms.openlocfilehash: 9512a8ae8e6bbd54704212539ad0650797cf4604
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93452395"
---
# <span data-ttu-id="f3cba-101">New-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="f3cba-101">New-AzureRmResourceGroupDeployment</span></span>

## <span data-ttu-id="f3cba-102">摘要</span><span class="sxs-lookup"><span data-stu-id="f3cba-102">SYNOPSIS</span></span>
<span data-ttu-id="f3cba-103">新增 Azure 部署至資源群組。</span><span class="sxs-lookup"><span data-stu-id="f3cba-103">Adds an Azure deployment to a resource group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f3cba-104">句法</span><span class="sxs-lookup"><span data-stu-id="f3cba-104">SYNTAX</span></span>

### <span data-ttu-id="f3cba-105">透過不含參數的範本檔案進行部署 (預設) </span><span class="sxs-lookup"><span data-stu-id="f3cba-105">Deployment via template file without parameters (Default)</span></span>
```
New-AzureRmResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-Force] -TemplateFile <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f3cba-106">透過 [範本檔案] 和 [範本參數] 物件進行部署</span><span class="sxs-lookup"><span data-stu-id="f3cba-106">Deployment via template file and template parameters object</span></span>
```
New-AzureRmResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-Force] -TemplateParameterObject <Hashtable> -TemplateFile <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f3cba-107">透過範本 uri 與範本參數物件進行部署</span><span class="sxs-lookup"><span data-stu-id="f3cba-107">Deployment via template uri and template parameters object</span></span>
```
New-AzureRmResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-Force] -TemplateParameterObject <Hashtable> -TemplateUri <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f3cba-108">透過範本檔案和範本參數檔案進行部署</span><span class="sxs-lookup"><span data-stu-id="f3cba-108">Deployment via template file and template parameters file</span></span>
```
New-AzureRmResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-Force] -TemplateParameterFile <String> -TemplateFile <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f3cba-109">透過範本 uri 與範本參數檔進行部署</span><span class="sxs-lookup"><span data-stu-id="f3cba-109">Deployment via template uri and template parameters file</span></span>
```
New-AzureRmResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-Force] -TemplateParameterFile <String> -TemplateUri <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f3cba-110">透過範本檔案範本參數 uri 進行部署</span><span class="sxs-lookup"><span data-stu-id="f3cba-110">Deployment via template file template parameters uri</span></span>
```
New-AzureRmResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-Force] -TemplateParameterUri <String> -TemplateFile <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f3cba-111">透過範本 uri 與範本參數 uri 進行部署</span><span class="sxs-lookup"><span data-stu-id="f3cba-111">Deployment via template uri and template parameters uri</span></span>
```
New-AzureRmResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-Force] -TemplateParameterUri <String> -TemplateUri <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f3cba-112">透過不含參數的範本 uri 進行部署</span><span class="sxs-lookup"><span data-stu-id="f3cba-112">Deployment via template uri without parameters</span></span>
```
New-AzureRmResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-Force] -TemplateUri <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f3cba-113">說明</span><span class="sxs-lookup"><span data-stu-id="f3cba-113">DESCRIPTION</span></span>
<span data-ttu-id="f3cba-114">**AzureRmResourceGroupDeployment** Cmdlet 會將部署新增至現有的資源群組。</span><span class="sxs-lookup"><span data-stu-id="f3cba-114">The **New-AzureRmResourceGroupDeployment** cmdlet adds a deployment to an existing resource group.</span></span>
<span data-ttu-id="f3cba-115">這包括部署所需的資源。</span><span class="sxs-lookup"><span data-stu-id="f3cba-115">This includes the resources that the deployment requires.</span></span>

<span data-ttu-id="f3cba-116">Azure 資源是使用者管理的 Azure 實體，例如資料庫伺服器、資料庫、網站、虛擬機器或儲存空間帳戶。</span><span class="sxs-lookup"><span data-stu-id="f3cba-116">An Azure resource is a user-managed Azure entity, such as a database server, database, website, virtual machine, or Storage account.</span></span>
<span data-ttu-id="f3cba-117">Azure 資源群組是一個以單位（例如網站、資料庫伺服器以及財務網站所需的資料庫）的形式來部署的 Azure 資源集合。</span><span class="sxs-lookup"><span data-stu-id="f3cba-117">An Azure resource group is a collection of Azure resources that are deployed as a unit, such as the website, database server, and databases that are required for a financial website.</span></span>
<span data-ttu-id="f3cba-118">資源群組部署使用範本將資源新增至資源群組，併發布資源，以便在 Azure 中使用它們。</span><span class="sxs-lookup"><span data-stu-id="f3cba-118">A resource group deployment uses a template to add resources to a resource group and publishes them so that they are available in Azure.</span></span>
<span data-ttu-id="f3cba-119">若要在不使用範本的情況下，將資源新增至資源群組，請使用 New-AzureRmResource Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="f3cba-119">To add resources to a resource group without using a template, use the New-AzureRmResource cmdlet.</span></span>

<span data-ttu-id="f3cba-120">若要新增資源群組部署，請指定現有資源群組和資源群組範本的名稱。</span><span class="sxs-lookup"><span data-stu-id="f3cba-120">To add a resource group deployment, specify the name of an existing resource group and a resource group template.</span></span>
<span data-ttu-id="f3cba-121">資源群組範本是一個 JSON 字串，代表複雜雲端服務（例如網頁入口網站）的資源群組。</span><span class="sxs-lookup"><span data-stu-id="f3cba-121">A resource group template is a JSON string that represents a resource group for a complex cloud-based service, such as a web portal.</span></span>
<span data-ttu-id="f3cba-122">範本包含必要資源的參數預留位置，以及可設定的屬性值，例如名稱和大小。</span><span class="sxs-lookup"><span data-stu-id="f3cba-122">The template includes parameter placeholders for required resources and configurable property values, such as names and sizes.</span></span>
<span data-ttu-id="f3cba-123">您可以在 Azure 範本庫中找到許多範本，或者您可以建立自己的範本。</span><span class="sxs-lookup"><span data-stu-id="f3cba-123">You can find many templates in the Azure template gallery or you can create your own templates.</span></span>
<span data-ttu-id="f3cba-124">您可以使用 **AzureRmResourceGroupGalleryTemplate** Cmdlet 來尋找圖庫中的範本。</span><span class="sxs-lookup"><span data-stu-id="f3cba-124">You can use the **Get-AzureRmResourceGroupGalleryTemplate** cmdlet to find a template in the gallery.</span></span>

<span data-ttu-id="f3cba-125">若要使用自訂範本來建立資源群組，請指定 *TemplateFile* 參數或 *TemplateUri* 參數。</span><span class="sxs-lookup"><span data-stu-id="f3cba-125">To use a custom template to create a resource group, specify the *TemplateFile* parameter or *TemplateUri* parameter.</span></span>
<span data-ttu-id="f3cba-126">每個範本都有可設定屬性的參數。</span><span class="sxs-lookup"><span data-stu-id="f3cba-126">Each template has parameters for configurable properties.</span></span>
<span data-ttu-id="f3cba-127">若要指定範本參數的值，請指定 *TemplateParameterFile* 參數或 *TemplateParameterObject* 參數。</span><span class="sxs-lookup"><span data-stu-id="f3cba-127">To specify values for the template parameters, specify the *TemplateParameterFile* parameter or the *TemplateParameterObject* parameter.</span></span>
<span data-ttu-id="f3cba-128">或者，您也可以使用在指定範本時動態新增到命令中的範本參數。</span><span class="sxs-lookup"><span data-stu-id="f3cba-128">Alternatively, you can use the template parameters that are dynamically added to the command when you specify a template.</span></span>
<span data-ttu-id="f3cba-129">若要使用動態參數，請在命令提示字元輸入，或輸入減號 ( ) 來指示參數，然後使用 Tab 鍵來迴圈顯示可用的參數。</span><span class="sxs-lookup"><span data-stu-id="f3cba-129">To use dynamic parameters, type them at the command prompt, or type a minus sign (-) to indicate a parameter and use the Tab key to cycle through available parameters.</span></span>
<span data-ttu-id="f3cba-130">您在命令提示字元中輸入的範本參數值會優先于範本參數物件或檔案中的值。</span><span class="sxs-lookup"><span data-stu-id="f3cba-130">Template parameter values that you enter at the command prompt take precedence over values in a template parameter object or file.</span></span>

## <span data-ttu-id="f3cba-131">示例</span><span class="sxs-lookup"><span data-stu-id="f3cba-131">EXAMPLES</span></span>

### <span data-ttu-id="f3cba-132">範例1：使用自訂範本和參數檔案建立部署</span><span class="sxs-lookup"><span data-stu-id="f3cba-132">Example 1: Use a custom template and parameter file to create a deployment</span></span>
```
PS C:\>New-AzureRmResourceGroupDeployment -ResourceGroupName "ContosoEngineering" -TemplateFile "D:\Azure\Templates\EngineeringSite.json" -TemplateParameterFile "D:\Azure\Templates\EngSiteParms.json" -TemplateVersion "2.1"
```

<span data-ttu-id="f3cba-133">這個命令會使用自訂範本與磁片上的範本檔案，建立新的部署。</span><span class="sxs-lookup"><span data-stu-id="f3cba-133">This command creates a new deployment by using a custom template and a template file on disk.</span></span>
<span data-ttu-id="f3cba-134">此命令會使用 *TemplateFile* 參數來指定範本和 *TemplateParameterFile* 參數，以指定包含參數和參數值的檔案。</span><span class="sxs-lookup"><span data-stu-id="f3cba-134">The command uses the *TemplateFile* parameter to specify the template and the *TemplateParameterFile* parameter to specify a file that contains parameters and parameter values.</span></span>
<span data-ttu-id="f3cba-135">它會使用 *TemplateVersion* 參數來指定範本版本。</span><span class="sxs-lookup"><span data-stu-id="f3cba-135">It uses the *TemplateVersion* parameter to specify the version of the template.</span></span>

## <span data-ttu-id="f3cba-136">參數</span><span class="sxs-lookup"><span data-stu-id="f3cba-136">PARAMETERS</span></span>

### <span data-ttu-id="f3cba-137">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="f3cba-137">-ApiVersion</span></span>
<span data-ttu-id="f3cba-138">指定資源提供者支援的 API 版本。</span><span class="sxs-lookup"><span data-stu-id="f3cba-138">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="f3cba-139">您可以指定不同于預設版本的版本。</span><span class="sxs-lookup"><span data-stu-id="f3cba-139">You can specify a different version than the default version.</span></span>

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

### <span data-ttu-id="f3cba-140">-DeploymentDebugLogLevel</span><span class="sxs-lookup"><span data-stu-id="f3cba-140">-DeploymentDebugLogLevel</span></span>
<span data-ttu-id="f3cba-141">指定調試記錄層級。</span><span class="sxs-lookup"><span data-stu-id="f3cba-141">Specifies a debug log level.</span></span>
<span data-ttu-id="f3cba-142">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="f3cba-142">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="f3cba-143">RequestContent</span><span class="sxs-lookup"><span data-stu-id="f3cba-143">RequestContent</span></span> 
- <span data-ttu-id="f3cba-144">ResponseContent</span><span class="sxs-lookup"><span data-stu-id="f3cba-144">ResponseContent</span></span> 
- <span data-ttu-id="f3cba-145">同時</span><span class="sxs-lookup"><span data-stu-id="f3cba-145">All</span></span> 
- <span data-ttu-id="f3cba-146">所有</span><span class="sxs-lookup"><span data-stu-id="f3cba-146">None</span></span>

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

### <span data-ttu-id="f3cba-147">-Force</span><span class="sxs-lookup"><span data-stu-id="f3cba-147">-Force</span></span>
<span data-ttu-id="f3cba-148">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="f3cba-148">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="f3cba-149">模式</span><span class="sxs-lookup"><span data-stu-id="f3cba-149">-Mode</span></span>
<span data-ttu-id="f3cba-150">指定部署模式。</span><span class="sxs-lookup"><span data-stu-id="f3cba-150">Specifies the deployment mode.</span></span> <span data-ttu-id="f3cba-151">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="f3cba-151">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="f3cba-152">完備</span><span class="sxs-lookup"><span data-stu-id="f3cba-152">Complete</span></span> 
- <span data-ttu-id="f3cba-153">少量</span><span class="sxs-lookup"><span data-stu-id="f3cba-153">Incremental</span></span>

```yaml
Type: Microsoft.Azure.Management.ResourceManager.Models.DeploymentMode
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: Incremental
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f3cba-154">-名稱</span><span class="sxs-lookup"><span data-stu-id="f3cba-154">-Name</span></span>
<span data-ttu-id="f3cba-155">指定要建立之資源群組部署的名稱。</span><span class="sxs-lookup"><span data-stu-id="f3cba-155">Specifies the name of the resource group deployment to create.</span></span>

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

### <span data-ttu-id="f3cba-156">-預先</span><span class="sxs-lookup"><span data-stu-id="f3cba-156">-Pre</span></span>
<span data-ttu-id="f3cba-157">表示此 Cmdlet 會在自動決定要使用哪個版本時，考慮預發行 API 版本。</span><span class="sxs-lookup"><span data-stu-id="f3cba-157">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="f3cba-158">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f3cba-158">-ResourceGroupName</span></span>
<span data-ttu-id="f3cba-159">指定要部署之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="f3cba-159">Specifies the name of the resource group to deploy.</span></span>

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

### <span data-ttu-id="f3cba-160">-TemplateFile</span><span class="sxs-lookup"><span data-stu-id="f3cba-160">-TemplateFile</span></span>
<span data-ttu-id="f3cba-161">指定 JSON 範本檔的完整路徑。</span><span class="sxs-lookup"><span data-stu-id="f3cba-161">Specifies the full path of a JSON template file.</span></span>
<span data-ttu-id="f3cba-162">這可以是一種已儲存為 JSON 檔案的自訂範本或圖庫範本，例如使用 **AzureRmResourceGroupGalleryTemplate** Cmdlet 建立的檔。</span><span class="sxs-lookup"><span data-stu-id="f3cba-162">This can be a custom template or a gallery template that is saved as a JSON file, such as one created by using the **Save-AzureRmResourceGroupGalleryTemplate** cmdlet.</span></span>

```yaml
Type: System.String
Parameter Sets: Deployment via template file without parameters, Deployment via template file and template parameters object, Deployment via template file and template parameters file, Deployment via template file template parameters uri
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f3cba-163">-TemplateParameterFile</span><span class="sxs-lookup"><span data-stu-id="f3cba-163">-TemplateParameterFile</span></span>
<span data-ttu-id="f3cba-164">指定包含範本參數之名稱和值的 JSON 檔案的完整路徑。</span><span class="sxs-lookup"><span data-stu-id="f3cba-164">Specifies the full path of a JSON file that contains the names and values of the template parameters.</span></span>
<span data-ttu-id="f3cba-165">如果範本有參數，您必須使用 *TemplateParameterFile* 參數或 *TemplateParameterObject* 參數指定參數值。</span><span class="sxs-lookup"><span data-stu-id="f3cba-165">If a template has parameters, you must specify the parameter values with the *TemplateParameterFile* parameter or the *TemplateParameterObject* parameter.</span></span>
<span data-ttu-id="f3cba-166">當您指定範本時，範本參數會動態新增到命令中。</span><span class="sxs-lookup"><span data-stu-id="f3cba-166">Template parameters are dynamically added to the command when you specify a template.</span></span>

<span data-ttu-id="f3cba-167">若要使用動態參數，請輸入減號， ( ) 來指示參數名稱，然後使用 Tab 鍵來迴圈顯示可用的參數。</span><span class="sxs-lookup"><span data-stu-id="f3cba-167">To use the dynamic parameters, type a minus sign (-) to indicate a parameter name and then use the Tab key to cycle through the available parameters.</span></span>

```yaml
Type: System.String
Parameter Sets: Deployment via template file and template parameters file, Deployment via template uri and template parameters file
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f3cba-168">-TemplateParameterObject</span><span class="sxs-lookup"><span data-stu-id="f3cba-168">-TemplateParameterObject</span></span>
<span data-ttu-id="f3cba-169">指定範本參數名稱和值的雜湊表。</span><span class="sxs-lookup"><span data-stu-id="f3cba-169">Specifies a hash table of template parameter names and values.</span></span>
<span data-ttu-id="f3cba-170">如需有關 Windows PowerShell 中的雜湊資料表的說明，請輸入 `Get-Help about_Hash_Tables` 。</span><span class="sxs-lookup"><span data-stu-id="f3cba-170">For help with hash tables in Windows PowerShell, type `Get-Help about_Hash_Tables`.</span></span>
<span data-ttu-id="f3cba-171">如果範本有參數，您必須指定參數值。</span><span class="sxs-lookup"><span data-stu-id="f3cba-171">If a template has parameters, you must specify parameter values.</span></span>
<span data-ttu-id="f3cba-172">當您指定範本時，範本參數會動態新增到命令中。</span><span class="sxs-lookup"><span data-stu-id="f3cba-172">Template parameters are dynamically added to the command when you specify a template.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: Deployment via template file and template parameters object, Deployment via template uri and template parameters object
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f3cba-173">-TemplateParameterUri</span><span class="sxs-lookup"><span data-stu-id="f3cba-173">-TemplateParameterUri</span></span>
<span data-ttu-id="f3cba-174">指定範本參數檔的 URI。</span><span class="sxs-lookup"><span data-stu-id="f3cba-174">Specifies the URI of a template parameters file.</span></span>

```yaml
Type: System.String
Parameter Sets: Deployment via template file template parameters uri, Deployment via template uri and template parameters uri
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f3cba-175">-TemplateUri</span><span class="sxs-lookup"><span data-stu-id="f3cba-175">-TemplateUri</span></span>
<span data-ttu-id="f3cba-176">指定 JSON 範本檔案的 URI。</span><span class="sxs-lookup"><span data-stu-id="f3cba-176">Specifies the URI of a JSON template file.</span></span>
<span data-ttu-id="f3cba-177">此檔案可以是另一個儲存為 JSON 檔案的自訂範本或圖庫範本，例如使用 **AzureRmResourceGroupGalleryTemplate** 。</span><span class="sxs-lookup"><span data-stu-id="f3cba-177">This file can be a custom template or a gallery template that is saved as a JSON file, such as by using **Save-AzureRmResourceGroupGalleryTemplate**.</span></span>

```yaml
Type: System.String
Parameter Sets: Deployment via template uri and template parameters object, Deployment via template uri and template parameters file, Deployment via template uri and template parameters uri, Deployment via template uri without parameters
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f3cba-178">-確認</span><span class="sxs-lookup"><span data-stu-id="f3cba-178">-Confirm</span></span>
<span data-ttu-id="f3cba-179">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="f3cba-179">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f3cba-180">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f3cba-180">-WhatIf</span></span>
<span data-ttu-id="f3cba-181">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="f3cba-181">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f3cba-182">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="f3cba-182">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f3cba-183">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f3cba-183">-DefaultProfile</span></span>
<span data-ttu-id="f3cba-184">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="f3cba-184">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f3cba-185">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f3cba-185">CommonParameters</span></span>
<span data-ttu-id="f3cba-186">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="f3cba-186">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f3cba-187">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="f3cba-187">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f3cba-188">輸入</span><span class="sxs-lookup"><span data-stu-id="f3cba-188">INPUTS</span></span>

### <span data-ttu-id="f3cba-189">所有</span><span class="sxs-lookup"><span data-stu-id="f3cba-189">None</span></span>

## <span data-ttu-id="f3cba-190">輸出</span><span class="sxs-lookup"><span data-stu-id="f3cba-190">OUTPUTS</span></span>

### <span data-ttu-id="f3cba-191">PSResourceGroupDeployment 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="f3cba-191">Microsoft.Azure.Commands.ResourceManager.Models.PSResourceGroupDeployment</span></span>

## <span data-ttu-id="f3cba-192">筆記</span><span class="sxs-lookup"><span data-stu-id="f3cba-192">NOTES</span></span>

## <span data-ttu-id="f3cba-193">相關連結</span><span class="sxs-lookup"><span data-stu-id="f3cba-193">RELATED LINKS</span></span>

[<span data-ttu-id="f3cba-194">AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="f3cba-194">Get-AzureRmResourceGroupDeployment</span></span>](./Get-AzureRmResourceGroupDeployment.md)

[<span data-ttu-id="f3cba-195">新-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="f3cba-195">New-AzureRmResource</span></span>](./New-AzureRmResource.md)

[<span data-ttu-id="f3cba-196">新-AzureRmResourceGroup</span><span class="sxs-lookup"><span data-stu-id="f3cba-196">New-AzureRmResourceGroup</span></span>](./New-AzureRmResourceGroup.md)

[<span data-ttu-id="f3cba-197">移除-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="f3cba-197">Remove-AzureRmResourceGroupDeployment</span></span>](./Remove-AzureRmResourceGroupDeployment.md)

[<span data-ttu-id="f3cba-198">停止 AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="f3cba-198">Stop-AzureRmResourceGroupDeployment</span></span>](./Stop-AzureRmResourceGroupDeployment.md)

[<span data-ttu-id="f3cba-199">Test-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="f3cba-199">Test-AzureRmResourceGroupDeployment</span></span>](./Test-AzureRmResourceGroupDeployment.md)


