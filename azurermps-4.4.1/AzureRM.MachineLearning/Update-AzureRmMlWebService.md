---
external help file: Microsoft.Azure.Commands.MachineLearning.dll-Help.xml
Module Name: AzureRM.MachineLearning
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Update-AzureRmMlWebService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Update-AzureRmMlWebService.md
ms.openlocfilehash: 75f94e5c93f81fa88dd33c3c0b94cb2b36ca291f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93451647"
---
# <span data-ttu-id="0da49-101">Update-AzureRmMlWebService</span><span class="sxs-lookup"><span data-stu-id="0da49-101">Update-AzureRmMlWebService</span></span>

## <span data-ttu-id="0da49-102">摘要</span><span class="sxs-lookup"><span data-stu-id="0da49-102">SYNOPSIS</span></span>
<span data-ttu-id="0da49-103">更新現有 web 服務資源的屬性。</span><span class="sxs-lookup"><span data-stu-id="0da49-103">Updates properties of an existing web service resource.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0da49-104">句法</span><span class="sxs-lookup"><span data-stu-id="0da49-104">SYNTAX</span></span>

### <span data-ttu-id="0da49-105">更新的特定屬性。</span><span class="sxs-lookup"><span data-stu-id="0da49-105">Update specific properties of the .</span></span>
```
Update-AzureRmMlWebService -ResourceGroupName <String> -Name <String> [-Title <String>] [-Description <String>]
 [-IsReadOnly] [-Keys <WebServiceKeys>] [-StorageAccountKey <String>] [-Diagnostics <DiagnosticsConfiguration>]
 [-RealtimeConfiguration <RealtimeConfiguration>] [-Assets <Hashtable>]
 [-Input <ServiceInputOutputSpecification>] [-Output <ServiceInputOutputSpecification>]
 [-Parameters <Hashtable>] [-Package <GraphPackage>] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0da49-106">從 WebService 實例定義建立新的 Azure ML webservice。</span><span class="sxs-lookup"><span data-stu-id="0da49-106">Create a new Azure ML webservice from a WebService instance definition.</span></span>
```
Update-AzureRmMlWebService -ResourceGroupName <String> -Name <String> -ServiceUpdates <WebService> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0da49-107">說明</span><span class="sxs-lookup"><span data-stu-id="0da49-107">DESCRIPTION</span></span>
<span data-ttu-id="0da49-108">Update-AzureRmMlWebService Cmdlet 可讓您更新 web 服務的非靜態屬性。</span><span class="sxs-lookup"><span data-stu-id="0da49-108">The Update-AzureRmMlWebService cmdlet allows you to update the non-static properties of a web service.</span></span>
<span data-ttu-id="0da49-109">這個 Cmdlet 可以做為修補程式操作。</span><span class="sxs-lookup"><span data-stu-id="0da49-109">The cmdlet works as a patch operation.</span></span>
<span data-ttu-id="0da49-110">只傳遞您想要修改的屬性。</span><span class="sxs-lookup"><span data-stu-id="0da49-110">Pass only the properties that you want modified.</span></span>

## <span data-ttu-id="0da49-111">示例</span><span class="sxs-lookup"><span data-stu-id="0da49-111">EXAMPLES</span></span>

### <span data-ttu-id="0da49-112">--------------------------範例1：選擇性更新引數--------------------------</span><span class="sxs-lookup"><span data-stu-id="0da49-112">--------------------------  Example 1: Selective update arguments  --------------------------</span></span>
<span data-ttu-id="0da49-113">@ {段落 = PS C： \\ \> }</span><span class="sxs-lookup"><span data-stu-id="0da49-113">@{paragraph=PS C:\\\>}</span></span>





```
Update-AzureRmMlWebService -ResourceGroupName "myresourcegroup" -Name "mywebservicename" -Description "new update to description" -Keys @{Primary='changed primary key'} -Diagnostics @{Level='All'}
```

<span data-ttu-id="0da49-114">在這裡，我們會變更描述、主要便捷鍵，以及在執行時間期間為 web 服務的所有追蹤啟用 [診斷集合]。</span><span class="sxs-lookup"><span data-stu-id="0da49-114">Here, we change the description, primary access key and enable the diagnostics collection for all traces during runtime for the web service.</span></span>

### <span data-ttu-id="0da49-115">--------------------------範例2：根據 web 服務實例進行更新--------------------------</span><span class="sxs-lookup"><span data-stu-id="0da49-115">--------------------------  Example 2: Update based on a web service instance  --------------------------</span></span>
<span data-ttu-id="0da49-116">@ {段落 = PS C： \\ \> }</span><span class="sxs-lookup"><span data-stu-id="0da49-116">@{paragraph=PS C:\\\>}</span></span>





```
$updates = @{ Properties = @{ Title="New Title"; RealtimeConfiguration = @{ MaxConcurrentCalls=25 }}}

Update-AzureRmMlWebService -ResourceGroupName "myresourcegroup" -Name "mywebservicename" -ServiceUpdates $updates
```

<span data-ttu-id="0da49-117">這個範例會先建立一份 web 服務定義，只包含要更新的欄位，然後使用 ServiceUpdates 參數呼叫 Update-AzureRmMlWebService 來套用它們。</span><span class="sxs-lookup"><span data-stu-id="0da49-117">The example first creates a web service definition, that only contains the fields to be updated, and then calls the Update-AzureRmMlWebService to apply them using the ServiceUpdates parameter.</span></span>

## <span data-ttu-id="0da49-118">參數</span><span class="sxs-lookup"><span data-stu-id="0da49-118">PARAMETERS</span></span>

### <span data-ttu-id="0da49-119">-資產</span><span class="sxs-lookup"><span data-stu-id="0da49-119">-Assets</span></span>
<span data-ttu-id="0da49-120">組成 web 服務的一組資產 (例如模組、資料集) 。</span><span class="sxs-lookup"><span data-stu-id="0da49-120">The set of assets (e.g. modules, datasets) that make up the web service.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: Update specific properties of the .
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0da49-121">-描述</span><span class="sxs-lookup"><span data-stu-id="0da49-121">-Description</span></span>
<span data-ttu-id="0da49-122">Web 服務描述的新值。</span><span class="sxs-lookup"><span data-stu-id="0da49-122">The new value for the web service's description.</span></span>
<span data-ttu-id="0da49-123">這會顯示在服務的 Swagger API 架構中。</span><span class="sxs-lookup"><span data-stu-id="0da49-123">This is visible in the service's Swagger API schema.</span></span>

```yaml
Type: System.String
Parameter Sets: Update specific properties of the .
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0da49-124">-診斷程式</span><span class="sxs-lookup"><span data-stu-id="0da49-124">-Diagnostics</span></span>
<span data-ttu-id="0da49-125">控制 web 服務之診斷跟蹤集合的設定。</span><span class="sxs-lookup"><span data-stu-id="0da49-125">The settings that control the diagnostics traces collection for the web service.</span></span>

```yaml
Type: Microsoft.Azure.Management.MachineLearning.WebServices.Models.DiagnosticsConfiguration
Parameter Sets: Update specific properties of the .
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0da49-126">-Force</span><span class="sxs-lookup"><span data-stu-id="0da49-126">-Force</span></span>
<span data-ttu-id="0da49-127">不要要求確認。</span><span class="sxs-lookup"><span data-stu-id="0da49-127">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="0da49-128">-輸入</span><span class="sxs-lookup"><span data-stu-id="0da49-128">-Input</span></span>
<span data-ttu-id="0da49-129">Web 服務輸入 (s) 的定義，提供為 Swagger 架構構造。</span><span class="sxs-lookup"><span data-stu-id="0da49-129">The definition for the web service's input(s), provided as a Swagger schema construct.</span></span>

```yaml
Type: Microsoft.Azure.Management.MachineLearning.WebServices.Models.ServiceInputOutputSpecification
Parameter Sets: Update specific properties of the .
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0da49-130">-IsReadOnly</span><span class="sxs-lookup"><span data-stu-id="0da49-130">-IsReadOnly</span></span>
<span data-ttu-id="0da49-131">指定此 web serviceis 唯讀。</span><span class="sxs-lookup"><span data-stu-id="0da49-131">Specifies that this web serviceis readonly.</span></span>
<span data-ttu-id="0da49-132">設定之後，web 服務就可以再更新，包括變更這個屬性的值，而且只能刪除。</span><span class="sxs-lookup"><span data-stu-id="0da49-132">Once set, the web service can longer be updated, including changing the value of this property, and can only be deleted.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Update specific properties of the .
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0da49-133">-按鍵</span><span class="sxs-lookup"><span data-stu-id="0da49-133">-Keys</span></span>
<span data-ttu-id="0da49-134">更新用來驗證服務的執行時間 Api 呼叫的一或兩個便捷鍵。</span><span class="sxs-lookup"><span data-stu-id="0da49-134">Updates one or both of the access keys used to authenticate calls to the service's runtime APIs.</span></span>

```yaml
Type: Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebServiceKeys
Parameter Sets: Update specific properties of the .
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0da49-135">-名稱</span><span class="sxs-lookup"><span data-stu-id="0da49-135">-Name</span></span>
<span data-ttu-id="0da49-136">要更新的 web 服務資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="0da49-136">The name of the web service resource to be updated.</span></span>

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

### <span data-ttu-id="0da49-137">-輸出</span><span class="sxs-lookup"><span data-stu-id="0da49-137">-Output</span></span>
<span data-ttu-id="0da49-138">Web 服務輸出 (s) 的定義，提供為 Swagger 架構構造。</span><span class="sxs-lookup"><span data-stu-id="0da49-138">The definition for the web service's output(s), provided as a Swagger schema construct.</span></span>

```yaml
Type: Microsoft.Azure.Management.MachineLearning.WebServices.Models.ServiceInputOutputSpecification
Parameter Sets: Update specific properties of the .
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0da49-139">-套件</span><span class="sxs-lookup"><span data-stu-id="0da49-139">-Package</span></span>
<span data-ttu-id="0da49-140">定義此 web 服務之圖表套件的定義。</span><span class="sxs-lookup"><span data-stu-id="0da49-140">The definition of the graph package that defines this web service.</span></span>

```yaml
Type: Microsoft.Azure.Management.MachineLearning.WebServices.Models.GraphPackage
Parameter Sets: Update specific properties of the .
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0da49-141">-參數</span><span class="sxs-lookup"><span data-stu-id="0da49-141">-Parameters</span></span>
<span data-ttu-id="0da49-142">為 web 服務定義的全域參數值集，指定為全域參數名稱- \> 預設值集合。</span><span class="sxs-lookup"><span data-stu-id="0da49-142">The set of global parameters values defined for the web service, given as a global parameter name -\> default value collection.</span></span>
<span data-ttu-id="0da49-143">如果沒有指定預設值，則認為該參數是必要的。</span><span class="sxs-lookup"><span data-stu-id="0da49-143">If no default value is specified, the parameter is considered to be required.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: Update specific properties of the .
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0da49-144">-RealtimeConfiguration</span><span class="sxs-lookup"><span data-stu-id="0da49-144">-RealtimeConfiguration</span></span>
<span data-ttu-id="0da49-145">更新服務的即時端點。</span><span class="sxs-lookup"><span data-stu-id="0da49-145">Updates for the configuration of the service's realtime endpoint.</span></span>

```yaml
Type: Microsoft.Azure.Management.MachineLearning.WebServices.Models.RealtimeConfiguration
Parameter Sets: Update specific properties of the .
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0da49-146">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0da49-146">-ResourceGroupName</span></span>
<span data-ttu-id="0da49-147">包含要更新之 web 服務的資源群組。</span><span class="sxs-lookup"><span data-stu-id="0da49-147">The resource group that contains the web service to be updated.</span></span>

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

### <span data-ttu-id="0da49-148">-ServiceUpdates</span><span class="sxs-lookup"><span data-stu-id="0da49-148">-ServiceUpdates</span></span>
<span data-ttu-id="0da49-149">將一組更新套用至以 web 服務定義實例形式提供的 web 服務。</span><span class="sxs-lookup"><span data-stu-id="0da49-149">A set of updates to apply to the web service provided as a web service definition instance.</span></span>
<span data-ttu-id="0da49-150">只會修改非靜態欄位。</span><span class="sxs-lookup"><span data-stu-id="0da49-150">Only non-static fields are modified.</span></span>

```yaml
Type: Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService
Parameter Sets: Create a new Azure ML webservice from a WebService instance definition.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0da49-151">-StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="0da49-151">-StorageAccountKey</span></span>
<span data-ttu-id="0da49-152">旋轉與 web 服務相關聯之儲存空間帳戶的便捷鍵。</span><span class="sxs-lookup"><span data-stu-id="0da49-152">Rotates the access key for the storage account associated with the web service.</span></span>

```yaml
Type: System.String
Parameter Sets: Update specific properties of the .
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0da49-153">-標題</span><span class="sxs-lookup"><span data-stu-id="0da49-153">-Title</span></span>
<span data-ttu-id="0da49-154">Web 服務標題的新值。</span><span class="sxs-lookup"><span data-stu-id="0da49-154">The new value for the web service's title.</span></span>
<span data-ttu-id="0da49-155">這會顯示在服務的 Swagger API 架構中。</span><span class="sxs-lookup"><span data-stu-id="0da49-155">This is visible in the service's Swagger API schema.</span></span>

```yaml
Type: System.String
Parameter Sets: Update specific properties of the .
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0da49-156">-確認</span><span class="sxs-lookup"><span data-stu-id="0da49-156">-Confirm</span></span>
<span data-ttu-id="0da49-157">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="0da49-157">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0da49-158">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0da49-158">-WhatIf</span></span>
<span data-ttu-id="0da49-159">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="0da49-159">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0da49-160">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="0da49-160">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0da49-161">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0da49-161">-DefaultProfile</span></span>
<span data-ttu-id="0da49-162">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="0da49-162">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0da49-163">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0da49-163">CommonParameters</span></span>
<span data-ttu-id="0da49-164">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="0da49-164">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0da49-165">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="0da49-165">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0da49-166">輸入</span><span class="sxs-lookup"><span data-stu-id="0da49-166">INPUTS</span></span>

### <span data-ttu-id="0da49-167">WebService</span><span class="sxs-lookup"><span data-stu-id="0da49-167">WebService</span></span>
<span data-ttu-id="0da49-168">"ServiceUpdates" 參數接受來自管線的 "WebService" 類型的值</span><span class="sxs-lookup"><span data-stu-id="0da49-168">Parameter 'ServiceUpdates' accepts value of type 'WebService' from the pipeline</span></span>

## <span data-ttu-id="0da49-169">輸出</span><span class="sxs-lookup"><span data-stu-id="0da49-169">OUTPUTS</span></span>

### <span data-ttu-id="0da49-170">[MachineLearning] WebServices 的 Web 元件</span><span class="sxs-lookup"><span data-stu-id="0da49-170">Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService</span></span>
<span data-ttu-id="0da49-171">Azure 機器學習 web 服務的摘要描述。</span><span class="sxs-lookup"><span data-stu-id="0da49-171">A summary description of the Azure Machine Learning web service.</span></span>
<span data-ttu-id="0da49-172">類似于在現有的 web 服務上呼叫 Get-AzureRmMlWebService Cmdlet 傳回的描述。</span><span class="sxs-lookup"><span data-stu-id="0da49-172">Similar to the description returned by calling the Get-AzureRmMlWebService cmdlet on an existing web service.</span></span>
<span data-ttu-id="0da49-173">此描述不包含敏感屬性，例如儲存帳戶的認證與服務的便捷鍵。</span><span class="sxs-lookup"><span data-stu-id="0da49-173">This description does not contain sensitive properties such as storage account's credentials and the service's access keys.</span></span>

## <span data-ttu-id="0da49-174">筆記</span><span class="sxs-lookup"><span data-stu-id="0da49-174">NOTES</span></span>
<span data-ttu-id="0da49-175">關鍵字： azure，azurerm，arm，資源，管理，管理員，機器，機器學習，azureml</span><span class="sxs-lookup"><span data-stu-id="0da49-175">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="0da49-176">相關連結</span><span class="sxs-lookup"><span data-stu-id="0da49-176">RELATED LINKS</span></span>

