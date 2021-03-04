---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: 8679240C-EA47-41C5-B8C1-A3C99547F42B
online version: https://docs.microsoft.com/powershell/module/az.logicapp/new-azlogicapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/New-AzLogicApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/New-AzLogicApp.md
ms.openlocfilehash: 98fb733f661d4d1c5a6c50ce472005763584a72c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101906161"
---
# <span data-ttu-id="8a03b-101">New-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="8a03b-101">New-AzLogicApp</span></span>

## <span data-ttu-id="8a03b-102">簡介</span><span class="sxs-lookup"><span data-stu-id="8a03b-102">SYNOPSIS</span></span>
<span data-ttu-id="8a03b-103">在資源群組中建立邏輯應用程式。</span><span class="sxs-lookup"><span data-stu-id="8a03b-103">Creates a logic app in a resource group.</span></span>

## <span data-ttu-id="8a03b-104">語法</span><span class="sxs-lookup"><span data-stu-id="8a03b-104">SYNTAX</span></span>

### <span data-ttu-id="8a03b-105">LogicAppWithDefinitionParameterSet</span><span class="sxs-lookup"><span data-stu-id="8a03b-105">LogicAppWithDefinitionParameterSet</span></span>
```
New-AzLogicApp -ResourceGroupName <String> -Name <String> -Location <String> [-State <String>]
 -Definition <Object> [-IntegrationAccountId <String>] [-Parameters <Object>] [-ParameterFilePath <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8a03b-106">LogicAppWithDefinitionFileParameterSet</span><span class="sxs-lookup"><span data-stu-id="8a03b-106">LogicAppWithDefinitionFileParameterSet</span></span>
```
New-AzLogicApp -ResourceGroupName <String> -Name <String> -Location <String> [-State <String>]
 -DefinitionFilePath <String> [-IntegrationAccountId <String>] [-Parameters <Object>]
 [-ParameterFilePath <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="8a03b-107">描述</span><span class="sxs-lookup"><span data-stu-id="8a03b-107">DESCRIPTION</span></span>
<span data-ttu-id="8a03b-108">**New-AzLogicApp** Cmdlet 會使用邏輯應用程式功能建立邏輯應用程式。</span><span class="sxs-lookup"><span data-stu-id="8a03b-108">The **New-AzLogicApp** cmdlet creates a logic app by using the Logic Apps feature.</span></span>
<span data-ttu-id="8a03b-109">邏輯應用程式是邏輯 App 定義中定義的動作或觸發程式集合。</span><span class="sxs-lookup"><span data-stu-id="8a03b-109">A logic app is a collection of actions or triggers defined in Logic App definition.</span></span>
<span data-ttu-id="8a03b-110">此 Cmdlet 會返回 **工作流程** 物件。</span><span class="sxs-lookup"><span data-stu-id="8a03b-110">This cmdlet returns a **Workflow** object.</span></span>
<span data-ttu-id="8a03b-111">您可以指定名稱、位置、邏輯應用程式定義、資源群組和計畫，以建立邏輯應用程式。</span><span class="sxs-lookup"><span data-stu-id="8a03b-111">You can create a logic app by specifying a name, location, Logic App definition, resource group, and plan.</span></span>
<span data-ttu-id="8a03b-112">邏輯應用程式定義和參數的格式設定為 JavaScript 物件標記法 (JSON) 。</span><span class="sxs-lookup"><span data-stu-id="8a03b-112">A Logic App definition and parameters are formatted in JavaScript Object Notation (JSON).</span></span>
<span data-ttu-id="8a03b-113">您可以使用邏輯應用程式做為定義和參數的範本。</span><span class="sxs-lookup"><span data-stu-id="8a03b-113">You can use a logic app as a template for definition and parameters.</span></span>
<span data-ttu-id="8a03b-114">此模組支援動態參數。</span><span class="sxs-lookup"><span data-stu-id="8a03b-114">This module supports dynamic parameters.</span></span>
<span data-ttu-id="8a03b-115">若要使用動態參數，請于命令中輸入。</span><span class="sxs-lookup"><span data-stu-id="8a03b-115">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="8a03b-116">若要探索動態參數的名稱，在 Cmdlet 名稱之後輸入連字號 (-) ，然後重複按 Tab 鍵以迴圈流覽可用的參數。</span><span class="sxs-lookup"><span data-stu-id="8a03b-116">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="8a03b-117">如果您省略必要的範本參數，Cmdlet 會提示您輸入值。</span><span class="sxs-lookup"><span data-stu-id="8a03b-117">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>
<span data-ttu-id="8a03b-118">在命令列中指定的範本參數檔案值優先于範本參數物件的範本參數值。</span><span class="sxs-lookup"><span data-stu-id="8a03b-118">Template parameter file values that you specify at the command line take precedence over template parameter values in a template parameter object.</span></span>

## <span data-ttu-id="8a03b-119">例子</span><span class="sxs-lookup"><span data-stu-id="8a03b-119">EXAMPLES</span></span>

### <span data-ttu-id="8a03b-120">範例 1：使用定義和參數檔案路徑建立邏輯應用程式</span><span class="sxs-lookup"><span data-stu-id="8a03b-120">Example 1: Create a logic app by using definition and parameter file paths</span></span>
```
PS C:\>New-AzLogicApp -ResourceGroupName "ResourceGroup11" -Name "LogicApp03" -State "Enabled" -AppServicePlan "ServicePlan01" -DefinitionFilePath "d:\workflows\Definition03.json" -ParameterFilePath "d:\workflows\Parameters03.json"
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

<span data-ttu-id="8a03b-121">此命令會于指定的資源群組中建立邏輯應用程式。</span><span class="sxs-lookup"><span data-stu-id="8a03b-121">This command creates a logic app in the specified resource group.</span></span>
<span data-ttu-id="8a03b-122">邏輯應用程式包含由檔案路徑指定的定義和參數。</span><span class="sxs-lookup"><span data-stu-id="8a03b-122">The logic app includes the definition and parameters specified by file paths.</span></span>

### <span data-ttu-id="8a03b-123">範例 2：使用定義和參數物件建立邏輯應用程式</span><span class="sxs-lookup"><span data-stu-id="8a03b-123">Example 2: Create a logic app by using definition and parameter objects</span></span>
```
PS C:\>New-AzLogicApp -ResourceGroupName "ResourceGroup11" -Name "LogicApp05" -Location "westus" -State "Enabled" -AppServicePlan "ServicePlan01" -Definition [IO.File]::ReadAllText("d:\Workflows\Definition.json") -Parameters @{name1="value1", name2="value2"}
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

<span data-ttu-id="8a03b-124">此命令會于指定的資源群組資源群組中建立邏輯應用程式。</span><span class="sxs-lookup"><span data-stu-id="8a03b-124">This command creates a logic app in the specified resource group resource group.</span></span>

### <span data-ttu-id="8a03b-125">範例 3：使用管線來指定資源群組來建立邏輯應用程式</span><span class="sxs-lookup"><span data-stu-id="8a03b-125">Example 3: Create a logic app by using the pipeline to specify the resource group</span></span>
```
PS C:\>Get-AzResourceGroup -ResourceGroupName "ResourceGroup11" | New-AzLogicApp -Name "LogicApp11" -State "Enabled" -AppServicePlan "ServicePlan01" -DefinitionFilePath "d:\Workflow\Definition.json" -ParameterFilePath "d:\Workflow\Parameters.json"
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

<span data-ttu-id="8a03b-126">此命令會使用 Cmdlet，獲得名為 ResourceGroup11 的資源Get-AzResourceGroup群組。</span><span class="sxs-lookup"><span data-stu-id="8a03b-126">This command gets the resource group named ResourceGroup11 by using the Get-AzResourceGroup cmdlet.</span></span>
<span data-ttu-id="8a03b-127">該命令會使用管線運算子，將資源群組傳遞至目前的 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="8a03b-127">The command passes that resource group to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="8a03b-128">目前的 Cmdlet 會建立資源群組中的邏輯應用程式。</span><span class="sxs-lookup"><span data-stu-id="8a03b-128">The current cmdlet creates a logic app in that resource group.</span></span>
<span data-ttu-id="8a03b-129">邏輯應用程式包含由檔案路徑指定的定義和參數。</span><span class="sxs-lookup"><span data-stu-id="8a03b-129">The logic app includes the definition and parameters specified by file paths.</span></span>

### <span data-ttu-id="8a03b-130">範例 4：根據現有的邏輯應用程式建立邏輯應用程式</span><span class="sxs-lookup"><span data-stu-id="8a03b-130">Example 4: Create a logic app based on an existing logic app</span></span>
```
PS C:\>$Workflow = Get-AzLogicApp -ResourceGroupName "ResourceGroup11" -Name "LogicApp03"
PS C:\> New-AzLogicApp -ResourceGroupName "ResourceGroup11" -Name "LogicApp13" -State "Enabled" -AppServicePlan "ServicePlan01" -Definition $Workflow.Definition -Parameters $Workflow.Parameters
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

<span data-ttu-id="8a03b-131">第一個命令會使用 Get-AzLogicApp Cmdlet，獲得名為 LogicApp03 的邏輯應用程式。</span><span class="sxs-lookup"><span data-stu-id="8a03b-131">The first command gets the logic app named LogicApp03 by using the Get-AzLogicApp cmdlet.</span></span>
<span data-ttu-id="8a03b-132">該命令將邏輯應用程式儲存在$Workflow變數中。</span><span class="sxs-lookup"><span data-stu-id="8a03b-132">The command stores the logic app in the $Workflow variable.</span></span>
<span data-ttu-id="8a03b-133">第二個命令會建立一個新的邏輯應用程式，使用儲存在 $Workflow 中之邏輯應用程式的定義和$Workflow。</span><span class="sxs-lookup"><span data-stu-id="8a03b-133">The second command creates a new logic app that uses the definition and parameters of the logic app stored in $Workflow.</span></span>

## <span data-ttu-id="8a03b-134">參數</span><span class="sxs-lookup"><span data-stu-id="8a03b-134">PARAMETERS</span></span>

### <span data-ttu-id="8a03b-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8a03b-135">-DefaultProfile</span></span>
<span data-ttu-id="8a03b-136">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="8a03b-136">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8a03b-137">-定義</span><span class="sxs-lookup"><span data-stu-id="8a03b-137">-Definition</span></span>
<span data-ttu-id="8a03b-138">以 JavaScript 物件標記法或 JSON 格式指定邏輯 (定義) 字串。</span><span class="sxs-lookup"><span data-stu-id="8a03b-138">Specifies the definition for your logic app as an object or a string in JavaScript Object Notation (JSON) format.</span></span>

```yaml
Type: System.Object
Parameter Sets: LogicAppWithDefinitionParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8a03b-139">-DefinitionFilePath</span><span class="sxs-lookup"><span data-stu-id="8a03b-139">-DefinitionFilePath</span></span>
<span data-ttu-id="8a03b-140">以 JSON 格式指定邏輯應用程式的定義做為定義檔案的路徑。</span><span class="sxs-lookup"><span data-stu-id="8a03b-140">Specifies the definition of a logic app as the path of a definition file in JSON format.</span></span>

```yaml
Type: System.String
Parameter Sets: LogicAppWithDefinitionFileParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8a03b-141">-IntegrationAccountId</span><span class="sxs-lookup"><span data-stu-id="8a03b-141">-IntegrationAccountId</span></span>
<span data-ttu-id="8a03b-142">指定邏輯應用程式的整合帳戶識別碼。</span><span class="sxs-lookup"><span data-stu-id="8a03b-142">Specifies an integration account ID for the logic app.</span></span>

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

### <span data-ttu-id="8a03b-143">-位置</span><span class="sxs-lookup"><span data-stu-id="8a03b-143">-Location</span></span>
<span data-ttu-id="8a03b-144">指定邏輯應用程式的位置。</span><span class="sxs-lookup"><span data-stu-id="8a03b-144">Specifies the location of the logic app.</span></span>
<span data-ttu-id="8a03b-145">輸入 Azure 資料中心位置，例如美國西部或東南亞。</span><span class="sxs-lookup"><span data-stu-id="8a03b-145">Enter an Azure data center location, such as West US or Southeast Asia.</span></span>
<span data-ttu-id="8a03b-146">您可以將邏輯應用程式放在任何位置。</span><span class="sxs-lookup"><span data-stu-id="8a03b-146">You can place a logic app in any location.</span></span>

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

### <span data-ttu-id="8a03b-147">-名稱</span><span class="sxs-lookup"><span data-stu-id="8a03b-147">-Name</span></span>
<span data-ttu-id="8a03b-148">指定邏輯應用程式的名稱。</span><span class="sxs-lookup"><span data-stu-id="8a03b-148">Specifies the name for the logic app.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8a03b-149">-ParameterFilePath</span><span class="sxs-lookup"><span data-stu-id="8a03b-149">-ParameterFilePath</span></span>
<span data-ttu-id="8a03b-150">指定 JSON 格式化參數檔案的路徑。</span><span class="sxs-lookup"><span data-stu-id="8a03b-150">Specifies the path of a JSON formatted parameter file.</span></span>

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

### <span data-ttu-id="8a03b-151">-參數</span><span class="sxs-lookup"><span data-stu-id="8a03b-151">-Parameters</span></span>
<span data-ttu-id="8a03b-152">指定邏輯 App 的參數集合物件。</span><span class="sxs-lookup"><span data-stu-id="8a03b-152">Specifies a parameters collection object for the Logic App.</span></span>
<span data-ttu-id="8a03b-153">指定雜湊表、字典 \<string\> 或字典 \<string, WorkflowParameter\> 。</span><span class="sxs-lookup"><span data-stu-id="8a03b-153">Specify a hash table, Dictionary\<string\>, or Dictionary\<string, WorkflowParameter\>.</span></span>

```yaml
Type: System.Object
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8a03b-154">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8a03b-154">-ResourceGroupName</span></span>
<span data-ttu-id="8a03b-155">指定資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="8a03b-155">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="8a03b-156">-State</span><span class="sxs-lookup"><span data-stu-id="8a03b-156">-State</span></span>
<span data-ttu-id="8a03b-157">指定邏輯應用程式的狀態。</span><span class="sxs-lookup"><span data-stu-id="8a03b-157">Specifies the state of the logic app.</span></span>
<span data-ttu-id="8a03b-158">此參數可接受的值為：啟用和停用。</span><span class="sxs-lookup"><span data-stu-id="8a03b-158">The acceptable values for this parameter are: Enabled and Disabled.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8a03b-159">-確認</span><span class="sxs-lookup"><span data-stu-id="8a03b-159">-Confirm</span></span>
<span data-ttu-id="8a03b-160">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="8a03b-160">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8a03b-161">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8a03b-161">-WhatIf</span></span>
<span data-ttu-id="8a03b-162">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="8a03b-162">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8a03b-163">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="8a03b-163">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8a03b-164">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8a03b-164">CommonParameters</span></span>
<span data-ttu-id="8a03b-165">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="8a03b-165">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8a03b-166">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="8a03b-166">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8a03b-167">輸入</span><span class="sxs-lookup"><span data-stu-id="8a03b-167">INPUTS</span></span>

### <span data-ttu-id="8a03b-168">System.String</span><span class="sxs-lookup"><span data-stu-id="8a03b-168">System.String</span></span>

## <span data-ttu-id="8a03b-169">輸出</span><span class="sxs-lookup"><span data-stu-id="8a03b-169">OUTPUTS</span></span>

### <span data-ttu-id="8a03b-170">System.Object</span><span class="sxs-lookup"><span data-stu-id="8a03b-170">System.Object</span></span>

## <span data-ttu-id="8a03b-171">筆記</span><span class="sxs-lookup"><span data-stu-id="8a03b-171">NOTES</span></span>

## <span data-ttu-id="8a03b-172">相關連結</span><span class="sxs-lookup"><span data-stu-id="8a03b-172">RELATED LINKS</span></span>

[<span data-ttu-id="8a03b-173">Get-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="8a03b-173">Get-AzLogicApp</span></span>](./Get-AzLogicApp.md)

[<span data-ttu-id="8a03b-174">Remove-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="8a03b-174">Remove-AzLogicApp</span></span>](./Remove-AzLogicApp.md)

[<span data-ttu-id="8a03b-175">Set-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="8a03b-175">Set-AzLogicApp</span></span>](./Set-AzLogicApp.md)

[<span data-ttu-id="8a03b-176">Start-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="8a03b-176">Start-AzLogicApp</span></span>](./Start-AzLogicApp.md)


