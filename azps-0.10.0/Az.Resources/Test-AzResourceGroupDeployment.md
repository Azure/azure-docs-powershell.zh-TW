---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 0143CE35-3B1D-4829-B880-A5CA25B83883
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/test-Azresourcegroupdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Test-AzResourceGroupDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Test-AzResourceGroupDeployment.md
ms.openlocfilehash: 59bbe7c5309764c41f22aaa99dbb4d47a23f1ba8
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/16/2020
ms.locfileid: "93795187"
---
# <span data-ttu-id="375cd-101">Test-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="375cd-101">Test-AzResourceGroupDeployment</span></span>

## <span data-ttu-id="375cd-102">摘要</span><span class="sxs-lookup"><span data-stu-id="375cd-102">SYNOPSIS</span></span>
<span data-ttu-id="375cd-103">驗證資源群組部署。</span><span class="sxs-lookup"><span data-stu-id="375cd-103">Validates a resource group deployment.</span></span>

## <span data-ttu-id="375cd-104">句法</span><span class="sxs-lookup"><span data-stu-id="375cd-104">SYNTAX</span></span>

### <span data-ttu-id="375cd-105">ByTemplateFileWithNoParameters (預設) </span><span class="sxs-lookup"><span data-stu-id="375cd-105">ByTemplateFileWithNoParameters (Default)</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-RollbackToLastDeployment] [-RollBackDeploymentName <String>] -TemplateFile <String> [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="375cd-106">ByTemplateFileAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="375cd-106">ByTemplateFileAndParameterObject</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-RollbackToLastDeployment] [-RollBackDeploymentName <String>] -TemplateParameterObject <Hashtable>
 -TemplateFile <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="375cd-107">ByTemplateUriAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="375cd-107">ByTemplateUriAndParameterObject</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-RollbackToLastDeployment] [-RollBackDeploymentName <String>] -TemplateParameterObject <Hashtable>
 -TemplateUri <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="375cd-108">ByTemplateFileAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="375cd-108">ByTemplateFileAndParameterFile</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-RollbackToLastDeployment] [-RollBackDeploymentName <String>] -TemplateParameterFile <String>
 -TemplateFile <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="375cd-109">ByTemplateUriAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="375cd-109">ByTemplateUriAndParameterFile</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-RollbackToLastDeployment] [-RollBackDeploymentName <String>] -TemplateParameterFile <String>
 -TemplateUri <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="375cd-110">ByTemplateFileAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="375cd-110">ByTemplateFileAndParameterUri</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-RollbackToLastDeployment] [-RollBackDeploymentName <String>] -TemplateParameterUri <String>
 -TemplateFile <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="375cd-111">ByTemplateUriAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="375cd-111">ByTemplateUriAndParameterUri</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-RollbackToLastDeployment] [-RollBackDeploymentName <String>] -TemplateParameterUri <String>
 -TemplateUri <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="375cd-112">ByTemplateUriWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="375cd-112">ByTemplateUriWithNoParameters</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-RollbackToLastDeployment] [-RollBackDeploymentName <String>] -TemplateUri <String> [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="375cd-113">說明</span><span class="sxs-lookup"><span data-stu-id="375cd-113">DESCRIPTION</span></span>
<span data-ttu-id="375cd-114">**Test AzResourceGroupDeployment** Cmdlet 會判斷 Azure 資源群組部署範本及其參數值是否有效。</span><span class="sxs-lookup"><span data-stu-id="375cd-114">The **Test-AzResourceGroupDeployment** cmdlet determines whether an Azure resource group deployment template and its parameter values are valid.</span></span>

## <span data-ttu-id="375cd-115">示例</span><span class="sxs-lookup"><span data-stu-id="375cd-115">EXAMPLES</span></span>

## <span data-ttu-id="375cd-116">參數</span><span class="sxs-lookup"><span data-stu-id="375cd-116">PARAMETERS</span></span>

### <span data-ttu-id="375cd-117">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="375cd-117">-ApiVersion</span></span>
<span data-ttu-id="375cd-118">指定資源提供者支援的 API 版本。</span><span class="sxs-lookup"><span data-stu-id="375cd-118">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="375cd-119">您可以指定不同于預設版本的版本。</span><span class="sxs-lookup"><span data-stu-id="375cd-119">You can specify a different version than the default version.</span></span>

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

### <span data-ttu-id="375cd-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="375cd-120">-DefaultProfile</span></span>
<span data-ttu-id="375cd-121">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="375cd-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="375cd-122">模式</span><span class="sxs-lookup"><span data-stu-id="375cd-122">-Mode</span></span>
<span data-ttu-id="375cd-123">指定部署模式。</span><span class="sxs-lookup"><span data-stu-id="375cd-123">Specifies the deployment mode.</span></span>
<span data-ttu-id="375cd-124">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="375cd-124">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="375cd-125">少量</span><span class="sxs-lookup"><span data-stu-id="375cd-125">Incremental</span></span>
- <span data-ttu-id="375cd-126">完備</span><span class="sxs-lookup"><span data-stu-id="375cd-126">Complete</span></span>

```yaml
Type: Microsoft.Azure.Management.ResourceManager.Models.DeploymentMode
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="375cd-127">-預先</span><span class="sxs-lookup"><span data-stu-id="375cd-127">-Pre</span></span>
<span data-ttu-id="375cd-128">表示此 Cmdlet 會在自動決定要使用哪個版本時，考慮預發行 API 版本。</span><span class="sxs-lookup"><span data-stu-id="375cd-128">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="375cd-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="375cd-129">-ResourceGroupName</span></span>
<span data-ttu-id="375cd-130">指定要測試之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="375cd-130">Specifies the name of the resource group to test.</span></span>

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

### <span data-ttu-id="375cd-131">-RollBackDeploymentName</span><span class="sxs-lookup"><span data-stu-id="375cd-131">-RollBackDeploymentName</span></span>
<span data-ttu-id="375cd-132">如果使用了-RollbackToLastDeployment，則會使用資源群組中的指定名稱回滾到成功的部署。</span><span class="sxs-lookup"><span data-stu-id="375cd-132">Rollback to the successful deployment with the given name in the resource group, should not be used if -RollbackToLastDeployment is used.</span></span>

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

### <span data-ttu-id="375cd-133">-RollbackToLastDeployment</span><span class="sxs-lookup"><span data-stu-id="375cd-133">-RollbackToLastDeployment</span></span>
<span data-ttu-id="375cd-134">如果使用-RollBackDeploymentName，則回退至 [資源] 群組中的最後一個成功部署。</span><span class="sxs-lookup"><span data-stu-id="375cd-134">Rollback to the last successful deployment in the resource group, should not be present if -RollBackDeploymentName is used.</span></span>

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

### <span data-ttu-id="375cd-135">-TemplateFile</span><span class="sxs-lookup"><span data-stu-id="375cd-135">-TemplateFile</span></span>
<span data-ttu-id="375cd-136">指定 JSON 範本檔的完整路徑。</span><span class="sxs-lookup"><span data-stu-id="375cd-136">Specifies the full path of a JSON template file.</span></span>

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

### <span data-ttu-id="375cd-137">-TemplateParameterFile</span><span class="sxs-lookup"><span data-stu-id="375cd-137">-TemplateParameterFile</span></span>
<span data-ttu-id="375cd-138">指定包含範本參數之名稱和值的 JSON 檔案的完整路徑。</span><span class="sxs-lookup"><span data-stu-id="375cd-138">Specifies the full path of a JSON file that contains the names and values of the template parameters.</span></span>

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

### <span data-ttu-id="375cd-139">-TemplateParameterObject</span><span class="sxs-lookup"><span data-stu-id="375cd-139">-TemplateParameterObject</span></span>
<span data-ttu-id="375cd-140">指定範本參數名稱和值的雜湊表。</span><span class="sxs-lookup"><span data-stu-id="375cd-140">Specifies a hash table of template parameter names and values.</span></span>

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

### <span data-ttu-id="375cd-141">-TemplateParameterUri</span><span class="sxs-lookup"><span data-stu-id="375cd-141">-TemplateParameterUri</span></span>
<span data-ttu-id="375cd-142">指定範本參數檔的 URI。</span><span class="sxs-lookup"><span data-stu-id="375cd-142">Specifies the URI of a template parameters file.</span></span>

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

### <span data-ttu-id="375cd-143">-TemplateUri</span><span class="sxs-lookup"><span data-stu-id="375cd-143">-TemplateUri</span></span>
<span data-ttu-id="375cd-144">指定 JSON 範本檔案的 URI。</span><span class="sxs-lookup"><span data-stu-id="375cd-144">Specifies the URI of a JSON template file.</span></span>

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

### <span data-ttu-id="375cd-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="375cd-145">CommonParameters</span></span>
<span data-ttu-id="375cd-146">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="375cd-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="375cd-147">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="375cd-147">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="375cd-148">輸入</span><span class="sxs-lookup"><span data-stu-id="375cd-148">INPUTS</span></span>

### <span data-ttu-id="375cd-149">所有</span><span class="sxs-lookup"><span data-stu-id="375cd-149">None</span></span>

## <span data-ttu-id="375cd-150">輸出</span><span class="sxs-lookup"><span data-stu-id="375cd-150">OUTPUTS</span></span>

### <span data-ttu-id="375cd-151">PSResourceManagerError 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="375cd-151">Microsoft.Azure.Commands.ResourceManager.Models.PSResourceManagerError</span></span>

## <span data-ttu-id="375cd-152">筆記</span><span class="sxs-lookup"><span data-stu-id="375cd-152">NOTES</span></span>

## <span data-ttu-id="375cd-153">相關連結</span><span class="sxs-lookup"><span data-stu-id="375cd-153">RELATED LINKS</span></span>

[<span data-ttu-id="375cd-154">AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="375cd-154">Get-AzResourceGroupDeployment</span></span>](./Get-AzResourceGroupDeployment.md)

[<span data-ttu-id="375cd-155">新-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="375cd-155">New-AzResourceGroupDeployment</span></span>](./New-AzResourceGroupDeployment.md)

[<span data-ttu-id="375cd-156">移除-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="375cd-156">Remove-AzResourceGroupDeployment</span></span>](./Remove-AzResourceGroupDeployment.md)

[<span data-ttu-id="375cd-157">停止 AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="375cd-157">Stop-AzResourceGroupDeployment</span></span>](./Stop-AzResourceGroupDeployment.md)


