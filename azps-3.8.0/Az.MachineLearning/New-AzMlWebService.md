---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MachineLearning.dll-Help.xml
Module Name: Az.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/az.machinelearning/new-azmlwebservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/New-AzMlWebService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/New-AzMlWebService.md
ms.openlocfilehash: 5988aed4ca0560daedc1470198e0b02975f18196
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93965678"
---
# <span data-ttu-id="2a4e6-101">New-AzMlWebService</span><span class="sxs-lookup"><span data-stu-id="2a4e6-101">New-AzMlWebService</span></span>

## <span data-ttu-id="2a4e6-102">摘要</span><span class="sxs-lookup"><span data-stu-id="2a4e6-102">SYNOPSIS</span></span>
<span data-ttu-id="2a4e6-103">建立新的 web 服務。</span><span class="sxs-lookup"><span data-stu-id="2a4e6-103">Creates a new web service.</span></span>

## <span data-ttu-id="2a4e6-104">句法</span><span class="sxs-lookup"><span data-stu-id="2a4e6-104">SYNTAX</span></span>

### <span data-ttu-id="2a4e6-105">CreateFromFile</span><span class="sxs-lookup"><span data-stu-id="2a4e6-105">CreateFromFile</span></span>
```
New-AzMlWebService -ResourceGroupName <String> -Location <String> -Name <String> -DefinitionFile <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2a4e6-106">CreateFromInstance</span><span class="sxs-lookup"><span data-stu-id="2a4e6-106">CreateFromInstance</span></span>
```
New-AzMlWebService -ResourceGroupName <String> -Location <String> -Name <String>
 -NewWebServiceDefinition <WebService> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="2a4e6-107">說明</span><span class="sxs-lookup"><span data-stu-id="2a4e6-107">DESCRIPTION</span></span>
<span data-ttu-id="2a4e6-108">在現有的資源群組中建立 Azure 機器學習 web 服務。</span><span class="sxs-lookup"><span data-stu-id="2a4e6-108">Creates an Azure Machine Learning web service in an existing resource group.</span></span>
<span data-ttu-id="2a4e6-109">如果資源群組中存在具有相同名稱的 web 服務，該呼叫就會做為更新作業，而現有的 web 服務會覆寫。</span><span class="sxs-lookup"><span data-stu-id="2a4e6-109">If a web service with the same name exists in the resource group, the call acts as an update operation and the existing web service is overwritten.</span></span>

## <span data-ttu-id="2a4e6-110">示例</span><span class="sxs-lookup"><span data-stu-id="2a4e6-110">EXAMPLES</span></span>

### <span data-ttu-id="2a4e6-111">範例1：從以 Json 檔案為基礎的定義建立新服務</span><span class="sxs-lookup"><span data-stu-id="2a4e6-111">Example 1: Create a new service from a Json file based definition</span></span>
```
New-AzMlWebService -ResourceGroupName "myresourcegroup" -Name "mywebservicename" -Location "South Central US" -DefinitionFile "C:\mlservice.json"
```

<span data-ttu-id="2a4e6-112">根據參照的 json 檔案中提供的定義，在 "myresourcegroup" 群組和華南美國地區建立名為 "mywebservicename" 的新 Azure 電腦學習 web 服務。</span><span class="sxs-lookup"><span data-stu-id="2a4e6-112">Creates a new Azure Machine Learning web service named "mywebservicename" in the "myresourcegroup" group and South Central US region, based on the definition present in the referenced json file.</span></span>

### <span data-ttu-id="2a4e6-113">範例2：從物件實例建立新的服務</span><span class="sxs-lookup"><span data-stu-id="2a4e6-113">Example 2: Create a new service from an object instance</span></span>
```
New-AzMlWebService -ResourceGroupName "myresourcegroup" -Name "mywebservicename" -Location "South Central US" -NewWebServiceDefinition $serviceDefinitionObject
```

<span data-ttu-id="2a4e6-114">您可以透過使用 Import-AzMlWebService Cmdlet，在發佈為資源前取得要自訂的 web 服務物件實例。</span><span class="sxs-lookup"><span data-stu-id="2a4e6-114">You can obtain a web service object instance to customize before publishing as a resource by using the Import-AzMlWebService cmdlet.</span></span>

## <span data-ttu-id="2a4e6-115">參數</span><span class="sxs-lookup"><span data-stu-id="2a4e6-115">PARAMETERS</span></span>

### <span data-ttu-id="2a4e6-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2a4e6-116">-DefaultProfile</span></span>
<span data-ttu-id="2a4e6-117">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="2a4e6-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2a4e6-118">-DefinitionFile</span><span class="sxs-lookup"><span data-stu-id="2a4e6-118">-DefinitionFile</span></span>
<span data-ttu-id="2a4e6-119">指定包含 web 服務 JSON 格式定義之檔案的路徑。</span><span class="sxs-lookup"><span data-stu-id="2a4e6-119">Specifies the path to the file containing the JSON format definition of the web service.</span></span>
<span data-ttu-id="2a4e6-120">您可以在 [swagger 規範] 底下的 [swagger] 中找到最新的 web 服務定義規格 https://github.com/Azure/azure-rest-api-specs/tree/master/arm-machinelearning 。</span><span class="sxs-lookup"><span data-stu-id="2a4e6-120">You can find the latest specification for the web service definition in the swagger spec under https://github.com/Azure/azure-rest-api-specs/tree/master/arm-machinelearning.</span></span>

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

### <span data-ttu-id="2a4e6-121">-Force</span><span class="sxs-lookup"><span data-stu-id="2a4e6-121">-Force</span></span>
<span data-ttu-id="2a4e6-122">不要要求確認。</span><span class="sxs-lookup"><span data-stu-id="2a4e6-122">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="2a4e6-123">-位置</span><span class="sxs-lookup"><span data-stu-id="2a4e6-123">-Location</span></span>
<span data-ttu-id="2a4e6-124">Web 服務的區域。</span><span class="sxs-lookup"><span data-stu-id="2a4e6-124">The region of the web service.</span></span>
<span data-ttu-id="2a4e6-125">輸入 Azure 資料中心區域，例如「美國西部」或「東南部亞洲」。</span><span class="sxs-lookup"><span data-stu-id="2a4e6-125">Enter an Azure data center region, such as "West US" or "Southeast Asia".</span></span>
<span data-ttu-id="2a4e6-126">您可以將 web 服務放在支援該類型之資源的任何區域中。</span><span class="sxs-lookup"><span data-stu-id="2a4e6-126">You can place a web service in any region that supports resources of that type.</span></span>
<span data-ttu-id="2a4e6-127">Web 服務不必須位於與您的 Azure 訂閱或與其資源群組相同的區域中。</span><span class="sxs-lookup"><span data-stu-id="2a4e6-127">The web service does not have to be in the same region your Azure subscription or the same region as its resource group.</span></span>
<span data-ttu-id="2a4e6-128">資源群組可以包含來自不同地區的 web 服務。</span><span class="sxs-lookup"><span data-stu-id="2a4e6-128">Resource groups can contain web services from different regions.</span></span>
<span data-ttu-id="2a4e6-129">若要判斷哪些區域支援每個資源類型，請將 Get-AzResourceProvider 與 ProviderNamespace 參數 Cmdlet 搭配使用。</span><span class="sxs-lookup"><span data-stu-id="2a4e6-129">To determine which regions support each resource type, use the Get-AzResourceProvider with the ProviderNamespace parameter cmdlet.</span></span>

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

### <span data-ttu-id="2a4e6-130">-名稱</span><span class="sxs-lookup"><span data-stu-id="2a4e6-130">-Name</span></span>
<span data-ttu-id="2a4e6-131">Web 服務的名稱。</span><span class="sxs-lookup"><span data-stu-id="2a4e6-131">The name for the web service.</span></span>
<span data-ttu-id="2a4e6-132">該名稱在 [資源] 群組中必須是唯一的。</span><span class="sxs-lookup"><span data-stu-id="2a4e6-132">The name must be unique in the resource group.</span></span>

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

### <span data-ttu-id="2a4e6-133">-NewWebServiceDefinition</span><span class="sxs-lookup"><span data-stu-id="2a4e6-133">-NewWebServiceDefinition</span></span>
<span data-ttu-id="2a4e6-134">新 web 服務的定義，包含組成服務的所有屬性。</span><span class="sxs-lookup"><span data-stu-id="2a4e6-134">The definition for the new web service, containing all the properties that make up the service.</span></span>
<span data-ttu-id="2a4e6-135">這個參數是必要的，且代表 MachineLearning WebServices 的實例。在 WebService 類別中，</span><span class="sxs-lookup"><span data-stu-id="2a4e6-135">This parameter is required and represents an instance of the Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService class.</span></span>
<span data-ttu-id="2a4e6-136">您可以在 [swagger 規範] 底下的 [swagger] 中找到最新的 web 服務定義規格 https://github.com/Azure/azure-rest-api-specs/blob/master/arm-machinelearning/2017-01-01/swagger/webservices.json 。</span><span class="sxs-lookup"><span data-stu-id="2a4e6-136">You can find the latest specification for the web service definition in the swagger spec under https://github.com/Azure/azure-rest-api-specs/blob/master/arm-machinelearning/2017-01-01/swagger/webservices.json.</span></span>

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

### <span data-ttu-id="2a4e6-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2a4e6-137">-ResourceGroupName</span></span>
<span data-ttu-id="2a4e6-138">要放置 web 服務的資源群組。</span><span class="sxs-lookup"><span data-stu-id="2a4e6-138">The resource group in which to place the web service.</span></span>
<span data-ttu-id="2a4e6-139">輸入 Azure 資料中心區域，例如「美國西部」或「東南部亞洲」。</span><span class="sxs-lookup"><span data-stu-id="2a4e6-139">Enter an Azure data center region, such as "West US" or "Southeast Asia".</span></span>
<span data-ttu-id="2a4e6-140">您可以將 web 服務放在支援該類型之資源的任何區域中。</span><span class="sxs-lookup"><span data-stu-id="2a4e6-140">You can place a web service in any region that supports resources of that type.</span></span>
<span data-ttu-id="2a4e6-141">Web 服務不必須位於與您的 Azure 訂閱或與其資源群組相同的區域中。</span><span class="sxs-lookup"><span data-stu-id="2a4e6-141">The web service does not have to be in the same region your Azure subscription or the same region as its resource group.</span></span>
<span data-ttu-id="2a4e6-142">資源群組可以包含來自不同地區的 web 服務。</span><span class="sxs-lookup"><span data-stu-id="2a4e6-142">Resource groups can contain web services from different regions.</span></span>
<span data-ttu-id="2a4e6-143">若要判斷哪些區域支援每個資源類型，請將 Get-AzResourceProvider 與 ProviderNamespace 參數 Cmdlet 搭配使用。</span><span class="sxs-lookup"><span data-stu-id="2a4e6-143">To determine which regions support each resource type, use the Get-AzResourceProvider with the ProviderNamespace parameter cmdlet.</span></span>

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

### <span data-ttu-id="2a4e6-144">-確認</span><span class="sxs-lookup"><span data-stu-id="2a4e6-144">-Confirm</span></span>
<span data-ttu-id="2a4e6-145">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="2a4e6-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2a4e6-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2a4e6-146">-WhatIf</span></span>
<span data-ttu-id="2a4e6-147">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="2a4e6-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2a4e6-148">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="2a4e6-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2a4e6-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2a4e6-149">CommonParameters</span></span>
<span data-ttu-id="2a4e6-150">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="2a4e6-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2a4e6-151">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="2a4e6-151">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2a4e6-152">輸入</span><span class="sxs-lookup"><span data-stu-id="2a4e6-152">INPUTS</span></span>

### <span data-ttu-id="2a4e6-153">[MachineLearning] WebServices 的 Web 元件</span><span class="sxs-lookup"><span data-stu-id="2a4e6-153">Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService</span></span>

## <span data-ttu-id="2a4e6-154">輸出</span><span class="sxs-lookup"><span data-stu-id="2a4e6-154">OUTPUTS</span></span>

### <span data-ttu-id="2a4e6-155">[MachineLearning] WebServices 的 Web 元件</span><span class="sxs-lookup"><span data-stu-id="2a4e6-155">Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService</span></span>

## <span data-ttu-id="2a4e6-156">筆記</span><span class="sxs-lookup"><span data-stu-id="2a4e6-156">NOTES</span></span>
<span data-ttu-id="2a4e6-157">關鍵字： azure，azurerm，arm，資源，管理，管理員，機器，機器學習，azureml</span><span class="sxs-lookup"><span data-stu-id="2a4e6-157">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="2a4e6-158">相關連結</span><span class="sxs-lookup"><span data-stu-id="2a4e6-158">RELATED LINKS</span></span>
