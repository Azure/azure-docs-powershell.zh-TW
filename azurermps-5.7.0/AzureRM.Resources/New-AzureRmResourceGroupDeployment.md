---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 6E2F0D5E-E683-46F3-B48B-55C4864F3308
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/new-azurermresourcegroupdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmResourceGroupDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmResourceGroupDeployment.md
ms.openlocfilehash: 514d1257d917dc1bbf20f93d05236af9f36bd832
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93447674"
---
# <span data-ttu-id="f20b8-101">New-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="f20b8-101">New-AzureRmResourceGroupDeployment</span></span>

## <span data-ttu-id="f20b8-102">摘要</span><span class="sxs-lookup"><span data-stu-id="f20b8-102">SYNOPSIS</span></span>
<span data-ttu-id="f20b8-103">新增 Azure 部署至資源群組。</span><span class="sxs-lookup"><span data-stu-id="f20b8-103">Adds an Azure deployment to a resource group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f20b8-104">句法</span><span class="sxs-lookup"><span data-stu-id="f20b8-104">SYNTAX</span></span>

### <span data-ttu-id="f20b8-105">ByTemplateFileWithNoParameters (預設) </span><span class="sxs-lookup"><span data-stu-id="f20b8-105">ByTemplateFileWithNoParameters (Default)</span></span>
```
New-AzureRmResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-Force] [-AsJob] -TemplateFile <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f20b8-106">ByTemplateFileAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="f20b8-106">ByTemplateFileAndParameterObject</span></span>
```
New-AzureRmResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-Force] [-AsJob] -TemplateParameterObject <Hashtable>
 -TemplateFile <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f20b8-107">ByTemplateUriAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="f20b8-107">ByTemplateUriAndParameterObject</span></span>
```
New-AzureRmResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-Force] [-AsJob] -TemplateParameterObject <Hashtable>
 -TemplateUri <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f20b8-108">ByTemplateFileAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="f20b8-108">ByTemplateFileAndParameterFile</span></span>
```
New-AzureRmResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-Force] [-AsJob] -TemplateParameterFile <String> -TemplateFile <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f20b8-109">ByTemplateUriAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="f20b8-109">ByTemplateUriAndParameterFile</span></span>
```
New-AzureRmResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-Force] [-AsJob] -TemplateParameterFile <String> -TemplateUri <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f20b8-110">ByTemplateFileAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="f20b8-110">ByTemplateFileAndParameterUri</span></span>
```
New-AzureRmResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-Force] [-AsJob] -TemplateParameterUri <String> -TemplateFile <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f20b8-111">ByTemplateUriAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="f20b8-111">ByTemplateUriAndParameterUri</span></span>
```
New-AzureRmResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-Force] [-AsJob] -TemplateParameterUri <String> -TemplateUri <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f20b8-112">ByTemplateUriWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="f20b8-112">ByTemplateUriWithNoParameters</span></span>
```
New-AzureRmResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-Force] [-AsJob] -TemplateUri <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f20b8-113">說明</span><span class="sxs-lookup"><span data-stu-id="f20b8-113">DESCRIPTION</span></span>
<span data-ttu-id="f20b8-114">**AzureRmResourceGroupDeployment** Cmdlet 會將部署新增至現有的資源群組。</span><span class="sxs-lookup"><span data-stu-id="f20b8-114">The **New-AzureRmResourceGroupDeployment** cmdlet adds a deployment to an existing resource group.</span></span>
<span data-ttu-id="f20b8-115">這包括部署所需的資源。</span><span class="sxs-lookup"><span data-stu-id="f20b8-115">This includes the resources that the deployment requires.</span></span>

<span data-ttu-id="f20b8-116">Azure 資源是使用者管理的 Azure 實體，例如資料庫伺服器、資料庫、網站、虛擬機器或儲存空間帳戶。</span><span class="sxs-lookup"><span data-stu-id="f20b8-116">An Azure resource is a user-managed Azure entity, such as a database server, database, website, virtual machine, or Storage account.</span></span>
<span data-ttu-id="f20b8-117">Azure 資源群組是一個以單位（例如網站、資料庫伺服器以及財務網站所需的資料庫）的形式來部署的 Azure 資源集合。</span><span class="sxs-lookup"><span data-stu-id="f20b8-117">An Azure resource group is a collection of Azure resources that are deployed as a unit, such as the website, database server, and databases that are required for a financial website.</span></span>
<span data-ttu-id="f20b8-118">資源群組部署使用範本將資源新增至資源群組，併發布資源，以便在 Azure 中使用它們。</span><span class="sxs-lookup"><span data-stu-id="f20b8-118">A resource group deployment uses a template to add resources to a resource group and publishes them so that they are available in Azure.</span></span>
<span data-ttu-id="f20b8-119">若要在不使用範本的情況下，將資源新增至資源群組，請使用 New-AzureRmResource Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="f20b8-119">To add resources to a resource group without using a template, use the New-AzureRmResource cmdlet.</span></span>

<span data-ttu-id="f20b8-120">若要新增資源群組部署，請指定現有資源群組和資源群組範本的名稱。</span><span class="sxs-lookup"><span data-stu-id="f20b8-120">To add a resource group deployment, specify the name of an existing resource group and a resource group template.</span></span>
<span data-ttu-id="f20b8-121">資源群組範本是一個 JSON 字串，代表複雜雲端服務（例如網頁入口網站）的資源群組。</span><span class="sxs-lookup"><span data-stu-id="f20b8-121">A resource group template is a JSON string that represents a resource group for a complex cloud-based service, such as a web portal.</span></span>
<span data-ttu-id="f20b8-122">範本包含必要資源的參數預留位置，以及可設定的屬性值，例如名稱和大小。</span><span class="sxs-lookup"><span data-stu-id="f20b8-122">The template includes parameter placeholders for required resources and configurable property values, such as names and sizes.</span></span>
<span data-ttu-id="f20b8-123">您可以在 Azure 範本庫中找到許多範本，或者您可以建立自己的範本。</span><span class="sxs-lookup"><span data-stu-id="f20b8-123">You can find many templates in the Azure template gallery or you can create your own templates.</span></span>
<span data-ttu-id="f20b8-124">您可以使用 **AzureRmResourceGroupGalleryTemplate** Cmdlet 來尋找圖庫中的範本。</span><span class="sxs-lookup"><span data-stu-id="f20b8-124">You can use the **Get-AzureRmResourceGroupGalleryTemplate** cmdlet to find a template in the gallery.</span></span>

<span data-ttu-id="f20b8-125">若要使用自訂範本來建立資源群組，請指定 *TemplateFile* 參數或 *TemplateUri* 參數。</span><span class="sxs-lookup"><span data-stu-id="f20b8-125">To use a custom template to create a resource group, specify the *TemplateFile* parameter or *TemplateUri* parameter.</span></span>
<span data-ttu-id="f20b8-126">每個範本都有可設定屬性的參數。</span><span class="sxs-lookup"><span data-stu-id="f20b8-126">Each template has parameters for configurable properties.</span></span>
<span data-ttu-id="f20b8-127">若要指定範本參數的值，請指定 *TemplateParameterFile* 參數或 *TemplateParameterObject* 參數。</span><span class="sxs-lookup"><span data-stu-id="f20b8-127">To specify values for the template parameters, specify the *TemplateParameterFile* parameter or the *TemplateParameterObject* parameter.</span></span>
<span data-ttu-id="f20b8-128">或者，您也可以使用在指定範本時動態新增到命令中的範本參數。</span><span class="sxs-lookup"><span data-stu-id="f20b8-128">Alternatively, you can use the template parameters that are dynamically added to the command when you specify a template.</span></span>
<span data-ttu-id="f20b8-129">若要使用動態參數，請在命令提示字元輸入，或輸入減號 ( ) 來指示參數，然後使用 Tab 鍵來迴圈顯示可用的參數。</span><span class="sxs-lookup"><span data-stu-id="f20b8-129">To use dynamic parameters, type them at the command prompt, or type a minus sign (-) to indicate a parameter and use the Tab key to cycle through available parameters.</span></span>
<span data-ttu-id="f20b8-130">您在命令提示字元中輸入的範本參數值會優先于範本參數物件或檔案中的值。</span><span class="sxs-lookup"><span data-stu-id="f20b8-130">Template parameter values that you enter at the command prompt take precedence over values in a template parameter object or file.</span></span>

## <span data-ttu-id="f20b8-131">示例</span><span class="sxs-lookup"><span data-stu-id="f20b8-131">EXAMPLES</span></span>

### <span data-ttu-id="f20b8-132">範例1：使用自訂範本和參數檔案建立部署</span><span class="sxs-lookup"><span data-stu-id="f20b8-132">Example 1: Use a custom template and parameter file to create a deployment</span></span>
```
PS C:\>New-AzureRmResourceGroupDeployment -ResourceGroupName "ContosoEngineering" -TemplateFile "D:\Azure\Templates\EngineeringSite.json" -TemplateParameterFile "D:\Azure\Templates\EngSiteParms.json" -TemplateVersion "2.1"
```

<span data-ttu-id="f20b8-133">這個命令會使用自訂範本與磁片上的範本檔案，建立新的部署。</span><span class="sxs-lookup"><span data-stu-id="f20b8-133">This command creates a new deployment by using a custom template and a template file on disk.</span></span>
<span data-ttu-id="f20b8-134">此命令會使用 *TemplateFile* 參數來指定範本和 *TemplateParameterFile* 參數，以指定包含參數和參數值的檔案。</span><span class="sxs-lookup"><span data-stu-id="f20b8-134">The command uses the *TemplateFile* parameter to specify the template and the *TemplateParameterFile* parameter to specify a file that contains parameters and parameter values.</span></span>
<span data-ttu-id="f20b8-135">它會使用 *TemplateVersion* 參數來指定範本版本。</span><span class="sxs-lookup"><span data-stu-id="f20b8-135">It uses the *TemplateVersion* parameter to specify the version of the template.</span></span>

## <span data-ttu-id="f20b8-136">參數</span><span class="sxs-lookup"><span data-stu-id="f20b8-136">PARAMETERS</span></span>

### <span data-ttu-id="f20b8-137">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="f20b8-137">-ApiVersion</span></span>
<span data-ttu-id="f20b8-138">指定資源提供者支援的 API 版本。</span><span class="sxs-lookup"><span data-stu-id="f20b8-138">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="f20b8-139">您可以指定不同于預設版本的版本。</span><span class="sxs-lookup"><span data-stu-id="f20b8-139">You can specify a different version than the default version.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f20b8-140">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f20b8-140">-AsJob</span></span>
<span data-ttu-id="f20b8-141">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="f20b8-141">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f20b8-142">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f20b8-142">-DefaultProfile</span></span>
<span data-ttu-id="f20b8-143">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="f20b8-143">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f20b8-144">-DeploymentDebugLogLevel</span><span class="sxs-lookup"><span data-stu-id="f20b8-144">-DeploymentDebugLogLevel</span></span>
<span data-ttu-id="f20b8-145">指定調試記錄層級。</span><span class="sxs-lookup"><span data-stu-id="f20b8-145">Specifies a debug log level.</span></span>
<span data-ttu-id="f20b8-146">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="f20b8-146">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="f20b8-147">RequestContent</span><span class="sxs-lookup"><span data-stu-id="f20b8-147">RequestContent</span></span>
- <span data-ttu-id="f20b8-148">ResponseContent</span><span class="sxs-lookup"><span data-stu-id="f20b8-148">ResponseContent</span></span>
- <span data-ttu-id="f20b8-149">同時</span><span class="sxs-lookup"><span data-stu-id="f20b8-149">All</span></span>
- <span data-ttu-id="f20b8-150">所有</span><span class="sxs-lookup"><span data-stu-id="f20b8-150">None</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f20b8-151">-Force</span><span class="sxs-lookup"><span data-stu-id="f20b8-151">-Force</span></span>
<span data-ttu-id="f20b8-152">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="f20b8-152">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f20b8-153">模式</span><span class="sxs-lookup"><span data-stu-id="f20b8-153">-Mode</span></span>
<span data-ttu-id="f20b8-154">指定部署模式。</span><span class="sxs-lookup"><span data-stu-id="f20b8-154">Specifies the deployment mode.</span></span> <span data-ttu-id="f20b8-155">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="f20b8-155">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="f20b8-156">完備</span><span class="sxs-lookup"><span data-stu-id="f20b8-156">Complete</span></span>
- <span data-ttu-id="f20b8-157">少量</span><span class="sxs-lookup"><span data-stu-id="f20b8-157">Incremental</span></span>

<span data-ttu-id="f20b8-158">在完整模式中，資源管理員會刪除資源群組中存在但未在範本中指定的資源。</span><span class="sxs-lookup"><span data-stu-id="f20b8-158">In complete mode, Resource Manager deletes resources that exist in the resource group but are not specified in the template.</span></span> <span data-ttu-id="f20b8-159">在增量模式中，資源管理器會保留資源群組中存在但未在範本中指定的未改動資源。</span><span class="sxs-lookup"><span data-stu-id="f20b8-159">In incremental mode, Resource Manager leaves unchanged resources that exist in the resource group but are not specified in the template.</span></span>

```yaml
Type: DeploymentMode
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: Incremental
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f20b8-160">-名稱</span><span class="sxs-lookup"><span data-stu-id="f20b8-160">-Name</span></span>
<span data-ttu-id="f20b8-161">指定要建立之資源群組部署的名稱。</span><span class="sxs-lookup"><span data-stu-id="f20b8-161">Specifies the name of the resource group deployment to create.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: DeploymentName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f20b8-162">-預先</span><span class="sxs-lookup"><span data-stu-id="f20b8-162">-Pre</span></span>
<span data-ttu-id="f20b8-163">表示此 Cmdlet 會在自動決定要使用哪個版本時，考慮預發行 API 版本。</span><span class="sxs-lookup"><span data-stu-id="f20b8-163">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f20b8-164">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f20b8-164">-ResourceGroupName</span></span>
<span data-ttu-id="f20b8-165">指定要部署之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="f20b8-165">Specifies the name of the resource group to deploy.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f20b8-166">-TemplateFile</span><span class="sxs-lookup"><span data-stu-id="f20b8-166">-TemplateFile</span></span>
<span data-ttu-id="f20b8-167">指定 JSON 範本檔的完整路徑。</span><span class="sxs-lookup"><span data-stu-id="f20b8-167">Specifies the full path of a JSON template file.</span></span>
<span data-ttu-id="f20b8-168">這可以是一種已儲存為 JSON 檔案的自訂範本或圖庫範本，例如使用 **AzureRmResourceGroupGalleryTemplate** Cmdlet 建立的檔。</span><span class="sxs-lookup"><span data-stu-id="f20b8-168">This can be a custom template or a gallery template that is saved as a JSON file, such as one created by using the **Save-AzureRmResourceGroupGalleryTemplate** cmdlet.</span></span>

```yaml
Type: String
Parameter Sets: ByTemplateFileWithNoParameters, ByTemplateFileAndParameterObject, ByTemplateFileAndParameterFile, ByTemplateFileAndParameterUri
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f20b8-169">-TemplateParameterFile</span><span class="sxs-lookup"><span data-stu-id="f20b8-169">-TemplateParameterFile</span></span>
<span data-ttu-id="f20b8-170">指定包含範本參數之名稱和值的 JSON 檔案的完整路徑。</span><span class="sxs-lookup"><span data-stu-id="f20b8-170">Specifies the full path of a JSON file that contains the names and values of the template parameters.</span></span>
<span data-ttu-id="f20b8-171">如果範本有參數，您必須使用 *TemplateParameterFile* 參數或 *TemplateParameterObject* 參數指定參數值。</span><span class="sxs-lookup"><span data-stu-id="f20b8-171">If a template has parameters, you must specify the parameter values with the *TemplateParameterFile* parameter or the *TemplateParameterObject* parameter.</span></span>
<span data-ttu-id="f20b8-172">當您指定範本時，範本參數會動態新增到命令中。</span><span class="sxs-lookup"><span data-stu-id="f20b8-172">Template parameters are dynamically added to the command when you specify a template.</span></span>

<span data-ttu-id="f20b8-173">若要使用動態參數，請輸入減號， ( ) 來指示參數名稱，然後使用 Tab 鍵來迴圈顯示可用的參數。</span><span class="sxs-lookup"><span data-stu-id="f20b8-173">To use the dynamic parameters, type a minus sign (-) to indicate a parameter name and then use the Tab key to cycle through the available parameters.</span></span>

```yaml
Type: String
Parameter Sets: ByTemplateFileAndParameterFile, ByTemplateUriAndParameterFile
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f20b8-174">-TemplateParameterObject</span><span class="sxs-lookup"><span data-stu-id="f20b8-174">-TemplateParameterObject</span></span>
<span data-ttu-id="f20b8-175">指定範本參數名稱和值的雜湊表。</span><span class="sxs-lookup"><span data-stu-id="f20b8-175">Specifies a hash table of template parameter names and values.</span></span>
<span data-ttu-id="f20b8-176">如需有關 Windows PowerShell 中的雜湊資料表的說明，請輸入 `Get-Help about_Hash_Tables` 。</span><span class="sxs-lookup"><span data-stu-id="f20b8-176">For help with hash tables in Windows PowerShell, type `Get-Help about_Hash_Tables`.</span></span>
<span data-ttu-id="f20b8-177">如果範本有參數，您必須指定參數值。</span><span class="sxs-lookup"><span data-stu-id="f20b8-177">If a template has parameters, you must specify parameter values.</span></span>
<span data-ttu-id="f20b8-178">當您指定範本時，範本參數會動態新增到命令中。</span><span class="sxs-lookup"><span data-stu-id="f20b8-178">Template parameters are dynamically added to the command when you specify a template.</span></span>

```yaml
Type: Hashtable
Parameter Sets: ByTemplateFileAndParameterObject, ByTemplateUriAndParameterObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f20b8-179">-TemplateParameterUri</span><span class="sxs-lookup"><span data-stu-id="f20b8-179">-TemplateParameterUri</span></span>
<span data-ttu-id="f20b8-180">指定範本參數檔的 URI。</span><span class="sxs-lookup"><span data-stu-id="f20b8-180">Specifies the URI of a template parameters file.</span></span>

```yaml
Type: String
Parameter Sets: ByTemplateFileAndParameterUri, ByTemplateUriAndParameterUri
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f20b8-181">-TemplateUri</span><span class="sxs-lookup"><span data-stu-id="f20b8-181">-TemplateUri</span></span>
<span data-ttu-id="f20b8-182">指定 JSON 範本檔案的 URI。</span><span class="sxs-lookup"><span data-stu-id="f20b8-182">Specifies the URI of a JSON template file.</span></span>
<span data-ttu-id="f20b8-183">此檔案可以是另一個儲存為 JSON 檔案的自訂範本或圖庫範本，例如使用 **AzureRmResourceGroupGalleryTemplate** 。</span><span class="sxs-lookup"><span data-stu-id="f20b8-183">This file can be a custom template or a gallery template that is saved as a JSON file, such as by using **Save-AzureRmResourceGroupGalleryTemplate**.</span></span>

```yaml
Type: String
Parameter Sets: ByTemplateUriAndParameterObject, ByTemplateUriAndParameterFile, ByTemplateUriAndParameterUri, ByTemplateUriWithNoParameters
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f20b8-184">-確認</span><span class="sxs-lookup"><span data-stu-id="f20b8-184">-Confirm</span></span>
<span data-ttu-id="f20b8-185">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="f20b8-185">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f20b8-186">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f20b8-186">-WhatIf</span></span>
<span data-ttu-id="f20b8-187">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="f20b8-187">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f20b8-188">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="f20b8-188">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f20b8-189">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f20b8-189">CommonParameters</span></span>
<span data-ttu-id="f20b8-190">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="f20b8-190">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f20b8-191">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="f20b8-191">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f20b8-192">輸入</span><span class="sxs-lookup"><span data-stu-id="f20b8-192">INPUTS</span></span>

### <span data-ttu-id="f20b8-193">所有</span><span class="sxs-lookup"><span data-stu-id="f20b8-193">None</span></span>

## <span data-ttu-id="f20b8-194">輸出</span><span class="sxs-lookup"><span data-stu-id="f20b8-194">OUTPUTS</span></span>

### <span data-ttu-id="f20b8-195">PSResourceGroupDeployment 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="f20b8-195">Microsoft.Azure.Commands.ResourceManager.Models.PSResourceGroupDeployment</span></span>

## <span data-ttu-id="f20b8-196">筆記</span><span class="sxs-lookup"><span data-stu-id="f20b8-196">NOTES</span></span>

## <span data-ttu-id="f20b8-197">相關連結</span><span class="sxs-lookup"><span data-stu-id="f20b8-197">RELATED LINKS</span></span>

[<span data-ttu-id="f20b8-198">AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="f20b8-198">Get-AzureRmResourceGroupDeployment</span></span>](./Get-AzureRmResourceGroupDeployment.md)

[<span data-ttu-id="f20b8-199">新-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="f20b8-199">New-AzureRmResource</span></span>](./New-AzureRmResource.md)

[<span data-ttu-id="f20b8-200">新-AzureRmResourceGroup</span><span class="sxs-lookup"><span data-stu-id="f20b8-200">New-AzureRmResourceGroup</span></span>](./New-AzureRmResourceGroup.md)

[<span data-ttu-id="f20b8-201">移除-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="f20b8-201">Remove-AzureRmResourceGroupDeployment</span></span>](./Remove-AzureRmResourceGroupDeployment.md)

[<span data-ttu-id="f20b8-202">停止 AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="f20b8-202">Stop-AzureRmResourceGroupDeployment</span></span>](./Stop-AzureRmResourceGroupDeployment.md)

[<span data-ttu-id="f20b8-203">Test-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="f20b8-203">Test-AzureRmResourceGroupDeployment</span></span>](./Test-AzureRmResourceGroupDeployment.md)


