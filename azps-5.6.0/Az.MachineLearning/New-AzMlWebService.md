---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MachineLearning.dll-Help.xml
Module Name: Az.MachineLearning
online version: https://docs.microsoft.com/powershell/module/az.machinelearning/new-azmlwebservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/New-AzMlWebService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/New-AzMlWebService.md
ms.openlocfilehash: 1a48438d6cec1621361a00cefa2bfead28117b97
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101904062"
---
# <span data-ttu-id="0dbdf-101">New-AzMlWebService</span><span class="sxs-lookup"><span data-stu-id="0dbdf-101">New-AzMlWebService</span></span>

## <span data-ttu-id="0dbdf-102">簡介</span><span class="sxs-lookup"><span data-stu-id="0dbdf-102">SYNOPSIS</span></span>
<span data-ttu-id="0dbdf-103">建立新 Web 服務。</span><span class="sxs-lookup"><span data-stu-id="0dbdf-103">Creates a new web service.</span></span>

## <span data-ttu-id="0dbdf-104">語法</span><span class="sxs-lookup"><span data-stu-id="0dbdf-104">SYNTAX</span></span>

### <span data-ttu-id="0dbdf-105">CreateFromFile</span><span class="sxs-lookup"><span data-stu-id="0dbdf-105">CreateFromFile</span></span>
```
New-AzMlWebService -ResourceGroupName <String> -Location <String> -Name <String> -DefinitionFile <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0dbdf-106">CreateFromInstance</span><span class="sxs-lookup"><span data-stu-id="0dbdf-106">CreateFromInstance</span></span>
```
New-AzMlWebService -ResourceGroupName <String> -Location <String> -Name <String>
 -NewWebServiceDefinition <WebService> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="0dbdf-107">描述</span><span class="sxs-lookup"><span data-stu-id="0dbdf-107">DESCRIPTION</span></span>
<span data-ttu-id="0dbdf-108">在現有的資源群組中建立 Azure 機器學習 Web 服務。</span><span class="sxs-lookup"><span data-stu-id="0dbdf-108">Creates an Azure Machine Learning web service in an existing resource group.</span></span>
<span data-ttu-id="0dbdf-109">如果相同名稱的 Web 服務存在於資源群組中，則呼叫會做為更新作業，且會覆蓋現有的 Web 服務。</span><span class="sxs-lookup"><span data-stu-id="0dbdf-109">If a web service with the same name exists in the resource group, the call acts as an update operation and the existing web service is overwritten.</span></span>

## <span data-ttu-id="0dbdf-110">例子</span><span class="sxs-lookup"><span data-stu-id="0dbdf-110">EXAMPLES</span></span>

### <span data-ttu-id="0dbdf-111">範例 1：從 Json 檔案定義建立新服務</span><span class="sxs-lookup"><span data-stu-id="0dbdf-111">Example 1: Create a new service from a Json file based definition</span></span>
```
New-AzMlWebService -ResourceGroupName "myresourcegroup" -Name "mywebservicename" -Location "South Central US" -DefinitionFile "C:\mlservice.json"
```

<span data-ttu-id="0dbdf-112">根據參照 json 檔案中的定義，在 "myresourcegroup" 群組和美國中南部地區建立名為 "mywebservicename" 的新 Azure 機器學習 Web 服務。</span><span class="sxs-lookup"><span data-stu-id="0dbdf-112">Creates a new Azure Machine Learning web service named "mywebservicename" in the "myresourcegroup" group and South Central US region, based on the definition present in the referenced json file.</span></span>

### <span data-ttu-id="0dbdf-113">範例 2：從物件實例建立新服務</span><span class="sxs-lookup"><span data-stu-id="0dbdf-113">Example 2: Create a new service from an object instance</span></span>
```
New-AzMlWebService -ResourceGroupName "myresourcegroup" -Name "mywebservicename" -Location "South Central US" -NewWebServiceDefinition $serviceDefinitionObject
```

<span data-ttu-id="0dbdf-114">您可以使用 Cmdlet 取得 Web 服務物件實例以自訂，然後再發佈為Import-AzMlWebService資源。</span><span class="sxs-lookup"><span data-stu-id="0dbdf-114">You can obtain a web service object instance to customize before publishing as a resource by using the Import-AzMlWebService cmdlet.</span></span>

## <span data-ttu-id="0dbdf-115">參數</span><span class="sxs-lookup"><span data-stu-id="0dbdf-115">PARAMETERS</span></span>

### <span data-ttu-id="0dbdf-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0dbdf-116">-DefaultProfile</span></span>
<span data-ttu-id="0dbdf-117">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="0dbdf-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0dbdf-118">-DefinitionFile</span><span class="sxs-lookup"><span data-stu-id="0dbdf-118">-DefinitionFile</span></span>
<span data-ttu-id="0dbdf-119">指定包含 Web 服務 JSON 格式定義的檔案路徑。</span><span class="sxs-lookup"><span data-stu-id="0dbdf-119">Specifies the path to the file containing the JSON format definition of the web service.</span></span>
<span data-ttu-id="0dbdf-120">您可以在 swagger 規格下找到 Web 服務定義的最新規格 https://github.com/Azure/azure-rest-api-specs/tree/master/arm-machinelearning 。</span><span class="sxs-lookup"><span data-stu-id="0dbdf-120">You can find the latest specification for the web service definition in the swagger spec under https://github.com/Azure/azure-rest-api-specs/tree/master/arm-machinelearning.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateFromFile
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0dbdf-121">-強制</span><span class="sxs-lookup"><span data-stu-id="0dbdf-121">-Force</span></span>
<span data-ttu-id="0dbdf-122">請勿要求確認。</span><span class="sxs-lookup"><span data-stu-id="0dbdf-122">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="0dbdf-123">-位置</span><span class="sxs-lookup"><span data-stu-id="0dbdf-123">-Location</span></span>
<span data-ttu-id="0dbdf-124">Web 服務的區域。</span><span class="sxs-lookup"><span data-stu-id="0dbdf-124">The region of the web service.</span></span>
<span data-ttu-id="0dbdf-125">輸入 Azure 資料中心區域，例如「美國西部」或「東南亞」。</span><span class="sxs-lookup"><span data-stu-id="0dbdf-125">Enter an Azure data center region, such as "West US" or "Southeast Asia".</span></span>
<span data-ttu-id="0dbdf-126">您可以將 Web 服務放在任何支援該類型資源的區域。</span><span class="sxs-lookup"><span data-stu-id="0dbdf-126">You can place a web service in any region that supports resources of that type.</span></span>
<span data-ttu-id="0dbdf-127">Web 服務不一定在 Azure 訂閱的同一區域，或與資源群組相同的區域。</span><span class="sxs-lookup"><span data-stu-id="0dbdf-127">The web service does not have to be in the same region your Azure subscription or the same region as its resource group.</span></span>
<span data-ttu-id="0dbdf-128">資源群組可以包含不同區域的 Web 服務。</span><span class="sxs-lookup"><span data-stu-id="0dbdf-128">Resource groups can contain web services from different regions.</span></span>
<span data-ttu-id="0dbdf-129">若要判斷哪些區域支援每種資源類型，請使用 Get-AzResourceProvider ProviderNamespace 參數 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="0dbdf-129">To determine which regions support each resource type, use the Get-AzResourceProvider with the ProviderNamespace parameter cmdlet.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0dbdf-130">-名稱</span><span class="sxs-lookup"><span data-stu-id="0dbdf-130">-Name</span></span>
<span data-ttu-id="0dbdf-131">Web 服務的名稱。</span><span class="sxs-lookup"><span data-stu-id="0dbdf-131">The name for the web service.</span></span>
<span data-ttu-id="0dbdf-132">名稱在資源群組中必須是唯一的。</span><span class="sxs-lookup"><span data-stu-id="0dbdf-132">The name must be unique in the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0dbdf-133">-NewWebServiceDefinition</span><span class="sxs-lookup"><span data-stu-id="0dbdf-133">-NewWebServiceDefinition</span></span>
<span data-ttu-id="0dbdf-134">新 Web 服務的定義，其中包含服務的所有屬性。</span><span class="sxs-lookup"><span data-stu-id="0dbdf-134">The definition for the new web service, containing all the properties that make up the service.</span></span>
<span data-ttu-id="0dbdf-135">此參數為必填專案，且代表 Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService 類的實例。</span><span class="sxs-lookup"><span data-stu-id="0dbdf-135">This parameter is required and represents an instance of the Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService class.</span></span>
<span data-ttu-id="0dbdf-136">您可以在 swagger 規格下找到 Web 服務定義的最新規格 https://github.com/Azure/azure-rest-api-specs/blob/master/arm-machinelearning/2017-01-01/swagger/webservices.json 。</span><span class="sxs-lookup"><span data-stu-id="0dbdf-136">You can find the latest specification for the web service definition in the swagger spec under https://github.com/Azure/azure-rest-api-specs/blob/master/arm-machinelearning/2017-01-01/swagger/webservices.json.</span></span>

```yaml
Type: Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService
Parameter Sets: CreateFromInstance
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0dbdf-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0dbdf-137">-ResourceGroupName</span></span>
<span data-ttu-id="0dbdf-138">放置 Web 服務的資源群組。</span><span class="sxs-lookup"><span data-stu-id="0dbdf-138">The resource group in which to place the web service.</span></span>
<span data-ttu-id="0dbdf-139">輸入 Azure 資料中心區域，例如「美國西部」或「東南亞」。</span><span class="sxs-lookup"><span data-stu-id="0dbdf-139">Enter an Azure data center region, such as "West US" or "Southeast Asia".</span></span>
<span data-ttu-id="0dbdf-140">您可以將 Web 服務放在任何支援該類型資源的區域。</span><span class="sxs-lookup"><span data-stu-id="0dbdf-140">You can place a web service in any region that supports resources of that type.</span></span>
<span data-ttu-id="0dbdf-141">Web 服務不一定在 Azure 訂閱的同一區域，或與資源群組相同的區域。</span><span class="sxs-lookup"><span data-stu-id="0dbdf-141">The web service does not have to be in the same region your Azure subscription or the same region as its resource group.</span></span>
<span data-ttu-id="0dbdf-142">資源群組可以包含不同區域的 Web 服務。</span><span class="sxs-lookup"><span data-stu-id="0dbdf-142">Resource groups can contain web services from different regions.</span></span>
<span data-ttu-id="0dbdf-143">若要判斷哪些區域支援每種資源類型，請使用 Get-AzResourceProvider ProviderNamespace 參數 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="0dbdf-143">To determine which regions support each resource type, use the Get-AzResourceProvider with the ProviderNamespace parameter cmdlet.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0dbdf-144">-確認</span><span class="sxs-lookup"><span data-stu-id="0dbdf-144">-Confirm</span></span>
<span data-ttu-id="0dbdf-145">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="0dbdf-145">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0dbdf-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0dbdf-146">-WhatIf</span></span>
<span data-ttu-id="0dbdf-147">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="0dbdf-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0dbdf-148">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="0dbdf-148">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0dbdf-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0dbdf-149">CommonParameters</span></span>
<span data-ttu-id="0dbdf-150">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="0dbdf-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0dbdf-151">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="0dbdf-151">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0dbdf-152">輸入</span><span class="sxs-lookup"><span data-stu-id="0dbdf-152">INPUTS</span></span>

### <span data-ttu-id="0dbdf-153">Microsoft.Azure.management.MachineLearning.WebServices.models.WebService</span><span class="sxs-lookup"><span data-stu-id="0dbdf-153">Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService</span></span>

## <span data-ttu-id="0dbdf-154">輸出</span><span class="sxs-lookup"><span data-stu-id="0dbdf-154">OUTPUTS</span></span>

### <span data-ttu-id="0dbdf-155">Microsoft.Azure.management.MachineLearning.WebServices.models.WebService</span><span class="sxs-lookup"><span data-stu-id="0dbdf-155">Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService</span></span>

## <span data-ttu-id="0dbdf-156">筆記</span><span class="sxs-lookup"><span data-stu-id="0dbdf-156">NOTES</span></span>
<span data-ttu-id="0dbdf-157">關鍵字：azure、azurerm、arm、resource、management、manager、machine、機器學習、azureml</span><span class="sxs-lookup"><span data-stu-id="0dbdf-157">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="0dbdf-158">相關連結</span><span class="sxs-lookup"><span data-stu-id="0dbdf-158">RELATED LINKS</span></span>
