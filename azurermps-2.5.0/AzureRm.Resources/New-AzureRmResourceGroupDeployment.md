---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 6E2F0D5E-E683-46F3-B48B-55C4864F3308
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/new-azurermresourcegroupdeployment
schema: 2.0.0
ms.openlocfilehash: 6c64c9defb3905e9851e79da5303b68e98514f44
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/15/2020
ms.locfileid: "93801901"
---
# <span data-ttu-id="55a88-101">New-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="55a88-101">New-AzureRmResourceGroupDeployment</span></span>

## <span data-ttu-id="55a88-102">摘要</span><span class="sxs-lookup"><span data-stu-id="55a88-102">SYNOPSIS</span></span>
<span data-ttu-id="55a88-103">新增 Azure 部署至資源群組。</span><span class="sxs-lookup"><span data-stu-id="55a88-103">Adds an Azure deployment to a resource group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="55a88-104">句法</span><span class="sxs-lookup"><span data-stu-id="55a88-104">SYNTAX</span></span>

### <span data-ttu-id="55a88-105">ByTemplateFileWithNoParameters (預設) </span><span class="sxs-lookup"><span data-stu-id="55a88-105">ByTemplateFileWithNoParameters (Default)</span></span>
```
New-AzureRmResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>] [-Force]
 [-AsJob] -TemplateFile <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="55a88-106">ByTemplateFileAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="55a88-106">ByTemplateFileAndParameterObject</span></span>
```
New-AzureRmResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>] [-Force]
 [-AsJob] -TemplateParameterObject <Hashtable> -TemplateFile <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="55a88-107">ByTemplateUriAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="55a88-107">ByTemplateUriAndParameterObject</span></span>
```
New-AzureRmResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>] [-Force]
 [-AsJob] -TemplateParameterObject <Hashtable> -TemplateUri <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="55a88-108">ByTemplateFileAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="55a88-108">ByTemplateFileAndParameterFile</span></span>
```
New-AzureRmResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>] [-Force]
 [-AsJob] -TemplateParameterFile <String> -TemplateFile <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="55a88-109">ByTemplateUriAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="55a88-109">ByTemplateUriAndParameterFile</span></span>
```
New-AzureRmResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>] [-Force]
 [-AsJob] -TemplateParameterFile <String> -TemplateUri <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="55a88-110">ByTemplateFileAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="55a88-110">ByTemplateFileAndParameterUri</span></span>
```
New-AzureRmResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>] [-Force]
 [-AsJob] -TemplateParameterUri <String> -TemplateFile <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="55a88-111">ByTemplateUriAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="55a88-111">ByTemplateUriAndParameterUri</span></span>
```
New-AzureRmResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>] [-Force]
 [-AsJob] -TemplateParameterUri <String> -TemplateUri <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="55a88-112">ByTemplateUriWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="55a88-112">ByTemplateUriWithNoParameters</span></span>
```
New-AzureRmResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>] [-Force]
 [-AsJob] -TemplateUri <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="55a88-113">說明</span><span class="sxs-lookup"><span data-stu-id="55a88-113">DESCRIPTION</span></span>
<span data-ttu-id="55a88-114">**AzureRmResourceGroupDeployment** Cmdlet 會將部署新增至現有的資源群組。</span><span class="sxs-lookup"><span data-stu-id="55a88-114">The **New-AzureRmResourceGroupDeployment** cmdlet adds a deployment to an existing resource group.</span></span>
<span data-ttu-id="55a88-115">這包括部署所需的資源。</span><span class="sxs-lookup"><span data-stu-id="55a88-115">This includes the resources that the deployment requires.</span></span>
<span data-ttu-id="55a88-116">Azure 資源是使用者管理的 Azure 實體，例如資料庫伺服器、資料庫、網站、虛擬機器或儲存空間帳戶。</span><span class="sxs-lookup"><span data-stu-id="55a88-116">An Azure resource is a user-managed Azure entity, such as a database server, database, website, virtual machine, or Storage account.</span></span>
<span data-ttu-id="55a88-117">Azure 資源群組是一個以單位（例如網站、資料庫伺服器以及財務網站所需的資料庫）的形式來部署的 Azure 資源集合。</span><span class="sxs-lookup"><span data-stu-id="55a88-117">An Azure resource group is a collection of Azure resources that are deployed as a unit, such as the website, database server, and databases that are required for a financial website.</span></span>
<span data-ttu-id="55a88-118">資源群組部署使用範本將資源新增至資源群組，併發布資源，以便在 Azure 中使用它們。</span><span class="sxs-lookup"><span data-stu-id="55a88-118">A resource group deployment uses a template to add resources to a resource group and publishes them so that they are available in Azure.</span></span>
<span data-ttu-id="55a88-119">若要在不使用範本的情況下，將資源新增至資源群組，請使用 New-AzureRmResource Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="55a88-119">To add resources to a resource group without using a template, use the New-AzureRmResource cmdlet.</span></span>
<span data-ttu-id="55a88-120">若要新增資源群組部署，請指定現有資源群組和資源群組範本的名稱。</span><span class="sxs-lookup"><span data-stu-id="55a88-120">To add a resource group deployment, specify the name of an existing resource group and a resource group template.</span></span>
<span data-ttu-id="55a88-121">資源群組範本是一個 JSON 字串，代表複雜雲端服務（例如網頁入口網站）的資源群組。</span><span class="sxs-lookup"><span data-stu-id="55a88-121">A resource group template is a JSON string that represents a resource group for a complex cloud-based service, such as a web portal.</span></span>
<span data-ttu-id="55a88-122">範本包含必要資源的參數預留位置，以及可設定的屬性值，例如名稱和大小。</span><span class="sxs-lookup"><span data-stu-id="55a88-122">The template includes parameter placeholders for required resources and configurable property values, such as names and sizes.</span></span>
<span data-ttu-id="55a88-123">您可以在 Azure 範本庫中找到許多範本，或者您可以建立自己的範本。</span><span class="sxs-lookup"><span data-stu-id="55a88-123">You can find many templates in the Azure template gallery or you can create your own templates.</span></span>
<span data-ttu-id="55a88-124">您可以使用 **AzureRmResourceGroupGalleryTemplate** Cmdlet 來尋找圖庫中的範本。</span><span class="sxs-lookup"><span data-stu-id="55a88-124">You can use the **Get-AzureRmResourceGroupGalleryTemplate** cmdlet to find a template in the gallery.</span></span>
<span data-ttu-id="55a88-125">若要使用自訂範本來建立資源群組，請指定 *TemplateFile* 參數或 *TemplateUri* 參數。</span><span class="sxs-lookup"><span data-stu-id="55a88-125">To use a custom template to create a resource group, specify the *TemplateFile* parameter or *TemplateUri* parameter.</span></span>
<span data-ttu-id="55a88-126">每個範本都有可設定屬性的參數。</span><span class="sxs-lookup"><span data-stu-id="55a88-126">Each template has parameters for configurable properties.</span></span>
<span data-ttu-id="55a88-127">若要指定範本參數的值，請指定 *TemplateParameterFile* 參數或 *TemplateParameterObject* 參數。</span><span class="sxs-lookup"><span data-stu-id="55a88-127">To specify values for the template parameters, specify the *TemplateParameterFile* parameter or the *TemplateParameterObject* parameter.</span></span>
<span data-ttu-id="55a88-128">或者，您也可以使用在指定範本時動態新增到命令中的範本參數。</span><span class="sxs-lookup"><span data-stu-id="55a88-128">Alternatively, you can use the template parameters that are dynamically added to the command when you specify a template.</span></span>
<span data-ttu-id="55a88-129">若要使用動態參數，請在命令提示字元輸入，或輸入減號 ( ) 來指示參數，然後使用 Tab 鍵來迴圈顯示可用的參數。</span><span class="sxs-lookup"><span data-stu-id="55a88-129">To use dynamic parameters, type them at the command prompt, or type a minus sign (-) to indicate a parameter and use the Tab key to cycle through available parameters.</span></span>
<span data-ttu-id="55a88-130">您在命令提示字元中輸入的範本參數值會優先于範本參數物件或檔案中的值。</span><span class="sxs-lookup"><span data-stu-id="55a88-130">Template parameter values that you enter at the command prompt take precedence over values in a template parameter object or file.</span></span>

## <span data-ttu-id="55a88-131">示例</span><span class="sxs-lookup"><span data-stu-id="55a88-131">EXAMPLES</span></span>

### <span data-ttu-id="55a88-132">範例1：使用自訂範本和參數檔案建立部署</span><span class="sxs-lookup"><span data-stu-id="55a88-132">Example 1: Use a custom template and parameter file to create a deployment</span></span>
```
PS C:\>New-AzureRmResourceGroupDeployment -ResourceGroupName "ContosoEngineering" -TemplateFile "D:\Azure\Templates\EngineeringSite.json" -TemplateParameterFile "D:\Azure\Templates\EngSiteParms.json"
```

<span data-ttu-id="55a88-133">這個命令會使用自訂範本與磁片上的範本檔案，建立新的部署。</span><span class="sxs-lookup"><span data-stu-id="55a88-133">This command creates a new deployment by using a custom template and a template file on disk.</span></span>
<span data-ttu-id="55a88-134">此命令會使用 *TemplateFile* 參數來指定範本和 *TemplateParameterFile* 參數，以指定包含參數和參數值的檔案。</span><span class="sxs-lookup"><span data-stu-id="55a88-134">The command uses the *TemplateFile* parameter to specify the template and the *TemplateParameterFile* parameter to specify a file that contains parameters and parameter values.</span></span>

## <span data-ttu-id="55a88-135">參數</span><span class="sxs-lookup"><span data-stu-id="55a88-135">PARAMETERS</span></span>

### <span data-ttu-id="55a88-136">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="55a88-136">-ApiVersion</span></span>
<span data-ttu-id="55a88-137">指定資源提供者支援的 API 版本。</span><span class="sxs-lookup"><span data-stu-id="55a88-137">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="55a88-138">您可以指定不同于預設版本的版本。</span><span class="sxs-lookup"><span data-stu-id="55a88-138">You can specify a different version than the default version.</span></span>

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

### <span data-ttu-id="55a88-139">-AsJob</span><span class="sxs-lookup"><span data-stu-id="55a88-139">-AsJob</span></span>
<span data-ttu-id="55a88-140">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="55a88-140">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="55a88-141">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="55a88-141">-DefaultProfile</span></span>
<span data-ttu-id="55a88-142">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="55a88-142">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="55a88-143">-DeploymentDebugLogLevel</span><span class="sxs-lookup"><span data-stu-id="55a88-143">-DeploymentDebugLogLevel</span></span>
<span data-ttu-id="55a88-144">指定調試記錄層級。</span><span class="sxs-lookup"><span data-stu-id="55a88-144">Specifies a debug log level.</span></span>
<span data-ttu-id="55a88-145">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="55a88-145">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="55a88-146">RequestContent</span><span class="sxs-lookup"><span data-stu-id="55a88-146">RequestContent</span></span>
- <span data-ttu-id="55a88-147">ResponseContent</span><span class="sxs-lookup"><span data-stu-id="55a88-147">ResponseContent</span></span>
- <span data-ttu-id="55a88-148">同時</span><span class="sxs-lookup"><span data-stu-id="55a88-148">All</span></span>
- <span data-ttu-id="55a88-149">所有</span><span class="sxs-lookup"><span data-stu-id="55a88-149">None</span></span>

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

### <span data-ttu-id="55a88-150">-Force</span><span class="sxs-lookup"><span data-stu-id="55a88-150">-Force</span></span>
<span data-ttu-id="55a88-151">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="55a88-151">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="55a88-152">模式</span><span class="sxs-lookup"><span data-stu-id="55a88-152">-Mode</span></span>
<span data-ttu-id="55a88-153">指定部署模式。</span><span class="sxs-lookup"><span data-stu-id="55a88-153">Specifies the deployment mode.</span></span> <span data-ttu-id="55a88-154">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="55a88-154">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="55a88-155">完備</span><span class="sxs-lookup"><span data-stu-id="55a88-155">Complete</span></span>
- <span data-ttu-id="55a88-156">在完整模式中增加，資源管理員會刪除資源群組中存在但未在範本中指定的資源。</span><span class="sxs-lookup"><span data-stu-id="55a88-156">Incremental In complete mode, Resource Manager deletes resources that exist in the resource group but are not specified in the template.</span></span> <span data-ttu-id="55a88-157">在增量模式中，資源管理器會保留資源群組中存在但未在範本中指定的未改動資源。</span><span class="sxs-lookup"><span data-stu-id="55a88-157">In incremental mode, Resource Manager leaves unchanged resources that exist in the resource group but are not specified in the template.</span></span>

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

### <span data-ttu-id="55a88-158">-名稱</span><span class="sxs-lookup"><span data-stu-id="55a88-158">-Name</span></span>
<span data-ttu-id="55a88-159">指定要建立之資源群組部署的名稱。</span><span class="sxs-lookup"><span data-stu-id="55a88-159">Specifies the name of the resource group deployment to create.</span></span>

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

### <span data-ttu-id="55a88-160">-預先</span><span class="sxs-lookup"><span data-stu-id="55a88-160">-Pre</span></span>
<span data-ttu-id="55a88-161">表示此 Cmdlet 會在自動決定要使用哪個版本時，考慮預發行 API 版本。</span><span class="sxs-lookup"><span data-stu-id="55a88-161">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="55a88-162">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="55a88-162">-ResourceGroupName</span></span>
<span data-ttu-id="55a88-163">指定要部署之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="55a88-163">Specifies the name of the resource group to deploy.</span></span>

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

### <span data-ttu-id="55a88-164">-RollBackDeploymentName</span><span class="sxs-lookup"><span data-stu-id="55a88-164">-RollBackDeploymentName</span></span>
<span data-ttu-id="55a88-165">如果使用了-RollbackToLastDeployment，則會使用資源群組中的指定名稱回滾到成功的部署。</span><span class="sxs-lookup"><span data-stu-id="55a88-165">Rollback to the successful deployment with the given name in the resource group, should not be used if -RollbackToLastDeployment is used.</span></span>

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

### <span data-ttu-id="55a88-166">-RollbackToLastDeployment</span><span class="sxs-lookup"><span data-stu-id="55a88-166">-RollbackToLastDeployment</span></span>
<span data-ttu-id="55a88-167">如果使用-RollBackDeploymentName，則回退至 [資源] 群組中的最後一個成功部署。</span><span class="sxs-lookup"><span data-stu-id="55a88-167">Rollback to the last successful deployment in the resource group, should not be present if -RollBackDeploymentName is used.</span></span>

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

### <span data-ttu-id="55a88-168">-TemplateFile</span><span class="sxs-lookup"><span data-stu-id="55a88-168">-TemplateFile</span></span>
<span data-ttu-id="55a88-169">指定 JSON 範本檔的完整路徑。</span><span class="sxs-lookup"><span data-stu-id="55a88-169">Specifies the full path of a JSON template file.</span></span>
<span data-ttu-id="55a88-170">這可以是一種已儲存為 JSON 檔案的自訂範本或圖庫範本，例如使用 **AzureRmResourceGroupGalleryTemplate** Cmdlet 建立的檔。</span><span class="sxs-lookup"><span data-stu-id="55a88-170">This can be a custom template or a gallery template that is saved as a JSON file, such as one created by using the **Save-AzureRmResourceGroupGalleryTemplate** cmdlet.</span></span>

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

### <span data-ttu-id="55a88-171">-TemplateParameterFile</span><span class="sxs-lookup"><span data-stu-id="55a88-171">-TemplateParameterFile</span></span>
<span data-ttu-id="55a88-172">指定包含範本參數之名稱和值的 JSON 檔案的完整路徑。</span><span class="sxs-lookup"><span data-stu-id="55a88-172">Specifies the full path of a JSON file that contains the names and values of the template parameters.</span></span>
<span data-ttu-id="55a88-173">如果範本有參數，您必須使用 *TemplateParameterFile* 參數或 *TemplateParameterObject* 參數指定參數值。</span><span class="sxs-lookup"><span data-stu-id="55a88-173">If a template has parameters, you must specify the parameter values with the *TemplateParameterFile* parameter or the *TemplateParameterObject* parameter.</span></span>
<span data-ttu-id="55a88-174">當您指定範本時，範本參數會動態新增到命令中。</span><span class="sxs-lookup"><span data-stu-id="55a88-174">Template parameters are dynamically added to the command when you specify a template.</span></span>
<span data-ttu-id="55a88-175">若要使用動態參數，請輸入減號， ( ) 來指示參數名稱，然後使用 Tab 鍵來迴圈顯示可用的參數。</span><span class="sxs-lookup"><span data-stu-id="55a88-175">To use the dynamic parameters, type a minus sign (-) to indicate a parameter name and then use the Tab key to cycle through the available parameters.</span></span>

```yaml
Type: System.String
Parameter Sets: ByTemplateFileAndParameterFile, ByTemplateUriAndParameterFile
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="55a88-176">-TemplateParameterObject</span><span class="sxs-lookup"><span data-stu-id="55a88-176">-TemplateParameterObject</span></span>
<span data-ttu-id="55a88-177">指定範本參數名稱和值的雜湊表。</span><span class="sxs-lookup"><span data-stu-id="55a88-177">Specifies a hash table of template parameter names and values.</span></span>
<span data-ttu-id="55a88-178">如需有關 Windows PowerShell 中的雜湊資料表的說明，請輸入 `Get-Help about_Hash_Tables` 。</span><span class="sxs-lookup"><span data-stu-id="55a88-178">For help with hash tables in Windows PowerShell, type `Get-Help about_Hash_Tables`.</span></span>
<span data-ttu-id="55a88-179">如果範本有參數，您必須指定參數值。</span><span class="sxs-lookup"><span data-stu-id="55a88-179">If a template has parameters, you must specify parameter values.</span></span>
<span data-ttu-id="55a88-180">當您指定範本時，範本參數會動態新增到命令中。</span><span class="sxs-lookup"><span data-stu-id="55a88-180">Template parameters are dynamically added to the command when you specify a template.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: ByTemplateFileAndParameterObject, ByTemplateUriAndParameterObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="55a88-181">-TemplateParameterUri</span><span class="sxs-lookup"><span data-stu-id="55a88-181">-TemplateParameterUri</span></span>
<span data-ttu-id="55a88-182">指定範本參數檔的 URI。</span><span class="sxs-lookup"><span data-stu-id="55a88-182">Specifies the URI of a template parameters file.</span></span>

```yaml
Type: System.String
Parameter Sets: ByTemplateFileAndParameterUri, ByTemplateUriAndParameterUri
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="55a88-183">-TemplateUri</span><span class="sxs-lookup"><span data-stu-id="55a88-183">-TemplateUri</span></span>
<span data-ttu-id="55a88-184">指定 JSON 範本檔案的 URI。</span><span class="sxs-lookup"><span data-stu-id="55a88-184">Specifies the URI of a JSON template file.</span></span>
<span data-ttu-id="55a88-185">此檔案可以是另一個儲存為 JSON 檔案的自訂範本或圖庫範本，例如使用 **AzureRmResourceGroupGalleryTemplate** 。</span><span class="sxs-lookup"><span data-stu-id="55a88-185">This file can be a custom template or a gallery template that is saved as a JSON file, such as by using **Save-AzureRmResourceGroupGalleryTemplate**.</span></span>

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

### <span data-ttu-id="55a88-186">-確認</span><span class="sxs-lookup"><span data-stu-id="55a88-186">-Confirm</span></span>
<span data-ttu-id="55a88-187">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="55a88-187">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="55a88-188">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="55a88-188">-WhatIf</span></span>
<span data-ttu-id="55a88-189">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="55a88-189">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="55a88-190">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="55a88-190">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="55a88-191">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="55a88-191">CommonParameters</span></span>
<span data-ttu-id="55a88-192">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="55a88-192">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="55a88-193">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="55a88-193">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="55a88-194">輸入</span><span class="sxs-lookup"><span data-stu-id="55a88-194">INPUTS</span></span>

### <span data-ttu-id="55a88-195">所有</span><span class="sxs-lookup"><span data-stu-id="55a88-195">None</span></span>

## <span data-ttu-id="55a88-196">輸出</span><span class="sxs-lookup"><span data-stu-id="55a88-196">OUTPUTS</span></span>

### <span data-ttu-id="55a88-197">PSResourceGroupDeployment 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="55a88-197">Microsoft.Azure.Commands.ResourceManager.Models.PSResourceGroupDeployment</span></span>

## <span data-ttu-id="55a88-198">筆記</span><span class="sxs-lookup"><span data-stu-id="55a88-198">NOTES</span></span>

## <span data-ttu-id="55a88-199">相關連結</span><span class="sxs-lookup"><span data-stu-id="55a88-199">RELATED LINKS</span></span>

[<span data-ttu-id="55a88-200">AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="55a88-200">Get-AzureRmResourceGroupDeployment</span></span>](./Get-AzureRmResourceGroupDeployment.md)

[<span data-ttu-id="55a88-201">新-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="55a88-201">New-AzureRmResource</span></span>](./New-AzureRmResource.md)

[<span data-ttu-id="55a88-202">新-AzureRmResourceGroup</span><span class="sxs-lookup"><span data-stu-id="55a88-202">New-AzureRmResourceGroup</span></span>](./New-AzureRmResourceGroup.md)

[<span data-ttu-id="55a88-203">移除-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="55a88-203">Remove-AzureRmResourceGroupDeployment</span></span>](./Remove-AzureRmResourceGroupDeployment.md)

[<span data-ttu-id="55a88-204">停止 AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="55a88-204">Stop-AzureRmResourceGroupDeployment</span></span>](./Stop-AzureRmResourceGroupDeployment.md)

[<span data-ttu-id="55a88-205">Test-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="55a88-205">Test-AzureRmResourceGroupDeployment</span></span>](./Test-AzureRmResourceGroupDeployment.md)


