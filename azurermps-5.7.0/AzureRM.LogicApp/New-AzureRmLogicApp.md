---
external help file: Microsoft.Azure.Commands.LogicApp.dll-Help.xml
Module Name: AzureRM.LogicApp
ms.assetid: 8679240C-EA47-41C5-B8C1-A3C99547F42B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.logicapp/new-azurermlogicapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/New-AzureRmLogicApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/New-AzureRmLogicApp.md
ms.openlocfilehash: 1d2c39fcb22dfcf554487318a3a8f0a0b114fe11
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93450580"
---
# <span data-ttu-id="cb686-101">New-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="cb686-101">New-AzureRmLogicApp</span></span>

## <span data-ttu-id="cb686-102">摘要</span><span class="sxs-lookup"><span data-stu-id="cb686-102">SYNOPSIS</span></span>
<span data-ttu-id="cb686-103">在資源群組中建立邏輯 app。</span><span class="sxs-lookup"><span data-stu-id="cb686-103">Creates a logic app in a resource group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cb686-104">句法</span><span class="sxs-lookup"><span data-stu-id="cb686-104">SYNTAX</span></span>

### <span data-ttu-id="cb686-105">LogicAppWithDefinitionParameterSet</span><span class="sxs-lookup"><span data-stu-id="cb686-105">LogicAppWithDefinitionParameterSet</span></span>
```
New-AzureRmLogicApp -ResourceGroupName <String> -Name <String> -Location <String> [-State <String>]
 [-Definition <Object>] [-IntegrationAccountId <String>] [-Parameters <Object>] [-ParameterFilePath <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cb686-106">LogicAppWithDefinitionFileParameterSet</span><span class="sxs-lookup"><span data-stu-id="cb686-106">LogicAppWithDefinitionFileParameterSet</span></span>
```
New-AzureRmLogicApp -ResourceGroupName <String> -Name <String> -Location <String> [-State <String>]
 [-DefinitionFilePath <String>] [-IntegrationAccountId <String>] [-Parameters <Object>]
 [-ParameterFilePath <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="cb686-107">說明</span><span class="sxs-lookup"><span data-stu-id="cb686-107">DESCRIPTION</span></span>
<span data-ttu-id="cb686-108">**新的-AzureRmLogicApp** Cmdlet 會使用邏輯應用程式功能來建立邏輯 app。</span><span class="sxs-lookup"><span data-stu-id="cb686-108">The **New-AzureRmLogicApp** cmdlet creates a logic app by using the Logic Apps feature.</span></span>
<span data-ttu-id="cb686-109">邏輯 app 是在邏輯應用程式定義中定義的動作或觸發程式的集合。</span><span class="sxs-lookup"><span data-stu-id="cb686-109">A logic app is a collection of actions or triggers defined in Logic App definition.</span></span>
<span data-ttu-id="cb686-110">這個 Cmdlet 會傳回 **工作流程** 物件。</span><span class="sxs-lookup"><span data-stu-id="cb686-110">This cmdlet returns a **Workflow** object.</span></span>

<span data-ttu-id="cb686-111">您可以透過指定名稱、位置、邏輯應用程式定義、資源群組和規劃來建立邏輯 app。</span><span class="sxs-lookup"><span data-stu-id="cb686-111">You can create a logic app by specifying a name, location, Logic App definition, resource group, and plan.</span></span>
<span data-ttu-id="cb686-112">邏輯應用程式定義和參數的格式設定為 JavaScript 物件符號 (JSON) 。</span><span class="sxs-lookup"><span data-stu-id="cb686-112">A Logic App definition and parameters are formatted in JavaScript Object Notation (JSON).</span></span>
<span data-ttu-id="cb686-113">您可以使用邏輯 app 做為定義與參數的範本。</span><span class="sxs-lookup"><span data-stu-id="cb686-113">You can use a logic app as a template for definition and parameters.</span></span>

<span data-ttu-id="cb686-114">此模組支援動態參數。</span><span class="sxs-lookup"><span data-stu-id="cb686-114">This module supports dynamic parameters.</span></span>
<span data-ttu-id="cb686-115">若要使用動態參數，請在命令中輸入。</span><span class="sxs-lookup"><span data-stu-id="cb686-115">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="cb686-116">若要探索動態參數的名稱，請在 Cmdlet 名稱後輸入連字號 ( ) ，然後重複按 Tab 鍵以迴圈顯示可用的參數。</span><span class="sxs-lookup"><span data-stu-id="cb686-116">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="cb686-117">如果您省略必要的範本參數，則 Cmdlet 會提示您輸入值。</span><span class="sxs-lookup"><span data-stu-id="cb686-117">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>
<span data-ttu-id="cb686-118">您在命令列中指定的範本參數檔值優先于 template 參數物件中的範本參數值。</span><span class="sxs-lookup"><span data-stu-id="cb686-118">Template parameter file values that you specify at the command line take precedence over template parameter values in a template parameter object.</span></span>

## <span data-ttu-id="cb686-119">示例</span><span class="sxs-lookup"><span data-stu-id="cb686-119">EXAMPLES</span></span>

### <span data-ttu-id="cb686-120">範例1：使用定義和參數檔路徑建立邏輯 app</span><span class="sxs-lookup"><span data-stu-id="cb686-120">Example 1: Create a logic app by using definition and parameter file paths</span></span>
```
PS C:\>New-AzureRmLogicApp -ResourceGroupName "ResourceGroup11" -Name "LogicApp03" -State "Enabled" -AppServicePlan "ServicePlan01" -DefinitionFilePath "d:\workflows\Definition03.json" -ParameterFilePath "d:\workflows\Parameters03.json"
Id                           : /subscriptions/57b7034d-72d4-433d-ace2-a7460aed6a99/resourceGroups/LogicAppCmdletTest/providers/Microsoft.Logic/workflows/LogicApp03
Name                         : LogicApp03
Type                         : Microsoft.Logic/workflows
Location                     : westus
ChangedTime                  : 1/13/2016 2:41:39 PM
CreatedTime                  : 1/13/2016 2:41:39 PM
AccessEndpoint               : https://westus.logic.azure.com:443/subscriptions/57b7034d-72d4-433d-ace2-a7460aed6a99/resourcegroups/ResourceGroup1/providers/Microsoft.Logic/workflows/LogicApp1
State                        : Enabled
DefinitionLinkUri            : 
DefinitionLinkContentVersion : 
Definition                   : {$schema, contentVersion, parameters, triggers...} 
ParametersLinkUri            : 
ParametersLinkContentVersion : 
Parameters                   : {[destinationUri, Microsoft.Azure.Management.Logic.Models.WorkflowParameter]} 
SkuName                      : Standard
PlanName                     : ServicePlan01
PlanType                     : Microsoft.Web/ServerFarms
PlanId                       : /subscriptions/57b7034d-72d4-433d-ace2-a7460aed6a99/resourceGroups/ResourceGroup11/providers/Microsoft.Web/serverfarms/ServicePlan1
Version                      : 08587489107859952120
```

<span data-ttu-id="cb686-121">這個命令會在指定的資源群組中建立一個邏輯 app。</span><span class="sxs-lookup"><span data-stu-id="cb686-121">This command creates a logic app in the specified resource group.</span></span>
<span data-ttu-id="cb686-122">邏輯 app 包括檔案路徑所指定的定義和參數。</span><span class="sxs-lookup"><span data-stu-id="cb686-122">The logic app includes the definition and parameters specified by file paths.</span></span>

### <span data-ttu-id="cb686-123">範例2：使用定義和參數物件建立邏輯 app</span><span class="sxs-lookup"><span data-stu-id="cb686-123">Example 2: Create a logic app by using definition and parameter objects</span></span>
```
PS C:\>New-AzureRmLogicApp -ResourceGroupName "ResourceGroup11" -Name "LogicApp05" -Location "westus" -State "Enabled" -AppServicePlan "ServicePlan01" -Definition [IO.File]::ReadAllText("d:\Workflows\Definition.json") -Parameters @{name1="value1", name2="value2"}
Id                           : /subscriptions/57b7034d-72d4-433d-ace2-a7460aed6a99/resourceGroups/LogicAppCmdletTest/providers/Microsoft.Logic/workflows/LogicApp05
Name                         : LogicApp05
Type                         : Microsoft.Logic/workflows
Location                     : westus
ChangedTime                  : 1/13/2016 2:41:39 PM
CreatedTime                  : 1/13/2016 2:41:39 PM
AccessEndpoint               : https://westus.logic.azure.com:443/subscriptions/57b7034d-72d4-433d-ace2-a7460aed6a99/resourcegroups/ResourceGroup11/providers/Microsoft.Logic/workflows/LogicApp05
State                        : Enabled
DefinitionLinkUri            : 
DefinitionLinkContentVersion : 
Definition                   : {$schema, contentVersion, parameters, triggers...} 
ParametersLinkUri            : 
ParametersLinkContentVersion : 
Parameters                   : {[destinationUri, Microsoft.Azure.Management.Logic.Models.WorkflowParameter]} 
SkuName                      : Standard
PlanName                     : ServicePlan1
PlanType                     : Microsoft.Web/ServerFarms
PlanId                       : /subscriptions/57b7034d-72d4-433d-ace2-a7460aed6a99/resourceGroups/ResourceGroup11/providers/Microsoft.Web/serverfarms/ServicePlan1
Version                      : 08587489107859952120
```

<span data-ttu-id="cb686-124">這個命令會在指定的資源群組資源群組中建立邏輯 app。</span><span class="sxs-lookup"><span data-stu-id="cb686-124">This command creates a logic app in the specified resource group resource group.</span></span>

### <span data-ttu-id="cb686-125">範例3：使用管線來指定資源群組以建立邏輯 app</span><span class="sxs-lookup"><span data-stu-id="cb686-125">Example 3: Create a logic app by using the pipeline to specify the resource group</span></span>
```
PS C:\>Get-AzureRmResourceGroup -ResourceGroupName "ResourceGroup11" | New-AzureRmLogicApp -Name "LogicApp11" -State "Enabled" -AppServicePlan "ServicePlan01" -DefinitionFilePath "d:\Workflow\Definition.json" -ParameterFilePath "d:\Workflow\Parameters.json"
Id                           : /subscriptions/57b7034d-72d4-433d-ace2-a7460aed6a99/resourceGroups/LogicAppCmdletTest/providers/Microsoft.Logic/workflows/LogicApp11
Name                         : LogicApp11
Type                         : Microsoft.Logic/workflows
Location                     : westus
ChangedTime                  : 1/13/2016 2:41:39 PM
CreatedTime                  : 1/13/2016 2:41:39 PM
AccessEndpoint               : https://westus.logic.azure.com:443/subscriptions/57b7034d-72d4-433d-ace2-a7460aed6a99/resourcegroups/ResourceGroup11/providers/Microsoft.Logic/workflows/LogicApp11
State                        : Enabled
DefinitionLinkUri            : 
DefinitionLinkContentVersion : 
Definition                   : {$schema, contentVersion, parameters, triggers...} 
ParametersLinkUri            : 
ParametersLinkContentVersion : 
Parameters                   : {[destinationUri, Microsoft.Azure.Management.Logic.Models.WorkflowParameter]} 
SkuName                      : Standard
PlanName                     : ServicePlan01
PlanType                     : Microsoft.Web/ServerFarms
PlanId                       : /subscriptions/57b7034d-72d4-433d-ace2-a7460aed6a99/resourceGroups/ResourceGroup11/providers/Microsoft.Web/serverfarms/ServicePlan01
Version                      : 08587489107859952120
```

<span data-ttu-id="cb686-126">這個命令會使用 Get-AzureRmResourceGroup Cmdlet 來取得名為 ResourceGroup11 的資源群組。</span><span class="sxs-lookup"><span data-stu-id="cb686-126">This command gets the resource group named ResourceGroup11 by using the Get-AzureRmResourceGroup cmdlet.</span></span>
<span data-ttu-id="cb686-127">命令會使用管線運算子，將該資源群組傳遞至目前的 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="cb686-127">The command passes that resource group to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="cb686-128">目前的 Cmdlet 會在該資源群組中建立一個邏輯 app。</span><span class="sxs-lookup"><span data-stu-id="cb686-128">The current cmdlet creates a logic app in that resource group.</span></span>
<span data-ttu-id="cb686-129">邏輯 app 包括檔案路徑所指定的定義和參數。</span><span class="sxs-lookup"><span data-stu-id="cb686-129">The logic app includes the definition and parameters specified by file paths.</span></span>

### <span data-ttu-id="cb686-130">範例4：根據現有的邏輯 app 建立邏輯 app</span><span class="sxs-lookup"><span data-stu-id="cb686-130">Example 4: Create a logic app based on an existing logic app</span></span>
```
PS C:\>$Workflow = Get-AzureRmLogicApp -ResourceGroupName "ResourceGroup11" -Name "LogicApp03"
PS C:\> New-AzureRmLogicApp -ResourceGroupName "ResourceGroup11" -Name "LogicApp13" -State "Enabled" -AppServicePlan "ServicePlan01" -Definition $Workflow.Definition -Parameters $Workflow.Parameters
Id                           : /subscriptions/57b7034d-72d4-433d-ace2-a7460aed6a99/resourceGroups/LogicAppCmdletTest/providers/Microsoft.Logic/workflows/LogicApp13
Name                         : LogicApp13
Type                         : Microsoft.Logic/workflows
Location                     : westus
ChangedTime                  : 1/13/2016 2:41:39 PM
CreatedTime                  : 1/13/2016 2:41:39 PM
AccessEndpoint               : https://westus.logic.azure.com:443/subscriptions/57b7034d-72d4-433d-ace2-a7460aed6a99/resourcegroups/ResourceGroup11/providers/Microsoft.Logic/workflows/LogicApp13
State                        : Enabled
DefinitionLinkUri            : 
DefinitionLinkContentVersion : 
Definition                   : {$schema, contentVersion, parameters, triggers...} 
ParametersLinkUri            : 
ParametersLinkContentVersion : 
Parameters                   : {[destinationUri, Microsoft.Azure.Management.Logic.Models.WorkflowParameter]} 
SkuName                      : Standard
PlanName                     : ServicePlan01
PlanType                     : Microsoft.Web/ServerFarms
PlanId                       : /subscriptions/57b7034d-72d4-433d-ace2-a7460aed6a99/resourceGroups/ResourceGroup11/providers/Microsoft.Web/serverfarms/ServicePlan01
Version                      : 08587489107859952120
```

<span data-ttu-id="cb686-131">第一個命令會使用 Get-AzureRmLogicApp Cmdlet 來取得名為 LogicApp03 的邏輯 app。</span><span class="sxs-lookup"><span data-stu-id="cb686-131">The first command gets the logic app named LogicApp03 by using the Get-AzureRmLogicApp cmdlet.</span></span>
<span data-ttu-id="cb686-132">該命令會將邏輯 app 儲存在 $Workflow 變數中。</span><span class="sxs-lookup"><span data-stu-id="cb686-132">The command stores the logic app in the $Workflow variable.</span></span>

<span data-ttu-id="cb686-133">第二個命令會建立新的邏輯 app，此應用程式會使用儲存在 $Workflow 中之邏輯 app 的定義和參數。</span><span class="sxs-lookup"><span data-stu-id="cb686-133">The second command creates a new logic app that uses the definition and parameters of the logic app stored in $Workflow.</span></span>

## <span data-ttu-id="cb686-134">參數</span><span class="sxs-lookup"><span data-stu-id="cb686-134">PARAMETERS</span></span>

### <span data-ttu-id="cb686-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cb686-135">-DefaultProfile</span></span>
<span data-ttu-id="cb686-136">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="cb686-136">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="cb686-137">-定義</span><span class="sxs-lookup"><span data-stu-id="cb686-137">-Definition</span></span>
<span data-ttu-id="cb686-138">將您的邏輯 app 的定義指定為 JavaScript 物件 Notataion (JSON) 格式中的物件或字串。</span><span class="sxs-lookup"><span data-stu-id="cb686-138">Specifies the definition for your logic app as an object or a string in JavaScript Object Notataion (JSON) format.</span></span>

```yaml
Type: Object
Parameter Sets: LogicAppWithDefinitionParameterSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cb686-139">-DefinitionFilePath</span><span class="sxs-lookup"><span data-stu-id="cb686-139">-DefinitionFilePath</span></span>
<span data-ttu-id="cb686-140">將邏輯 app 的定義指定為 JSON 格式的定義檔路徑。</span><span class="sxs-lookup"><span data-stu-id="cb686-140">Specifies the definition of a logic app as the path of a definition file in JSON format.</span></span>

```yaml
Type: String
Parameter Sets: LogicAppWithDefinitionFileParameterSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cb686-141">-IntegrationAccountId</span><span class="sxs-lookup"><span data-stu-id="cb686-141">-IntegrationAccountId</span></span>
<span data-ttu-id="cb686-142">指定邏輯 app 的整合帳戶識別碼。</span><span class="sxs-lookup"><span data-stu-id="cb686-142">Specifies an integration account ID for the logic app.</span></span>

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

### <span data-ttu-id="cb686-143">-位置</span><span class="sxs-lookup"><span data-stu-id="cb686-143">-Location</span></span>
<span data-ttu-id="cb686-144">指定邏輯 app 的位置。</span><span class="sxs-lookup"><span data-stu-id="cb686-144">Specifies the location of the logic app.</span></span>
<span data-ttu-id="cb686-145">輸入 Azure 資料中心的位置，例如 [西部] 或 [東南部]。</span><span class="sxs-lookup"><span data-stu-id="cb686-145">Enter an Azure data center location, such as West US or Southeast Asia.</span></span>
<span data-ttu-id="cb686-146">您可以將邏輯 app 放置在任何位置。</span><span class="sxs-lookup"><span data-stu-id="cb686-146">You can place a logic app in any location.</span></span>

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

### <span data-ttu-id="cb686-147">-名稱</span><span class="sxs-lookup"><span data-stu-id="cb686-147">-Name</span></span>
<span data-ttu-id="cb686-148">指定邏輯應用程式的名稱。</span><span class="sxs-lookup"><span data-stu-id="cb686-148">Specifies the name for the logic app.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cb686-149">-ParameterFilePath</span><span class="sxs-lookup"><span data-stu-id="cb686-149">-ParameterFilePath</span></span>
<span data-ttu-id="cb686-150">指定 JSON 格式化參數檔的路徑。</span><span class="sxs-lookup"><span data-stu-id="cb686-150">Specifies the path of a JSON formatted parameter file.</span></span>

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

### <span data-ttu-id="cb686-151">-參數</span><span class="sxs-lookup"><span data-stu-id="cb686-151">-Parameters</span></span>
<span data-ttu-id="cb686-152">指定邏輯 App 的參數集合物件。</span><span class="sxs-lookup"><span data-stu-id="cb686-152">Specifies a parameters collection object for the Logic App.</span></span>
<span data-ttu-id="cb686-153">指定雜湊資料表、字典 \<string\> 或字典 \<string, WorkflowParameter\> 。</span><span class="sxs-lookup"><span data-stu-id="cb686-153">Specify a hash table, Dictionary\<string\>, or Dictionary\<string, WorkflowParameter\>.</span></span>

```yaml
Type: Object
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cb686-154">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cb686-154">-ResourceGroupName</span></span>
<span data-ttu-id="cb686-155">指定資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="cb686-155">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="cb686-156">-State</span><span class="sxs-lookup"><span data-stu-id="cb686-156">-State</span></span>
<span data-ttu-id="cb686-157">指定邏輯 app 的狀態。</span><span class="sxs-lookup"><span data-stu-id="cb686-157">Specifies the state of the logic app.</span></span>
<span data-ttu-id="cb686-158">此參數可接受的值為： [已啟用] 和 [已停用]。</span><span class="sxs-lookup"><span data-stu-id="cb686-158">The acceptable values for this parameter are: Enabled and Disabled.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cb686-159">-確認</span><span class="sxs-lookup"><span data-stu-id="cb686-159">-Confirm</span></span>
<span data-ttu-id="cb686-160">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="cb686-160">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cb686-161">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cb686-161">-WhatIf</span></span>
<span data-ttu-id="cb686-162">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="cb686-162">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cb686-163">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="cb686-163">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cb686-164">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cb686-164">CommonParameters</span></span>
<span data-ttu-id="cb686-165">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="cb686-165">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cb686-166">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="cb686-166">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cb686-167">輸入</span><span class="sxs-lookup"><span data-stu-id="cb686-167">INPUTS</span></span>

### <span data-ttu-id="cb686-168">所有</span><span class="sxs-lookup"><span data-stu-id="cb686-168">None</span></span>

## <span data-ttu-id="cb686-169">輸出</span><span class="sxs-lookup"><span data-stu-id="cb686-169">OUTPUTS</span></span>

### <span data-ttu-id="cb686-170">[Azure. 管理]。工作流程</span><span class="sxs-lookup"><span data-stu-id="cb686-170">Microsoft.Azure.Management.Logic.Models.Workflow</span></span>

## <span data-ttu-id="cb686-171">筆記</span><span class="sxs-lookup"><span data-stu-id="cb686-171">NOTES</span></span>

## <span data-ttu-id="cb686-172">相關連結</span><span class="sxs-lookup"><span data-stu-id="cb686-172">RELATED LINKS</span></span>

[<span data-ttu-id="cb686-173">AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="cb686-173">Get-AzureRmLogicApp</span></span>](./Get-AzureRmLogicApp.md)

[<span data-ttu-id="cb686-174">移除-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="cb686-174">Remove-AzureRmLogicApp</span></span>](./Remove-AzureRmLogicApp.md)

[<span data-ttu-id="cb686-175">Set-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="cb686-175">Set-AzureRmLogicApp</span></span>](./Set-AzureRmLogicApp.md)

[<span data-ttu-id="cb686-176">開始-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="cb686-176">Start-AzureRmLogicApp</span></span>](./Start-AzureRmLogicApp.md)

