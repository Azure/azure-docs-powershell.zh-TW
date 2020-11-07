---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/test-azurermdeployment
schema: 2.0.0
ms.openlocfilehash: 51d0405ffbedf5ad5a708fdcf9184ef49dc6ecdb
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/15/2020
ms.locfileid: "93801126"
---
# <span data-ttu-id="d1e2e-101">Test-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="d1e2e-101">Test-AzureRmDeployment</span></span>

## <span data-ttu-id="d1e2e-102">摘要</span><span class="sxs-lookup"><span data-stu-id="d1e2e-102">SYNOPSIS</span></span>
<span data-ttu-id="d1e2e-103">驗證部署。</span><span class="sxs-lookup"><span data-stu-id="d1e2e-103">Validates a deployment.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d1e2e-104">句法</span><span class="sxs-lookup"><span data-stu-id="d1e2e-104">SYNTAX</span></span>

### <span data-ttu-id="d1e2e-105">ByTemplateFileWithNoParameters (預設) </span><span class="sxs-lookup"><span data-stu-id="d1e2e-105">ByTemplateFileWithNoParameters (Default)</span></span>
```
Test-AzureRmDeployment -Location <String> -TemplateFile <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d1e2e-106">ByTemplateFileAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="d1e2e-106">ByTemplateFileAndParameterObject</span></span>
```
Test-AzureRmDeployment -Location <String> -TemplateParameterObject <Hashtable> -TemplateFile <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d1e2e-107">ByTemplateUriAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="d1e2e-107">ByTemplateUriAndParameterObject</span></span>
```
Test-AzureRmDeployment -Location <String> -TemplateParameterObject <Hashtable> -TemplateUri <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d1e2e-108">ByTemplateFileAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="d1e2e-108">ByTemplateFileAndParameterFile</span></span>
```
Test-AzureRmDeployment -Location <String> -TemplateParameterFile <String> -TemplateFile <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d1e2e-109">ByTemplateUriAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="d1e2e-109">ByTemplateUriAndParameterFile</span></span>
```
Test-AzureRmDeployment -Location <String> -TemplateParameterFile <String> -TemplateUri <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d1e2e-110">ByTemplateFileAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="d1e2e-110">ByTemplateFileAndParameterUri</span></span>
```
Test-AzureRmDeployment -Location <String> -TemplateParameterUri <String> -TemplateFile <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d1e2e-111">ByTemplateUriAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="d1e2e-111">ByTemplateUriAndParameterUri</span></span>
```
Test-AzureRmDeployment -Location <String> -TemplateParameterUri <String> -TemplateUri <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d1e2e-112">ByTemplateUriWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="d1e2e-112">ByTemplateUriWithNoParameters</span></span>
```
Test-AzureRmDeployment -Location <String> -TemplateUri <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d1e2e-113">說明</span><span class="sxs-lookup"><span data-stu-id="d1e2e-113">DESCRIPTION</span></span>
<span data-ttu-id="d1e2e-114">**Test AzureRmDeployment** Cmdlet 會判斷部署範本及其參數值是否有效。</span><span class="sxs-lookup"><span data-stu-id="d1e2e-114">The **Test-AzureRmDeployment** cmdlet determines whether a deployment template and its parameter values are valid.</span></span>

## <span data-ttu-id="d1e2e-115">示例</span><span class="sxs-lookup"><span data-stu-id="d1e2e-115">EXAMPLES</span></span>

### <span data-ttu-id="d1e2e-116">範例1：使用自訂範本和參數檔案測試部署</span><span class="sxs-lookup"><span data-stu-id="d1e2e-116">Example 1: Test deployment with a custom template and parameter file</span></span>
```
PS C:\>Test-AzureRmDeployment -Location "West US" -TemplateFile "D:\Azure\Templates\EngineeringSite.json" -TemplateParameterFile "D:\Azure\Templates\EngSiteParms.json"
```

<span data-ttu-id="d1e2e-117">這個命令會使用指定的範本檔案和參數檔案，在目前的訂閱範圍內測試部署。</span><span class="sxs-lookup"><span data-stu-id="d1e2e-117">This command tests a deployment at the current subscription scope using the given template file and parameters file.</span></span>

## <span data-ttu-id="d1e2e-118">參數</span><span class="sxs-lookup"><span data-stu-id="d1e2e-118">PARAMETERS</span></span>

### <span data-ttu-id="d1e2e-119">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="d1e2e-119">-ApiVersion</span></span>
<span data-ttu-id="d1e2e-120">設定時，會指出要使用的資源提供者 API 版本。</span><span class="sxs-lookup"><span data-stu-id="d1e2e-120">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="d1e2e-121">如果未指定，API 版本會自動決定為最新的可用。</span><span class="sxs-lookup"><span data-stu-id="d1e2e-121">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="d1e2e-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d1e2e-122">-DefaultProfile</span></span>
<span data-ttu-id="d1e2e-123">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="d1e2e-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d1e2e-124">-位置</span><span class="sxs-lookup"><span data-stu-id="d1e2e-124">-Location</span></span>
<span data-ttu-id="d1e2e-125">儲存部署資料的位置。</span><span class="sxs-lookup"><span data-stu-id="d1e2e-125">The location to store deployment data.</span></span>

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

### <span data-ttu-id="d1e2e-126">-預先</span><span class="sxs-lookup"><span data-stu-id="d1e2e-126">-Pre</span></span>
<span data-ttu-id="d1e2e-127">設定時，表示 Cmdlet 應該使用預發行 API 版本，以便自動判斷要使用的版本。</span><span class="sxs-lookup"><span data-stu-id="d1e2e-127">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="d1e2e-128">-TemplateFile</span><span class="sxs-lookup"><span data-stu-id="d1e2e-128">-TemplateFile</span></span>
<span data-ttu-id="d1e2e-129">範本檔案的本機路徑。</span><span class="sxs-lookup"><span data-stu-id="d1e2e-129">Local path to the template file.</span></span>

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

### <span data-ttu-id="d1e2e-130">-TemplateParameterFile</span><span class="sxs-lookup"><span data-stu-id="d1e2e-130">-TemplateParameterFile</span></span>
<span data-ttu-id="d1e2e-131">具有範本參數的檔案。</span><span class="sxs-lookup"><span data-stu-id="d1e2e-131">A file that has the template parameters.</span></span>

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

### <span data-ttu-id="d1e2e-132">-TemplateParameterObject</span><span class="sxs-lookup"><span data-stu-id="d1e2e-132">-TemplateParameterObject</span></span>
<span data-ttu-id="d1e2e-133">代表參數的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="d1e2e-133">A hash table which represents the parameters.</span></span>

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

### <span data-ttu-id="d1e2e-134">-TemplateParameterUri</span><span class="sxs-lookup"><span data-stu-id="d1e2e-134">-TemplateParameterUri</span></span>
<span data-ttu-id="d1e2e-135">範本參數檔的 Uri。</span><span class="sxs-lookup"><span data-stu-id="d1e2e-135">Uri to the template parameter file.</span></span>

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

### <span data-ttu-id="d1e2e-136">-TemplateUri</span><span class="sxs-lookup"><span data-stu-id="d1e2e-136">-TemplateUri</span></span>
<span data-ttu-id="d1e2e-137">範本檔案的 Uri。</span><span class="sxs-lookup"><span data-stu-id="d1e2e-137">Uri to the template file.</span></span>

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

### <span data-ttu-id="d1e2e-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d1e2e-138">CommonParameters</span></span>
<span data-ttu-id="d1e2e-139">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="d1e2e-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d1e2e-140">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="d1e2e-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d1e2e-141">輸入</span><span class="sxs-lookup"><span data-stu-id="d1e2e-141">INPUTS</span></span>

### <span data-ttu-id="d1e2e-142">System.object</span><span class="sxs-lookup"><span data-stu-id="d1e2e-142">System.String</span></span>
<span data-ttu-id="d1e2e-143">DeploymentMode 集合. Hashtable. 雜湊表。</span><span class="sxs-lookup"><span data-stu-id="d1e2e-143">Microsoft.Azure.Management.ResourceManager.Models.DeploymentMode System.Collections.Hashtable</span></span>

## <span data-ttu-id="d1e2e-144">輸出</span><span class="sxs-lookup"><span data-stu-id="d1e2e-144">OUTPUTS</span></span>

### <span data-ttu-id="d1e2e-145">PSResourceManagerError 中的 SdkModels （）</span><span class="sxs-lookup"><span data-stu-id="d1e2e-145">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceManagerError</span></span>

## <span data-ttu-id="d1e2e-146">筆記</span><span class="sxs-lookup"><span data-stu-id="d1e2e-146">NOTES</span></span>

## <span data-ttu-id="d1e2e-147">相關連結</span><span class="sxs-lookup"><span data-stu-id="d1e2e-147">RELATED LINKS</span></span>
