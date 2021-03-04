---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MachineLearning.dll-Help.xml
Module Name: Az.MachineLearning
online version: https://docs.microsoft.com/powershell/module/az.machinelearning/update-azmlwebservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Update-AzMlWebService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Update-AzMlWebService.md
ms.openlocfilehash: 510e33655fd2e76383fa89a972c477e65d67f070
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101908118"
---
# <span data-ttu-id="6797d-101">Update-AzMlWebService</span><span class="sxs-lookup"><span data-stu-id="6797d-101">Update-AzMlWebService</span></span>

## <span data-ttu-id="6797d-102">簡介</span><span class="sxs-lookup"><span data-stu-id="6797d-102">SYNOPSIS</span></span>
<span data-ttu-id="6797d-103">更新現有 Web 服務資源的屬性。</span><span class="sxs-lookup"><span data-stu-id="6797d-103">Updates properties of an existing web service resource.</span></span>

## <span data-ttu-id="6797d-104">語法</span><span class="sxs-lookup"><span data-stu-id="6797d-104">SYNTAX</span></span>

### <span data-ttu-id="6797d-105">UpdateFromParameters</span><span class="sxs-lookup"><span data-stu-id="6797d-105">UpdateFromParameters</span></span>
```
Update-AzMlWebService -ResourceGroupName <String> -Name <String> [-Title <String>] [-Description <String>]
 [-IsReadOnly] [-Keys <WebServiceKeys>] [-StorageAccountKey <String>] [-Diagnostics <DiagnosticsConfiguration>]
 [-RealtimeConfiguration <RealtimeConfiguration>] [-Assets <Hashtable>]
 [-Input <ServiceInputOutputSpecification>] [-Output <ServiceInputOutputSpecification>]
 [-Parameters <Hashtable>] [-Package <GraphPackage>] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6797d-106">UpdateFromObject</span><span class="sxs-lookup"><span data-stu-id="6797d-106">UpdateFromObject</span></span>
```
Update-AzMlWebService -ResourceGroupName <String> -Name <String> -ServiceUpdates <WebService> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6797d-107">描述</span><span class="sxs-lookup"><span data-stu-id="6797d-107">DESCRIPTION</span></span>
<span data-ttu-id="6797d-108">Update-AzMlWebService Cmdlet 可讓您更新 Web 服務的非靜態屬性。</span><span class="sxs-lookup"><span data-stu-id="6797d-108">The Update-AzMlWebService cmdlet allows you to update the non-static properties of a web service.</span></span>
<span data-ttu-id="6797d-109">Cmdlet 可做為修補程式作業。</span><span class="sxs-lookup"><span data-stu-id="6797d-109">The cmdlet works as a patch operation.</span></span>
<span data-ttu-id="6797d-110">只傳遞您想要修改的屬性。</span><span class="sxs-lookup"><span data-stu-id="6797d-110">Pass only the properties that you want modified.</span></span>

## <span data-ttu-id="6797d-111">例子</span><span class="sxs-lookup"><span data-stu-id="6797d-111">EXAMPLES</span></span>

### <span data-ttu-id="6797d-112">範例 1：選擇性更新引數</span><span class="sxs-lookup"><span data-stu-id="6797d-112">Example 1: Selective update arguments</span></span>
```
Update-AzMlWebService -ResourceGroupName "myresourcegroup" -Name "mywebservicename" -Description "new update to description" -Keys @{Primary='changed primary key'} -Diagnostics @{Level='All'}
```

<span data-ttu-id="6797d-113">在這裡，我們變更描述、主存取鍵，並啟用 Web 服務執行時間期間所有追蹤的診斷集合。</span><span class="sxs-lookup"><span data-stu-id="6797d-113">Here, we change the description, primary access key and enable the diagnostics collection for all traces during runtime for the web service.</span></span>

### <span data-ttu-id="6797d-114">範例 2：根據 Web 服務實例更新</span><span class="sxs-lookup"><span data-stu-id="6797d-114">Example 2: Update based on a web service instance</span></span>
```
$updates = @{ Properties = @{ Title="New Title"; RealtimeConfiguration = @{ MaxConcurrentCalls=25 }}}

Update-AzMlWebService -ResourceGroupName "myresourcegroup" -Name "mywebservicename" -ServiceUpdates $updates
```

<span data-ttu-id="6797d-115">範例會先建立只包含要更新之欄位的 Web 服務定義，然後呼叫 Update-AzMlWebService使用 ServiceUpdates 參數來將它們進行申請。</span><span class="sxs-lookup"><span data-stu-id="6797d-115">The example first creates a web service definition, that only contains the fields to be updated, and then calls the Update-AzMlWebService to apply them using the ServiceUpdates parameter.</span></span>

## <span data-ttu-id="6797d-116">參數</span><span class="sxs-lookup"><span data-stu-id="6797d-116">PARAMETERS</span></span>

### <span data-ttu-id="6797d-117">-資產</span><span class="sxs-lookup"><span data-stu-id="6797d-117">-Assets</span></span>
<span data-ttu-id="6797d-118">資產集合 (例如模組、資料集) 組成 Web 服務。</span><span class="sxs-lookup"><span data-stu-id="6797d-118">The set of assets (e.g. modules, datasets) that make up the web service.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: UpdateFromParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6797d-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6797d-119">-DefaultProfile</span></span>
<span data-ttu-id="6797d-120">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="6797d-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6797d-121">-描述</span><span class="sxs-lookup"><span data-stu-id="6797d-121">-Description</span></span>
<span data-ttu-id="6797d-122">Web 服務描述的新值。</span><span class="sxs-lookup"><span data-stu-id="6797d-122">The new value for the web service's description.</span></span>
<span data-ttu-id="6797d-123">這會在服務的 Swagger API 架構中顯示。</span><span class="sxs-lookup"><span data-stu-id="6797d-123">This is visible in the service's Swagger API schema.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateFromParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6797d-124">-診斷</span><span class="sxs-lookup"><span data-stu-id="6797d-124">-Diagnostics</span></span>
<span data-ttu-id="6797d-125">控制 Web 服務的診斷追蹤集合的設定。</span><span class="sxs-lookup"><span data-stu-id="6797d-125">The settings that control the diagnostics traces collection for the web service.</span></span>

```yaml
Type: Microsoft.Azure.Management.MachineLearning.WebServices.Models.DiagnosticsConfiguration
Parameter Sets: UpdateFromParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6797d-126">-強制</span><span class="sxs-lookup"><span data-stu-id="6797d-126">-Force</span></span>
<span data-ttu-id="6797d-127">請勿要求確認。</span><span class="sxs-lookup"><span data-stu-id="6797d-127">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="6797d-128">-輸入</span><span class="sxs-lookup"><span data-stu-id="6797d-128">-Input</span></span>
<span data-ttu-id="6797d-129">Web 服務輸入的定義 (Swagger 架構) 提供。</span><span class="sxs-lookup"><span data-stu-id="6797d-129">The definition for the web service's input(s), provided as a Swagger schema construct.</span></span>

```yaml
Type: Microsoft.Azure.Management.MachineLearning.WebServices.Models.ServiceInputOutputSpecification
Parameter Sets: UpdateFromParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6797d-130">-IsReadOnly</span><span class="sxs-lookup"><span data-stu-id="6797d-130">-IsReadOnly</span></span>
<span data-ttu-id="6797d-131">指定此 Web 服務為唯讀。</span><span class="sxs-lookup"><span data-stu-id="6797d-131">Specifies that this web service is readonly.</span></span>
<span data-ttu-id="6797d-132">設定完成後，Web 服務可以更新更久，包括變更此屬性的值，而且只能刪除。</span><span class="sxs-lookup"><span data-stu-id="6797d-132">Once set, the web service can longer be updated, including changing the value of this property, and can only be deleted.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: UpdateFromParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6797d-133">-按鍵</span><span class="sxs-lookup"><span data-stu-id="6797d-133">-Keys</span></span>
<span data-ttu-id="6797d-134">更新用來驗證服務執行時間 API 之呼叫的一個或兩個便捷鍵。</span><span class="sxs-lookup"><span data-stu-id="6797d-134">Updates one or both of the access keys used to authenticate calls to the service's runtime APIs.</span></span>

```yaml
Type: Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebServiceKeys
Parameter Sets: UpdateFromParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6797d-135">-名稱</span><span class="sxs-lookup"><span data-stu-id="6797d-135">-Name</span></span>
<span data-ttu-id="6797d-136">要更新的 Web 服務資源名稱。</span><span class="sxs-lookup"><span data-stu-id="6797d-136">The name of the web service resource to be updated.</span></span>

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

### <span data-ttu-id="6797d-137">-輸出</span><span class="sxs-lookup"><span data-stu-id="6797d-137">-Output</span></span>
<span data-ttu-id="6797d-138">Web 服務輸出的定義是 (架構) ，提供為 Swa之架構架構。</span><span class="sxs-lookup"><span data-stu-id="6797d-138">The definition for the web service's output(s), provided as a Swagger schema construct.</span></span>

```yaml
Type: Microsoft.Azure.Management.MachineLearning.WebServices.Models.ServiceInputOutputSpecification
Parameter Sets: UpdateFromParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6797d-139">-套件</span><span class="sxs-lookup"><span data-stu-id="6797d-139">-Package</span></span>
<span data-ttu-id="6797d-140">定義此 Web 服務的圖形套件定義。</span><span class="sxs-lookup"><span data-stu-id="6797d-140">The definition of the graph package that defines this web service.</span></span>

```yaml
Type: Microsoft.Azure.Management.MachineLearning.WebServices.Models.GraphPackage
Parameter Sets: UpdateFromParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6797d-141">-參數</span><span class="sxs-lookup"><span data-stu-id="6797d-141">-Parameters</span></span>
<span data-ttu-id="6797d-142">為 Web 服務定義的一組全域參數值，以全域參數名稱做為預設值 \> 集合。</span><span class="sxs-lookup"><span data-stu-id="6797d-142">The set of global parameters values defined for the web service, given as a global parameter name -\> default value collection.</span></span>
<span data-ttu-id="6797d-143">如果沒有指定預設值，則視為需要參數。</span><span class="sxs-lookup"><span data-stu-id="6797d-143">If no default value is specified, the parameter is considered to be required.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: UpdateFromParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6797d-144">-RealtimeConfiguration</span><span class="sxs-lookup"><span data-stu-id="6797d-144">-RealtimeConfiguration</span></span>
<span data-ttu-id="6797d-145">服務即時端點之組配置的更新。</span><span class="sxs-lookup"><span data-stu-id="6797d-145">Updates for the configuration of the service's realtime endpoint.</span></span>

```yaml
Type: Microsoft.Azure.Management.MachineLearning.WebServices.Models.RealtimeConfiguration
Parameter Sets: UpdateFromParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6797d-146">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6797d-146">-ResourceGroupName</span></span>
<span data-ttu-id="6797d-147">包含要更新之 Web 服務的資源群組。</span><span class="sxs-lookup"><span data-stu-id="6797d-147">The resource group that contains the web service to be updated.</span></span>

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

### <span data-ttu-id="6797d-148">-ServiceUpdates</span><span class="sxs-lookup"><span data-stu-id="6797d-148">-ServiceUpdates</span></span>
<span data-ttu-id="6797d-149">一組更新，以套用至以 Web 服務定義實例提供的 Web 服務。</span><span class="sxs-lookup"><span data-stu-id="6797d-149">A set of updates to apply to the web service provided as a web service definition instance.</span></span>
<span data-ttu-id="6797d-150">只有非靜態欄位會修改。</span><span class="sxs-lookup"><span data-stu-id="6797d-150">Only non-static fields are modified.</span></span>

```yaml
Type: Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService
Parameter Sets: UpdateFromObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6797d-151">-StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="6797d-151">-StorageAccountKey</span></span>
<span data-ttu-id="6797d-152">旋轉與 Web 服務相關聯的儲存空間帳戶的便捷鍵。</span><span class="sxs-lookup"><span data-stu-id="6797d-152">Rotates the access key for the storage account associated with the web service.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateFromParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6797d-153">-標題</span><span class="sxs-lookup"><span data-stu-id="6797d-153">-Title</span></span>
<span data-ttu-id="6797d-154">Web 服務標題的新值。</span><span class="sxs-lookup"><span data-stu-id="6797d-154">The new value for the web service's title.</span></span>
<span data-ttu-id="6797d-155">這會在服務的 Swagger API 架構中顯示。</span><span class="sxs-lookup"><span data-stu-id="6797d-155">This is visible in the service's Swagger API schema.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateFromParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6797d-156">-確認</span><span class="sxs-lookup"><span data-stu-id="6797d-156">-Confirm</span></span>
<span data-ttu-id="6797d-157">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="6797d-157">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6797d-158">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6797d-158">-WhatIf</span></span>
<span data-ttu-id="6797d-159">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="6797d-159">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6797d-160">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="6797d-160">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6797d-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6797d-161">CommonParameters</span></span>
<span data-ttu-id="6797d-162">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="6797d-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6797d-163">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="6797d-163">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6797d-164">輸入</span><span class="sxs-lookup"><span data-stu-id="6797d-164">INPUTS</span></span>

### <span data-ttu-id="6797d-165">Microsoft.Azure.management.MachineLearning.WebServices.models.WebService</span><span class="sxs-lookup"><span data-stu-id="6797d-165">Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService</span></span>

## <span data-ttu-id="6797d-166">輸出</span><span class="sxs-lookup"><span data-stu-id="6797d-166">OUTPUTS</span></span>

### <span data-ttu-id="6797d-167">Microsoft.Azure.management.MachineLearning.WebServices.models.WebService</span><span class="sxs-lookup"><span data-stu-id="6797d-167">Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService</span></span>

## <span data-ttu-id="6797d-168">筆記</span><span class="sxs-lookup"><span data-stu-id="6797d-168">NOTES</span></span>
<span data-ttu-id="6797d-169">關鍵字：azure、azurerm、arm、resource、management、manager、machine、機器學習、azureml</span><span class="sxs-lookup"><span data-stu-id="6797d-169">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="6797d-170">相關連結</span><span class="sxs-lookup"><span data-stu-id="6797d-170">RELATED LINKS</span></span>
