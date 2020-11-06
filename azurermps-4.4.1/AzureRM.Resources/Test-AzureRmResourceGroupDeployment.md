---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 0143CE35-3B1D-4829-B880-A5CA25B83883
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Test-AzureRmResourceGroupDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Test-AzureRmResourceGroupDeployment.md
ms.openlocfilehash: b357215bf2c4ba032ca44e37cc445e12606aeffe
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93449542"
---
# <span data-ttu-id="94202-101">Test-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="94202-101">Test-AzureRmResourceGroupDeployment</span></span>

## <span data-ttu-id="94202-102">摘要</span><span class="sxs-lookup"><span data-stu-id="94202-102">SYNOPSIS</span></span>
<span data-ttu-id="94202-103">驗證資源群組部署。</span><span class="sxs-lookup"><span data-stu-id="94202-103">Validates a resource group deployment.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="94202-104">句法</span><span class="sxs-lookup"><span data-stu-id="94202-104">SYNTAX</span></span>

### <span data-ttu-id="94202-105">透過不含參數的範本檔案進行部署 (預設) </span><span class="sxs-lookup"><span data-stu-id="94202-105">Deployment via template file without parameters (Default)</span></span>
```
Test-AzureRmResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] -TemplateFile <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="94202-106">透過 [範本檔案] 和 [範本參數] 物件進行部署</span><span class="sxs-lookup"><span data-stu-id="94202-106">Deployment via template file and template parameters object</span></span>
```
Test-AzureRmResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>]
 -TemplateParameterObject <Hashtable> -TemplateFile <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="94202-107">透過範本 uri 與範本參數物件進行部署</span><span class="sxs-lookup"><span data-stu-id="94202-107">Deployment via template uri and template parameters object</span></span>
```
Test-AzureRmResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>]
 -TemplateParameterObject <Hashtable> -TemplateUri <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="94202-108">透過範本檔案和範本參數檔案進行部署</span><span class="sxs-lookup"><span data-stu-id="94202-108">Deployment via template file and template parameters file</span></span>
```
Test-AzureRmResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>]
 -TemplateParameterFile <String> -TemplateFile <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="94202-109">透過範本 uri 與範本參數檔進行部署</span><span class="sxs-lookup"><span data-stu-id="94202-109">Deployment via template uri and template parameters file</span></span>
```
Test-AzureRmResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>]
 -TemplateParameterFile <String> -TemplateUri <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="94202-110">透過範本檔案範本參數 uri 進行部署</span><span class="sxs-lookup"><span data-stu-id="94202-110">Deployment via template file template parameters uri</span></span>
```
Test-AzureRmResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>]
 -TemplateParameterUri <String> -TemplateFile <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="94202-111">透過範本 uri 與範本參數 uri 進行部署</span><span class="sxs-lookup"><span data-stu-id="94202-111">Deployment via template uri and template parameters uri</span></span>
```
Test-AzureRmResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>]
 -TemplateParameterUri <String> -TemplateUri <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="94202-112">透過不含參數的範本 uri 進行部署</span><span class="sxs-lookup"><span data-stu-id="94202-112">Deployment via template uri without parameters</span></span>
```
Test-AzureRmResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] -TemplateUri <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="94202-113">說明</span><span class="sxs-lookup"><span data-stu-id="94202-113">DESCRIPTION</span></span>
<span data-ttu-id="94202-114">**Test AzureRmResourceGroupDeployment** Cmdlet 會判斷 Azure 資源群組部署範本及其參數值是否有效。</span><span class="sxs-lookup"><span data-stu-id="94202-114">The **Test-AzureRmResourceGroupDeployment** cmdlet determines whether an Azure resource group deployment template and its parameter values are valid.</span></span>

## <span data-ttu-id="94202-115">示例</span><span class="sxs-lookup"><span data-stu-id="94202-115">EXAMPLES</span></span>

## <span data-ttu-id="94202-116">參數</span><span class="sxs-lookup"><span data-stu-id="94202-116">PARAMETERS</span></span>

### <span data-ttu-id="94202-117">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="94202-117">-ApiVersion</span></span>
<span data-ttu-id="94202-118">指定資源提供者支援的 API 版本。</span><span class="sxs-lookup"><span data-stu-id="94202-118">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="94202-119">您可以指定不同于預設版本的版本。</span><span class="sxs-lookup"><span data-stu-id="94202-119">You can specify a different version than the default version.</span></span>

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

### <span data-ttu-id="94202-120">模式</span><span class="sxs-lookup"><span data-stu-id="94202-120">-Mode</span></span>
<span data-ttu-id="94202-121">指定部署模式。</span><span class="sxs-lookup"><span data-stu-id="94202-121">Specifies the deployment mode.</span></span>
<span data-ttu-id="94202-122">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="94202-122">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="94202-123">少量</span><span class="sxs-lookup"><span data-stu-id="94202-123">Incremental</span></span>
- <span data-ttu-id="94202-124">完備</span><span class="sxs-lookup"><span data-stu-id="94202-124">Complete</span></span>

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

### <span data-ttu-id="94202-125">-預先</span><span class="sxs-lookup"><span data-stu-id="94202-125">-Pre</span></span>
<span data-ttu-id="94202-126">表示此 Cmdlet 會在自動決定要使用哪個版本時，考慮預發行 API 版本。</span><span class="sxs-lookup"><span data-stu-id="94202-126">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="94202-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="94202-127">-ResourceGroupName</span></span>
<span data-ttu-id="94202-128">指定要測試之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="94202-128">Specifies the name of the resource group to test.</span></span>

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

### <span data-ttu-id="94202-129">-TemplateFile</span><span class="sxs-lookup"><span data-stu-id="94202-129">-TemplateFile</span></span>
<span data-ttu-id="94202-130">指定 JSON 範本檔的完整路徑。</span><span class="sxs-lookup"><span data-stu-id="94202-130">Specifies the full path of a JSON template file.</span></span>

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

### <span data-ttu-id="94202-131">-TemplateParameterFile</span><span class="sxs-lookup"><span data-stu-id="94202-131">-TemplateParameterFile</span></span>
<span data-ttu-id="94202-132">指定包含範本參數之名稱和值的 JSON 檔案的完整路徑。</span><span class="sxs-lookup"><span data-stu-id="94202-132">Specifies the full path of a JSON file that contains the names and values of the template parameters.</span></span>

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

### <span data-ttu-id="94202-133">-TemplateParameterObject</span><span class="sxs-lookup"><span data-stu-id="94202-133">-TemplateParameterObject</span></span>
<span data-ttu-id="94202-134">指定範本參數名稱和值的雜湊表。</span><span class="sxs-lookup"><span data-stu-id="94202-134">Specifies a hash table of template parameter names and values.</span></span>

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

### <span data-ttu-id="94202-135">-TemplateParameterUri</span><span class="sxs-lookup"><span data-stu-id="94202-135">-TemplateParameterUri</span></span>
<span data-ttu-id="94202-136">指定範本參數檔的 URI。</span><span class="sxs-lookup"><span data-stu-id="94202-136">Specifies the URI of a template parameters file.</span></span>

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

### <span data-ttu-id="94202-137">-TemplateUri</span><span class="sxs-lookup"><span data-stu-id="94202-137">-TemplateUri</span></span>
<span data-ttu-id="94202-138">指定 JSON 範本檔案的 URI。</span><span class="sxs-lookup"><span data-stu-id="94202-138">Specifies the URI of a JSON template file.</span></span>

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

### <span data-ttu-id="94202-139">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="94202-139">-DefaultProfile</span></span>
<span data-ttu-id="94202-140">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="94202-140">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="94202-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="94202-141">CommonParameters</span></span>
<span data-ttu-id="94202-142">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="94202-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="94202-143">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="94202-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="94202-144">輸入</span><span class="sxs-lookup"><span data-stu-id="94202-144">INPUTS</span></span>

## <span data-ttu-id="94202-145">輸出</span><span class="sxs-lookup"><span data-stu-id="94202-145">OUTPUTS</span></span>

### <span data-ttu-id="94202-146">[System.object]。清單 ' 1 [PSResourceManagerError] SdkModels. 命令.]</span><span class="sxs-lookup"><span data-stu-id="94202-146">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceManagerError]</span></span>

## <span data-ttu-id="94202-147">筆記</span><span class="sxs-lookup"><span data-stu-id="94202-147">NOTES</span></span>

## <span data-ttu-id="94202-148">相關連結</span><span class="sxs-lookup"><span data-stu-id="94202-148">RELATED LINKS</span></span>

[<span data-ttu-id="94202-149">AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="94202-149">Get-AzureRmResourceGroupDeployment</span></span>](./Get-AzureRmResourceGroupDeployment.md)

[<span data-ttu-id="94202-150">新-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="94202-150">New-AzureRmResourceGroupDeployment</span></span>](./New-AzureRmResourceGroupDeployment.md)

[<span data-ttu-id="94202-151">移除-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="94202-151">Remove-AzureRmResourceGroupDeployment</span></span>](./Remove-AzureRmResourceGroupDeployment.md)

[<span data-ttu-id="94202-152">停止 AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="94202-152">Stop-AzureRmResourceGroupDeployment</span></span>](./Stop-AzureRmResourceGroupDeployment.md)


