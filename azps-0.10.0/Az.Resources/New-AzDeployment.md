---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-Azdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/New-AzDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/New-AzDeployment.md
ms.openlocfilehash: 97d6b11a4993ced62b84de24c501a2c438173141
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/16/2020
ms.locfileid: "93795278"
---
# <span data-ttu-id="8f6b3-101">New-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="8f6b3-101">New-AzDeployment</span></span>

## <span data-ttu-id="8f6b3-102">摘要</span><span class="sxs-lookup"><span data-stu-id="8f6b3-102">SYNOPSIS</span></span>
<span data-ttu-id="8f6b3-103">建立部署</span><span class="sxs-lookup"><span data-stu-id="8f6b3-103">Creat a deployment</span></span>

## <span data-ttu-id="8f6b3-104">句法</span><span class="sxs-lookup"><span data-stu-id="8f6b3-104">SYNTAX</span></span>

### <span data-ttu-id="8f6b3-105">ByTemplateFileWithNoParameters (預設) </span><span class="sxs-lookup"><span data-stu-id="8f6b3-105">ByTemplateFileWithNoParameters (Default)</span></span>
```
New-AzDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-AsJob]
 -TemplateFile <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8f6b3-106">ByTemplateFileAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="8f6b3-106">ByTemplateFileAndParameterObject</span></span>
```
New-AzDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-AsJob]
 -TemplateParameterObject <Hashtable> -TemplateFile <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8f6b3-107">ByTemplateUriAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="8f6b3-107">ByTemplateUriAndParameterObject</span></span>
```
New-AzDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-AsJob]
 -TemplateParameterObject <Hashtable> -TemplateUri <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8f6b3-108">ByTemplateFileAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="8f6b3-108">ByTemplateFileAndParameterFile</span></span>
```
New-AzDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-AsJob]
 -TemplateParameterFile <String> -TemplateFile <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8f6b3-109">ByTemplateUriAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="8f6b3-109">ByTemplateUriAndParameterFile</span></span>
```
New-AzDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-AsJob]
 -TemplateParameterFile <String> -TemplateUri <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8f6b3-110">ByTemplateFileAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="8f6b3-110">ByTemplateFileAndParameterUri</span></span>
```
New-AzDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-AsJob]
 -TemplateParameterUri <String> -TemplateFile <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8f6b3-111">ByTemplateUriAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="8f6b3-111">ByTemplateUriAndParameterUri</span></span>
```
New-AzDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-AsJob]
 -TemplateParameterUri <String> -TemplateUri <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8f6b3-112">ByTemplateUriWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="8f6b3-112">ByTemplateUriWithNoParameters</span></span>
```
New-AzDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-AsJob]
 -TemplateUri <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8f6b3-113">說明</span><span class="sxs-lookup"><span data-stu-id="8f6b3-113">DESCRIPTION</span></span>
<span data-ttu-id="8f6b3-114">**新的-AzDeployment** Cmdlet 會在目前的訂閱範圍中新增部署。</span><span class="sxs-lookup"><span data-stu-id="8f6b3-114">The **New-AzDeployment** cmdlet adds a deployment at the current subscription scope.</span></span>
<span data-ttu-id="8f6b3-115">這包括部署所需的資源。</span><span class="sxs-lookup"><span data-stu-id="8f6b3-115">This includes the resources that the deployment requires.</span></span>

<span data-ttu-id="8f6b3-116">Azure 資源是使用者管理的 Azure 實體。</span><span class="sxs-lookup"><span data-stu-id="8f6b3-116">An Azure resource is a user-managed Azure entity.</span></span> <span data-ttu-id="8f6b3-117">資源可以駐留在資源群組中，例如資料庫伺服器、資料庫、網站、虛擬機器或儲存空間帳戶。</span><span class="sxs-lookup"><span data-stu-id="8f6b3-117">A resource can live in a resource group, like database server, database, website, virtual machine, or Storage account.</span></span> <span data-ttu-id="8f6b3-118">或者，它可以是訂閱階層資源，例如角色定義、原則定義等。</span><span class="sxs-lookup"><span data-stu-id="8f6b3-118">Or, it can be a subscription level resource, like role definition, policy definition, etc.</span></span>

<span data-ttu-id="8f6b3-119">若要將資源新增至資源群組，請使用 **New-AzDeployment** ，這會在資源群組建立部署。</span><span class="sxs-lookup"><span data-stu-id="8f6b3-119">To add resources to a resource group, use the **New-AzDeployment** which creates a deployment at a resource group.</span></span>
<span data-ttu-id="8f6b3-120">**新的-AzDeployment** Cmdlet 會在目前的訂閱範圍中建立部署，以部署訂閱層級資源。</span><span class="sxs-lookup"><span data-stu-id="8f6b3-120">The **New-AzDeployment** cmdlet creates a deployment at the current subscription scope, which deploys subscription level resources.</span></span> 

<span data-ttu-id="8f6b3-121">若要在訂閱中新增部署，請指定位置和範本。</span><span class="sxs-lookup"><span data-stu-id="8f6b3-121">To add a deployment at subscription, specify the location and a template.</span></span>
<span data-ttu-id="8f6b3-122">位置會告知 Azure 資源管理員要儲存部署資料的位置。</span><span class="sxs-lookup"><span data-stu-id="8f6b3-122">The location tells Azure Resource Manager where to store the deployment data.</span></span> <span data-ttu-id="8f6b3-123">範本是一個 JSON 字串，其中包含要部署的個別資源。</span><span class="sxs-lookup"><span data-stu-id="8f6b3-123">The template is a JSON string that contains individual resources to be deployed.</span></span>
<span data-ttu-id="8f6b3-124">範本包含必要資源的參數預留位置，以及可設定的屬性值，例如名稱和大小。</span><span class="sxs-lookup"><span data-stu-id="8f6b3-124">The template includes parameter placeholders for required resources and configurable property values, such as names and sizes.</span></span>

<span data-ttu-id="8f6b3-125">若要在部署中使用自訂範本，請指定 *TemplateFile* 參數或 *TemplateUri* 參數。</span><span class="sxs-lookup"><span data-stu-id="8f6b3-125">To use a custom template for the deployment, specify the *TemplateFile* parameter or *TemplateUri* parameter.</span></span>
<span data-ttu-id="8f6b3-126">每個範本都有可設定屬性的參數。</span><span class="sxs-lookup"><span data-stu-id="8f6b3-126">Each template has parameters for configurable properties.</span></span>
<span data-ttu-id="8f6b3-127">若要指定範本參數的值，請指定 *TemplateParameterFile* 參數或 *TemplateParameterObject* 參數。</span><span class="sxs-lookup"><span data-stu-id="8f6b3-127">To specify values for the template parameters, specify the *TemplateParameterFile* parameter or the *TemplateParameterObject* parameter.</span></span>
<span data-ttu-id="8f6b3-128">或者，您也可以使用在指定範本時動態新增到命令中的範本參數。</span><span class="sxs-lookup"><span data-stu-id="8f6b3-128">Alternatively, you can use the template parameters that are dynamically added to the command when you specify a template.</span></span>
<span data-ttu-id="8f6b3-129">若要使用動態參數，請在命令提示字元輸入，或輸入減號 ( ) 來指示參數，然後使用 Tab 鍵來迴圈顯示可用的參數。</span><span class="sxs-lookup"><span data-stu-id="8f6b3-129">To use dynamic parameters, type them at the command prompt, or type a minus sign (-) to indicate a parameter and use the Tab key to cycle through available parameters.</span></span>
<span data-ttu-id="8f6b3-130">您在命令提示字元中輸入的範本參數值會優先于範本參數物件或檔案中的值。</span><span class="sxs-lookup"><span data-stu-id="8f6b3-130">Template parameter values that you enter at the command prompt take precedence over values in a template parameter object or file.</span></span>

## <span data-ttu-id="8f6b3-131">示例</span><span class="sxs-lookup"><span data-stu-id="8f6b3-131">EXAMPLES</span></span>

### <span data-ttu-id="8f6b3-132">範例1：使用自訂範本和參數檔案建立部署</span><span class="sxs-lookup"><span data-stu-id="8f6b3-132">Example 1: Use a custom template and parameter file to create a deployment</span></span>
```
PS C:\>New-AzDeployment -Location "West US" -TemplateFile "D:\Azure\Templates\EngineeringSite.json" -TemplateParameterFile "D:\Azure\Templates\EngSiteParms.json" -TemplateVersion "2.1"
```

<span data-ttu-id="8f6b3-133">這個命令會使用自訂範本與磁片上的範本檔案，在目前的訂閱範圍中建立新的部署。</span><span class="sxs-lookup"><span data-stu-id="8f6b3-133">This command creates a new deployment at the current subscription scope by using a custom template and a template file on disk.</span></span>
<span data-ttu-id="8f6b3-134">此命令會使用 *TemplateFile* 參數來指定範本和 *TemplateParameterFile* 參數，以指定包含參數和參數值的檔案。</span><span class="sxs-lookup"><span data-stu-id="8f6b3-134">The command uses the *TemplateFile* parameter to specify the template and the *TemplateParameterFile* parameter to specify a file that contains parameters and parameter values.</span></span>
<span data-ttu-id="8f6b3-135">它會使用 *TemplateVersion* 參數來指定範本版本。</span><span class="sxs-lookup"><span data-stu-id="8f6b3-135">It uses the *TemplateVersion* parameter to specify the version of the template.</span></span>

## <span data-ttu-id="8f6b3-136">參數</span><span class="sxs-lookup"><span data-stu-id="8f6b3-136">PARAMETERS</span></span>

### <span data-ttu-id="8f6b3-137">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="8f6b3-137">-ApiVersion</span></span>
<span data-ttu-id="8f6b3-138">設定時，會指出要使用的資源提供者 API 版本。</span><span class="sxs-lookup"><span data-stu-id="8f6b3-138">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="8f6b3-139">如果未指定，API 版本會自動決定為最新的可用。</span><span class="sxs-lookup"><span data-stu-id="8f6b3-139">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="8f6b3-140">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8f6b3-140">-AsJob</span></span>
<span data-ttu-id="8f6b3-141">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="8f6b3-141">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="8f6b3-142">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8f6b3-142">-DefaultProfile</span></span>
<span data-ttu-id="8f6b3-143">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="8f6b3-143">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8f6b3-144">-DeploymentDebugLogLevel</span><span class="sxs-lookup"><span data-stu-id="8f6b3-144">-DeploymentDebugLogLevel</span></span>
<span data-ttu-id="8f6b3-145">部署調試記錄層級。</span><span class="sxs-lookup"><span data-stu-id="8f6b3-145">The deployment debug log level.</span></span>

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

### <span data-ttu-id="8f6b3-146">-位置</span><span class="sxs-lookup"><span data-stu-id="8f6b3-146">-Location</span></span>
<span data-ttu-id="8f6b3-147">儲存部署資料的位置。</span><span class="sxs-lookup"><span data-stu-id="8f6b3-147">The location to store deployment data.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8f6b3-148">-名稱</span><span class="sxs-lookup"><span data-stu-id="8f6b3-148">-Name</span></span>
<span data-ttu-id="8f6b3-149">將要建立之部署的名稱。</span><span class="sxs-lookup"><span data-stu-id="8f6b3-149">The name of the deployment it's going to create.</span></span>
<span data-ttu-id="8f6b3-150">僅在使用範本時有效。</span><span class="sxs-lookup"><span data-stu-id="8f6b3-150">Only valid when a template is used.</span></span>
<span data-ttu-id="8f6b3-151">使用範本時，如果使用者未指定部署名稱，請使用目前的時間，例如「20131223140835」。</span><span class="sxs-lookup"><span data-stu-id="8f6b3-151">When a template is used, if the user doesn't specify a deployment name, use the current time, like "20131223140835".</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: DeploymentName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8f6b3-152">-預先</span><span class="sxs-lookup"><span data-stu-id="8f6b3-152">-Pre</span></span>
<span data-ttu-id="8f6b3-153">設定時，表示 Cmdlet 應該使用預發行 API 版本，以便自動判斷要使用的版本。</span><span class="sxs-lookup"><span data-stu-id="8f6b3-153">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="8f6b3-154">-TemplateFile</span><span class="sxs-lookup"><span data-stu-id="8f6b3-154">-TemplateFile</span></span>
<span data-ttu-id="8f6b3-155">範本檔案的本機路徑。</span><span class="sxs-lookup"><span data-stu-id="8f6b3-155">Local path to the template file.</span></span>

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

### <span data-ttu-id="8f6b3-156">-TemplateParameterFile</span><span class="sxs-lookup"><span data-stu-id="8f6b3-156">-TemplateParameterFile</span></span>
<span data-ttu-id="8f6b3-157">具有範本參數的檔案。</span><span class="sxs-lookup"><span data-stu-id="8f6b3-157">A file that has the template parameters.</span></span>

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

### <span data-ttu-id="8f6b3-158">-TemplateParameterObject</span><span class="sxs-lookup"><span data-stu-id="8f6b3-158">-TemplateParameterObject</span></span>
<span data-ttu-id="8f6b3-159">代表參數的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="8f6b3-159">A hash table which represents the parameters.</span></span>

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

### <span data-ttu-id="8f6b3-160">-TemplateParameterUri</span><span class="sxs-lookup"><span data-stu-id="8f6b3-160">-TemplateParameterUri</span></span>
<span data-ttu-id="8f6b3-161">範本參數檔的 Uri。</span><span class="sxs-lookup"><span data-stu-id="8f6b3-161">Uri to the template parameter file.</span></span>

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

### <span data-ttu-id="8f6b3-162">-TemplateUri</span><span class="sxs-lookup"><span data-stu-id="8f6b3-162">-TemplateUri</span></span>
<span data-ttu-id="8f6b3-163">範本檔案的 Uri。</span><span class="sxs-lookup"><span data-stu-id="8f6b3-163">Uri to the template file.</span></span>

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

### <span data-ttu-id="8f6b3-164">-確認</span><span class="sxs-lookup"><span data-stu-id="8f6b3-164">-Confirm</span></span>
<span data-ttu-id="8f6b3-165">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="8f6b3-165">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8f6b3-166">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8f6b3-166">-WhatIf</span></span>
<span data-ttu-id="8f6b3-167">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="8f6b3-167">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8f6b3-168">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="8f6b3-168">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8f6b3-169">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8f6b3-169">CommonParameters</span></span>
<span data-ttu-id="8f6b3-170">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="8f6b3-170">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8f6b3-171">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="8f6b3-171">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8f6b3-172">輸入</span><span class="sxs-lookup"><span data-stu-id="8f6b3-172">INPUTS</span></span>

### <span data-ttu-id="8f6b3-173">System.object</span><span class="sxs-lookup"><span data-stu-id="8f6b3-173">System.String</span></span>
<span data-ttu-id="8f6b3-174">[System.object] 集合. Hashtable</span><span class="sxs-lookup"><span data-stu-id="8f6b3-174">System.Collections.Hashtable</span></span>

## <span data-ttu-id="8f6b3-175">輸出</span><span class="sxs-lookup"><span data-stu-id="8f6b3-175">OUTPUTS</span></span>

### <span data-ttu-id="8f6b3-176">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span><span class="sxs-lookup"><span data-stu-id="8f6b3-176">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="8f6b3-177">筆記</span><span class="sxs-lookup"><span data-stu-id="8f6b3-177">NOTES</span></span>

## <span data-ttu-id="8f6b3-178">相關連結</span><span class="sxs-lookup"><span data-stu-id="8f6b3-178">RELATED LINKS</span></span>
