---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MachineLearning.dll-Help.xml
Module Name: Az.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/az.machinelearning/update-azmlwebservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Update-AzMlWebService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Update-AzMlWebService.md
ms.openlocfilehash: a4c8e2687fd525b32ef3a9da3684a3da9f3c5717
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93611892"
---
# <span data-ttu-id="b3d39-101">Update-AzMlWebService</span><span class="sxs-lookup"><span data-stu-id="b3d39-101">Update-AzMlWebService</span></span>

## <span data-ttu-id="b3d39-102">摘要</span><span class="sxs-lookup"><span data-stu-id="b3d39-102">SYNOPSIS</span></span>
<span data-ttu-id="b3d39-103">更新現有 web 服務資源的屬性。</span><span class="sxs-lookup"><span data-stu-id="b3d39-103">Updates properties of an existing web service resource.</span></span>

## <span data-ttu-id="b3d39-104">句法</span><span class="sxs-lookup"><span data-stu-id="b3d39-104">SYNTAX</span></span>

### <span data-ttu-id="b3d39-105">UpdateFromParameters</span><span class="sxs-lookup"><span data-stu-id="b3d39-105">UpdateFromParameters</span></span>
```
Update-AzMlWebService -ResourceGroupName <String> -Name <String> [-Title <String>] [-Description <String>]
 [-IsReadOnly] [-Keys <WebServiceKeys>] [-StorageAccountKey <String>] [-Diagnostics <DiagnosticsConfiguration>]
 [-RealtimeConfiguration <RealtimeConfiguration>] [-Assets <Hashtable>]
 [-Input <ServiceInputOutputSpecification>] [-Output <ServiceInputOutputSpecification>]
 [-Parameters <Hashtable>] [-Package <GraphPackage>] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b3d39-106">UpdateFromObject</span><span class="sxs-lookup"><span data-stu-id="b3d39-106">UpdateFromObject</span></span>
```
Update-AzMlWebService -ResourceGroupName <String> -Name <String> -ServiceUpdates <WebService> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b3d39-107">說明</span><span class="sxs-lookup"><span data-stu-id="b3d39-107">DESCRIPTION</span></span>
<span data-ttu-id="b3d39-108">Update-AzMlWebService Cmdlet 可讓您更新 web 服務的非靜態屬性。</span><span class="sxs-lookup"><span data-stu-id="b3d39-108">The Update-AzMlWebService cmdlet allows you to update the non-static properties of a web service.</span></span>
<span data-ttu-id="b3d39-109">這個 Cmdlet 可以做為修補程式操作。</span><span class="sxs-lookup"><span data-stu-id="b3d39-109">The cmdlet works as a patch operation.</span></span>
<span data-ttu-id="b3d39-110">只傳遞您想要修改的屬性。</span><span class="sxs-lookup"><span data-stu-id="b3d39-110">Pass only the properties that you want modified.</span></span>

## <span data-ttu-id="b3d39-111">示例</span><span class="sxs-lookup"><span data-stu-id="b3d39-111">EXAMPLES</span></span>

### <span data-ttu-id="b3d39-112">範例1：選擇性更新引數</span><span class="sxs-lookup"><span data-stu-id="b3d39-112">Example 1: Selective update arguments</span></span>
```
Update-AzMlWebService -ResourceGroupName "myresourcegroup" -Name "mywebservicename" -Description "new update to description" -Keys @{Primary='changed primary key'} -Diagnostics @{Level='All'}
```

<span data-ttu-id="b3d39-113">在這裡，我們會變更描述、主要便捷鍵，以及在執行時間期間為 web 服務的所有追蹤啟用 [診斷集合]。</span><span class="sxs-lookup"><span data-stu-id="b3d39-113">Here, we change the description, primary access key and enable the diagnostics collection for all traces during runtime for the web service.</span></span>

### <span data-ttu-id="b3d39-114">範例2：根據 web 服務實例進行更新</span><span class="sxs-lookup"><span data-stu-id="b3d39-114">Example 2: Update based on a web service instance</span></span>
```
$updates = @{ Properties = @{ Title="New Title"; RealtimeConfiguration = @{ MaxConcurrentCalls=25 }}}

Update-AzMlWebService -ResourceGroupName "myresourcegroup" -Name "mywebservicename" -ServiceUpdates $updates
```

<span data-ttu-id="b3d39-115">這個範例會先建立一份 web 服務定義，只包含要更新的欄位，然後使用 ServiceUpdates 參數呼叫 Update-AzMlWebService 來套用它們。</span><span class="sxs-lookup"><span data-stu-id="b3d39-115">The example first creates a web service definition, that only contains the fields to be updated, and then calls the Update-AzMlWebService to apply them using the ServiceUpdates parameter.</span></span>

## <span data-ttu-id="b3d39-116">參數</span><span class="sxs-lookup"><span data-stu-id="b3d39-116">PARAMETERS</span></span>

### <span data-ttu-id="b3d39-117">-資產</span><span class="sxs-lookup"><span data-stu-id="b3d39-117">-Assets</span></span>
<span data-ttu-id="b3d39-118">組成 web 服務的一組資產 (例如模組、資料集) 。</span><span class="sxs-lookup"><span data-stu-id="b3d39-118">The set of assets (e.g. modules, datasets) that make up the web service.</span></span>

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

### <span data-ttu-id="b3d39-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b3d39-119">-DefaultProfile</span></span>
<span data-ttu-id="b3d39-120">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="b3d39-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b3d39-121">-描述</span><span class="sxs-lookup"><span data-stu-id="b3d39-121">-Description</span></span>
<span data-ttu-id="b3d39-122">Web 服務描述的新值。</span><span class="sxs-lookup"><span data-stu-id="b3d39-122">The new value for the web service's description.</span></span>
<span data-ttu-id="b3d39-123">這會顯示在服務的 Swagger API 架構中。</span><span class="sxs-lookup"><span data-stu-id="b3d39-123">This is visible in the service's Swagger API schema.</span></span>

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

### <span data-ttu-id="b3d39-124">-診斷程式</span><span class="sxs-lookup"><span data-stu-id="b3d39-124">-Diagnostics</span></span>
<span data-ttu-id="b3d39-125">控制 web 服務之診斷跟蹤集合的設定。</span><span class="sxs-lookup"><span data-stu-id="b3d39-125">The settings that control the diagnostics traces collection for the web service.</span></span>

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

### <span data-ttu-id="b3d39-126">-Force</span><span class="sxs-lookup"><span data-stu-id="b3d39-126">-Force</span></span>
<span data-ttu-id="b3d39-127">不要要求確認。</span><span class="sxs-lookup"><span data-stu-id="b3d39-127">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="b3d39-128">-輸入</span><span class="sxs-lookup"><span data-stu-id="b3d39-128">-Input</span></span>
<span data-ttu-id="b3d39-129">Web 服務輸入 (s) 的定義，提供為 Swagger 架構構造。</span><span class="sxs-lookup"><span data-stu-id="b3d39-129">The definition for the web service's input(s), provided as a Swagger schema construct.</span></span>

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

### <span data-ttu-id="b3d39-130">-IsReadOnly</span><span class="sxs-lookup"><span data-stu-id="b3d39-130">-IsReadOnly</span></span>
<span data-ttu-id="b3d39-131">指定此 web 服務為唯讀。</span><span class="sxs-lookup"><span data-stu-id="b3d39-131">Specifies that this web service is readonly.</span></span>
<span data-ttu-id="b3d39-132">設定之後，web 服務就可以再更新，包括變更這個屬性的值，而且只能刪除。</span><span class="sxs-lookup"><span data-stu-id="b3d39-132">Once set, the web service can longer be updated, including changing the value of this property, and can only be deleted.</span></span>

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

### <span data-ttu-id="b3d39-133">-按鍵</span><span class="sxs-lookup"><span data-stu-id="b3d39-133">-Keys</span></span>
<span data-ttu-id="b3d39-134">更新用來驗證服務的執行時間 Api 呼叫的一或兩個便捷鍵。</span><span class="sxs-lookup"><span data-stu-id="b3d39-134">Updates one or both of the access keys used to authenticate calls to the service's runtime APIs.</span></span>

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

### <span data-ttu-id="b3d39-135">-名稱</span><span class="sxs-lookup"><span data-stu-id="b3d39-135">-Name</span></span>
<span data-ttu-id="b3d39-136">要更新的 web 服務資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="b3d39-136">The name of the web service resource to be updated.</span></span>

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

### <span data-ttu-id="b3d39-137">-輸出</span><span class="sxs-lookup"><span data-stu-id="b3d39-137">-Output</span></span>
<span data-ttu-id="b3d39-138">Web 服務輸出 (s) 的定義，提供為 Swagger 架構構造。</span><span class="sxs-lookup"><span data-stu-id="b3d39-138">The definition for the web service's output(s), provided as a Swagger schema construct.</span></span>

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

### <span data-ttu-id="b3d39-139">-套件</span><span class="sxs-lookup"><span data-stu-id="b3d39-139">-Package</span></span>
<span data-ttu-id="b3d39-140">定義此 web 服務之圖表套件的定義。</span><span class="sxs-lookup"><span data-stu-id="b3d39-140">The definition of the graph package that defines this web service.</span></span>

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

### <span data-ttu-id="b3d39-141">-參數</span><span class="sxs-lookup"><span data-stu-id="b3d39-141">-Parameters</span></span>
<span data-ttu-id="b3d39-142">為 web 服務定義的全域參數值集，指定為全域參數名稱- \> 預設值集合。</span><span class="sxs-lookup"><span data-stu-id="b3d39-142">The set of global parameters values defined for the web service, given as a global parameter name -\> default value collection.</span></span>
<span data-ttu-id="b3d39-143">如果沒有指定預設值，則認為該參數是必要的。</span><span class="sxs-lookup"><span data-stu-id="b3d39-143">If no default value is specified, the parameter is considered to be required.</span></span>

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

### <span data-ttu-id="b3d39-144">-RealtimeConfiguration</span><span class="sxs-lookup"><span data-stu-id="b3d39-144">-RealtimeConfiguration</span></span>
<span data-ttu-id="b3d39-145">更新服務的即時端點。</span><span class="sxs-lookup"><span data-stu-id="b3d39-145">Updates for the configuration of the service's realtime endpoint.</span></span>

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

### <span data-ttu-id="b3d39-146">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b3d39-146">-ResourceGroupName</span></span>
<span data-ttu-id="b3d39-147">包含要更新之 web 服務的資源群組。</span><span class="sxs-lookup"><span data-stu-id="b3d39-147">The resource group that contains the web service to be updated.</span></span>

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

### <span data-ttu-id="b3d39-148">-ServiceUpdates</span><span class="sxs-lookup"><span data-stu-id="b3d39-148">-ServiceUpdates</span></span>
<span data-ttu-id="b3d39-149">將一組更新套用至以 web 服務定義實例形式提供的 web 服務。</span><span class="sxs-lookup"><span data-stu-id="b3d39-149">A set of updates to apply to the web service provided as a web service definition instance.</span></span>
<span data-ttu-id="b3d39-150">只會修改非靜態欄位。</span><span class="sxs-lookup"><span data-stu-id="b3d39-150">Only non-static fields are modified.</span></span>

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

### <span data-ttu-id="b3d39-151">-StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="b3d39-151">-StorageAccountKey</span></span>
<span data-ttu-id="b3d39-152">旋轉與 web 服務相關聯之儲存空間帳戶的便捷鍵。</span><span class="sxs-lookup"><span data-stu-id="b3d39-152">Rotates the access key for the storage account associated with the web service.</span></span>

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

### <span data-ttu-id="b3d39-153">-標題</span><span class="sxs-lookup"><span data-stu-id="b3d39-153">-Title</span></span>
<span data-ttu-id="b3d39-154">Web 服務標題的新值。</span><span class="sxs-lookup"><span data-stu-id="b3d39-154">The new value for the web service's title.</span></span>
<span data-ttu-id="b3d39-155">這會顯示在服務的 Swagger API 架構中。</span><span class="sxs-lookup"><span data-stu-id="b3d39-155">This is visible in the service's Swagger API schema.</span></span>

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

### <span data-ttu-id="b3d39-156">-確認</span><span class="sxs-lookup"><span data-stu-id="b3d39-156">-Confirm</span></span>
<span data-ttu-id="b3d39-157">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="b3d39-157">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b3d39-158">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b3d39-158">-WhatIf</span></span>
<span data-ttu-id="b3d39-159">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="b3d39-159">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b3d39-160">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="b3d39-160">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b3d39-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b3d39-161">CommonParameters</span></span>
<span data-ttu-id="b3d39-162">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="b3d39-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b3d39-163">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="b3d39-163">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b3d39-164">輸入</span><span class="sxs-lookup"><span data-stu-id="b3d39-164">INPUTS</span></span>

### <span data-ttu-id="b3d39-165">[MachineLearning] WebServices 的 Web 元件</span><span class="sxs-lookup"><span data-stu-id="b3d39-165">Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService</span></span>

## <span data-ttu-id="b3d39-166">輸出</span><span class="sxs-lookup"><span data-stu-id="b3d39-166">OUTPUTS</span></span>

### <span data-ttu-id="b3d39-167">[MachineLearning] WebServices 的 Web 元件</span><span class="sxs-lookup"><span data-stu-id="b3d39-167">Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService</span></span>

## <span data-ttu-id="b3d39-168">筆記</span><span class="sxs-lookup"><span data-stu-id="b3d39-168">NOTES</span></span>
<span data-ttu-id="b3d39-169">關鍵字： azure，azurerm，arm，資源，管理，管理員，機器，機器學習，azureml</span><span class="sxs-lookup"><span data-stu-id="b3d39-169">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="b3d39-170">相關連結</span><span class="sxs-lookup"><span data-stu-id="b3d39-170">RELATED LINKS</span></span>
