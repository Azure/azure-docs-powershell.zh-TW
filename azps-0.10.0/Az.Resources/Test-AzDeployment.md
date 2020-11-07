---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/test-Azdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Test-AzDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Test-AzDeployment.md
ms.openlocfilehash: 77c2a712a3d44d963fd08642d1a1c88b5d8c81e1
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/16/2020
ms.locfileid: "93795189"
---
# <span data-ttu-id="9e66e-101">Test-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="9e66e-101">Test-AzDeployment</span></span>

## <span data-ttu-id="9e66e-102">摘要</span><span class="sxs-lookup"><span data-stu-id="9e66e-102">SYNOPSIS</span></span>
<span data-ttu-id="9e66e-103">驗證部署。</span><span class="sxs-lookup"><span data-stu-id="9e66e-103">Validates a deployment.</span></span>

## <span data-ttu-id="9e66e-104">句法</span><span class="sxs-lookup"><span data-stu-id="9e66e-104">SYNTAX</span></span>

### <span data-ttu-id="9e66e-105">ByTemplateFileWithNoParameters (預設) </span><span class="sxs-lookup"><span data-stu-id="9e66e-105">ByTemplateFileWithNoParameters (Default)</span></span>
```
Test-AzDeployment -Location <String> -TemplateFile <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9e66e-106">ByTemplateFileAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="9e66e-106">ByTemplateFileAndParameterObject</span></span>
```
Test-AzDeployment -Location <String> -TemplateParameterObject <Hashtable> -TemplateFile <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9e66e-107">ByTemplateUriAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="9e66e-107">ByTemplateUriAndParameterObject</span></span>
```
Test-AzDeployment -Location <String> -TemplateParameterObject <Hashtable> -TemplateUri <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9e66e-108">ByTemplateFileAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="9e66e-108">ByTemplateFileAndParameterFile</span></span>
```
Test-AzDeployment -Location <String> -TemplateParameterFile <String> -TemplateFile <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9e66e-109">ByTemplateUriAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="9e66e-109">ByTemplateUriAndParameterFile</span></span>
```
Test-AzDeployment -Location <String> -TemplateParameterFile <String> -TemplateUri <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9e66e-110">ByTemplateFileAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="9e66e-110">ByTemplateFileAndParameterUri</span></span>
```
Test-AzDeployment -Location <String> -TemplateParameterUri <String> -TemplateFile <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9e66e-111">ByTemplateUriAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="9e66e-111">ByTemplateUriAndParameterUri</span></span>
```
Test-AzDeployment -Location <String> -TemplateParameterUri <String> -TemplateUri <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9e66e-112">ByTemplateUriWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="9e66e-112">ByTemplateUriWithNoParameters</span></span>
```
Test-AzDeployment -Location <String> -TemplateUri <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9e66e-113">說明</span><span class="sxs-lookup"><span data-stu-id="9e66e-113">DESCRIPTION</span></span>
<span data-ttu-id="9e66e-114">**Test AzDeployment** Cmdlet 會判斷部署範本及其參數值是否有效。</span><span class="sxs-lookup"><span data-stu-id="9e66e-114">The **Test-AzDeployment** cmdlet determines whether a deployment template and its parameter values are valid.</span></span>

## <span data-ttu-id="9e66e-115">示例</span><span class="sxs-lookup"><span data-stu-id="9e66e-115">EXAMPLES</span></span>

### <span data-ttu-id="9e66e-116">範例1：使用自訂範本和參數檔案測試部署</span><span class="sxs-lookup"><span data-stu-id="9e66e-116">Example 1: Test deployment with a custom template and parameter file</span></span>
```
PS C:\>Test-AzDeployment -Location "West US" -TemplateFile "D:\Azure\Templates\EngineeringSite.json" -TemplateParameterFile "D:\Azure\Templates\EngSiteParms.json"
```

<span data-ttu-id="9e66e-117">這個命令會使用指定的範本檔案和參數檔案，在目前的訂閱範圍內測試部署。</span><span class="sxs-lookup"><span data-stu-id="9e66e-117">This command tests a deployment at the current subscription scope using the given template file and parameters file.</span></span>

## <span data-ttu-id="9e66e-118">參數</span><span class="sxs-lookup"><span data-stu-id="9e66e-118">PARAMETERS</span></span>

### <span data-ttu-id="9e66e-119">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="9e66e-119">-ApiVersion</span></span>
<span data-ttu-id="9e66e-120">設定時，會指出要使用的資源提供者 API 版本。</span><span class="sxs-lookup"><span data-stu-id="9e66e-120">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="9e66e-121">如果未指定，API 版本會自動決定為最新的可用。</span><span class="sxs-lookup"><span data-stu-id="9e66e-121">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="9e66e-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9e66e-122">-DefaultProfile</span></span>
<span data-ttu-id="9e66e-123">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="9e66e-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9e66e-124">-位置</span><span class="sxs-lookup"><span data-stu-id="9e66e-124">-Location</span></span>
<span data-ttu-id="9e66e-125">儲存部署資料的位置。</span><span class="sxs-lookup"><span data-stu-id="9e66e-125">The location to store deployment data.</span></span>

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

### <span data-ttu-id="9e66e-126">-預先</span><span class="sxs-lookup"><span data-stu-id="9e66e-126">-Pre</span></span>
<span data-ttu-id="9e66e-127">設定時，表示 Cmdlet 應該使用預發行 API 版本，以便自動判斷要使用的版本。</span><span class="sxs-lookup"><span data-stu-id="9e66e-127">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="9e66e-128">-TemplateFile</span><span class="sxs-lookup"><span data-stu-id="9e66e-128">-TemplateFile</span></span>
<span data-ttu-id="9e66e-129">範本檔案的本機路徑。</span><span class="sxs-lookup"><span data-stu-id="9e66e-129">Local path to the template file.</span></span>

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

### <span data-ttu-id="9e66e-130">-TemplateParameterFile</span><span class="sxs-lookup"><span data-stu-id="9e66e-130">-TemplateParameterFile</span></span>
<span data-ttu-id="9e66e-131">具有範本參數的檔案。</span><span class="sxs-lookup"><span data-stu-id="9e66e-131">A file that has the template parameters.</span></span>

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

### <span data-ttu-id="9e66e-132">-TemplateParameterObject</span><span class="sxs-lookup"><span data-stu-id="9e66e-132">-TemplateParameterObject</span></span>
<span data-ttu-id="9e66e-133">代表參數的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="9e66e-133">A hash table which represents the parameters.</span></span>

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

### <span data-ttu-id="9e66e-134">-TemplateParameterUri</span><span class="sxs-lookup"><span data-stu-id="9e66e-134">-TemplateParameterUri</span></span>
<span data-ttu-id="9e66e-135">範本參數檔的 Uri。</span><span class="sxs-lookup"><span data-stu-id="9e66e-135">Uri to the template parameter file.</span></span>

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

### <span data-ttu-id="9e66e-136">-TemplateUri</span><span class="sxs-lookup"><span data-stu-id="9e66e-136">-TemplateUri</span></span>
<span data-ttu-id="9e66e-137">範本檔案的 Uri。</span><span class="sxs-lookup"><span data-stu-id="9e66e-137">Uri to the template file.</span></span>

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

### <span data-ttu-id="9e66e-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9e66e-138">CommonParameters</span></span>
<span data-ttu-id="9e66e-139">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="9e66e-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9e66e-140">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="9e66e-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9e66e-141">輸入</span><span class="sxs-lookup"><span data-stu-id="9e66e-141">INPUTS</span></span>

### <span data-ttu-id="9e66e-142">System.object</span><span class="sxs-lookup"><span data-stu-id="9e66e-142">System.String</span></span>
<span data-ttu-id="9e66e-143">DeploymentMode 集合. Hashtable. 雜湊表。</span><span class="sxs-lookup"><span data-stu-id="9e66e-143">Microsoft.Azure.Management.ResourceManager.Models.DeploymentMode System.Collections.Hashtable</span></span>

## <span data-ttu-id="9e66e-144">輸出</span><span class="sxs-lookup"><span data-stu-id="9e66e-144">OUTPUTS</span></span>

### <span data-ttu-id="9e66e-145">PSResourceManagerError 中的 SdkModels （）</span><span class="sxs-lookup"><span data-stu-id="9e66e-145">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceManagerError</span></span>

## <span data-ttu-id="9e66e-146">筆記</span><span class="sxs-lookup"><span data-stu-id="9e66e-146">NOTES</span></span>

## <span data-ttu-id="9e66e-147">相關連結</span><span class="sxs-lookup"><span data-stu-id="9e66e-147">RELATED LINKS</span></span>
