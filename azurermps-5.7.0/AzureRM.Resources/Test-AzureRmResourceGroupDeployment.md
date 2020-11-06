---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 0143CE35-3B1D-4829-B880-A5CA25B83883
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/test-azurermresourcegroupdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Test-AzureRmResourceGroupDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Test-AzureRmResourceGroupDeployment.md
ms.openlocfilehash: 0caf541aeadcbf2617ae5d31d0dfaf69e432e888
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93454103"
---
# <span data-ttu-id="e5aaf-101">Test-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="e5aaf-101">Test-AzureRmResourceGroupDeployment</span></span>

## <span data-ttu-id="e5aaf-102">摘要</span><span class="sxs-lookup"><span data-stu-id="e5aaf-102">SYNOPSIS</span></span>
<span data-ttu-id="e5aaf-103">驗證資源群組部署。</span><span class="sxs-lookup"><span data-stu-id="e5aaf-103">Validates a resource group deployment.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e5aaf-104">句法</span><span class="sxs-lookup"><span data-stu-id="e5aaf-104">SYNTAX</span></span>

### <span data-ttu-id="e5aaf-105">ByTemplateFileWithNoParameters (預設) </span><span class="sxs-lookup"><span data-stu-id="e5aaf-105">ByTemplateFileWithNoParameters (Default)</span></span>
```
Test-AzureRmResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] -TemplateFile <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e5aaf-106">ByTemplateFileAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="e5aaf-106">ByTemplateFileAndParameterObject</span></span>
```
Test-AzureRmResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>]
 -TemplateParameterObject <Hashtable> -TemplateFile <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e5aaf-107">ByTemplateUriAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="e5aaf-107">ByTemplateUriAndParameterObject</span></span>
```
Test-AzureRmResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>]
 -TemplateParameterObject <Hashtable> -TemplateUri <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e5aaf-108">ByTemplateFileAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="e5aaf-108">ByTemplateFileAndParameterFile</span></span>
```
Test-AzureRmResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>]
 -TemplateParameterFile <String> -TemplateFile <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e5aaf-109">ByTemplateUriAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="e5aaf-109">ByTemplateUriAndParameterFile</span></span>
```
Test-AzureRmResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>]
 -TemplateParameterFile <String> -TemplateUri <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e5aaf-110">ByTemplateFileAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="e5aaf-110">ByTemplateFileAndParameterUri</span></span>
```
Test-AzureRmResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>]
 -TemplateParameterUri <String> -TemplateFile <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e5aaf-111">ByTemplateUriAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="e5aaf-111">ByTemplateUriAndParameterUri</span></span>
```
Test-AzureRmResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>]
 -TemplateParameterUri <String> -TemplateUri <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e5aaf-112">ByTemplateUriWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="e5aaf-112">ByTemplateUriWithNoParameters</span></span>
```
Test-AzureRmResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] -TemplateUri <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e5aaf-113">說明</span><span class="sxs-lookup"><span data-stu-id="e5aaf-113">DESCRIPTION</span></span>
<span data-ttu-id="e5aaf-114">**Test AzureRmResourceGroupDeployment** Cmdlet 會判斷 Azure 資源群組部署範本及其參數值是否有效。</span><span class="sxs-lookup"><span data-stu-id="e5aaf-114">The **Test-AzureRmResourceGroupDeployment** cmdlet determines whether an Azure resource group deployment template and its parameter values are valid.</span></span>

## <span data-ttu-id="e5aaf-115">示例</span><span class="sxs-lookup"><span data-stu-id="e5aaf-115">EXAMPLES</span></span>

## <span data-ttu-id="e5aaf-116">參數</span><span class="sxs-lookup"><span data-stu-id="e5aaf-116">PARAMETERS</span></span>

### <span data-ttu-id="e5aaf-117">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="e5aaf-117">-ApiVersion</span></span>
<span data-ttu-id="e5aaf-118">指定資源提供者支援的 API 版本。</span><span class="sxs-lookup"><span data-stu-id="e5aaf-118">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="e5aaf-119">您可以指定不同于預設版本的版本。</span><span class="sxs-lookup"><span data-stu-id="e5aaf-119">You can specify a different version than the default version.</span></span>

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

### <span data-ttu-id="e5aaf-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e5aaf-120">-DefaultProfile</span></span>
<span data-ttu-id="e5aaf-121">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="e5aaf-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e5aaf-122">模式</span><span class="sxs-lookup"><span data-stu-id="e5aaf-122">-Mode</span></span>
<span data-ttu-id="e5aaf-123">指定部署模式。</span><span class="sxs-lookup"><span data-stu-id="e5aaf-123">Specifies the deployment mode.</span></span>
<span data-ttu-id="e5aaf-124">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="e5aaf-124">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="e5aaf-125">少量</span><span class="sxs-lookup"><span data-stu-id="e5aaf-125">Incremental</span></span>
- <span data-ttu-id="e5aaf-126">完備</span><span class="sxs-lookup"><span data-stu-id="e5aaf-126">Complete</span></span>

```yaml
Type: DeploymentMode
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e5aaf-127">-預先</span><span class="sxs-lookup"><span data-stu-id="e5aaf-127">-Pre</span></span>
<span data-ttu-id="e5aaf-128">表示此 Cmdlet 會在自動決定要使用哪個版本時，考慮預發行 API 版本。</span><span class="sxs-lookup"><span data-stu-id="e5aaf-128">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="e5aaf-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e5aaf-129">-ResourceGroupName</span></span>
<span data-ttu-id="e5aaf-130">指定要測試之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="e5aaf-130">Specifies the name of the resource group to test.</span></span>

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

### <span data-ttu-id="e5aaf-131">-TemplateFile</span><span class="sxs-lookup"><span data-stu-id="e5aaf-131">-TemplateFile</span></span>
<span data-ttu-id="e5aaf-132">指定 JSON 範本檔的完整路徑。</span><span class="sxs-lookup"><span data-stu-id="e5aaf-132">Specifies the full path of a JSON template file.</span></span>

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

### <span data-ttu-id="e5aaf-133">-TemplateParameterFile</span><span class="sxs-lookup"><span data-stu-id="e5aaf-133">-TemplateParameterFile</span></span>
<span data-ttu-id="e5aaf-134">指定包含範本參數之名稱和值的 JSON 檔案的完整路徑。</span><span class="sxs-lookup"><span data-stu-id="e5aaf-134">Specifies the full path of a JSON file that contains the names and values of the template parameters.</span></span>

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

### <span data-ttu-id="e5aaf-135">-TemplateParameterObject</span><span class="sxs-lookup"><span data-stu-id="e5aaf-135">-TemplateParameterObject</span></span>
<span data-ttu-id="e5aaf-136">指定範本參數名稱和值的雜湊表。</span><span class="sxs-lookup"><span data-stu-id="e5aaf-136">Specifies a hash table of template parameter names and values.</span></span>

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

### <span data-ttu-id="e5aaf-137">-TemplateParameterUri</span><span class="sxs-lookup"><span data-stu-id="e5aaf-137">-TemplateParameterUri</span></span>
<span data-ttu-id="e5aaf-138">指定範本參數檔的 URI。</span><span class="sxs-lookup"><span data-stu-id="e5aaf-138">Specifies the URI of a template parameters file.</span></span>

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

### <span data-ttu-id="e5aaf-139">-TemplateUri</span><span class="sxs-lookup"><span data-stu-id="e5aaf-139">-TemplateUri</span></span>
<span data-ttu-id="e5aaf-140">指定 JSON 範本檔案的 URI。</span><span class="sxs-lookup"><span data-stu-id="e5aaf-140">Specifies the URI of a JSON template file.</span></span>

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

### <span data-ttu-id="e5aaf-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e5aaf-141">CommonParameters</span></span>
<span data-ttu-id="e5aaf-142">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="e5aaf-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e5aaf-143">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="e5aaf-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e5aaf-144">輸入</span><span class="sxs-lookup"><span data-stu-id="e5aaf-144">INPUTS</span></span>

### <span data-ttu-id="e5aaf-145">所有</span><span class="sxs-lookup"><span data-stu-id="e5aaf-145">None</span></span>
<span data-ttu-id="e5aaf-146">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="e5aaf-146">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="e5aaf-147">輸出</span><span class="sxs-lookup"><span data-stu-id="e5aaf-147">OUTPUTS</span></span>

### <span data-ttu-id="e5aaf-148">[System.object]。清單 ' 1 [PSResourceManagerError] SdkModels. 命令.]</span><span class="sxs-lookup"><span data-stu-id="e5aaf-148">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceManagerError]</span></span>

## <span data-ttu-id="e5aaf-149">筆記</span><span class="sxs-lookup"><span data-stu-id="e5aaf-149">NOTES</span></span>

## <span data-ttu-id="e5aaf-150">相關連結</span><span class="sxs-lookup"><span data-stu-id="e5aaf-150">RELATED LINKS</span></span>

[<span data-ttu-id="e5aaf-151">AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="e5aaf-151">Get-AzureRmResourceGroupDeployment</span></span>](./Get-AzureRmResourceGroupDeployment.md)

[<span data-ttu-id="e5aaf-152">新-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="e5aaf-152">New-AzureRmResourceGroupDeployment</span></span>](./New-AzureRmResourceGroupDeployment.md)

[<span data-ttu-id="e5aaf-153">移除-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="e5aaf-153">Remove-AzureRmResourceGroupDeployment</span></span>](./Remove-AzureRmResourceGroupDeployment.md)

[<span data-ttu-id="e5aaf-154">停止 AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="e5aaf-154">Stop-AzureRmResourceGroupDeployment</span></span>](./Stop-AzureRmResourceGroupDeployment.md)


