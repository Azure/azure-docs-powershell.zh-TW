---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: AEDA89D3-EF80-4E56-9B97-677EC8F3959D
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/set-azlogicapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Set-AzLogicApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Set-AzLogicApp.md
ms.openlocfilehash: 254ab4f1dd126e1b671c9a1d899a9dbe8e71beca
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93611941"
---
# <span data-ttu-id="b61c7-101">Set-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="b61c7-101">Set-AzLogicApp</span></span>

## <span data-ttu-id="b61c7-102">摘要</span><span class="sxs-lookup"><span data-stu-id="b61c7-102">SYNOPSIS</span></span>
<span data-ttu-id="b61c7-103">修改資源群組中的邏輯 app。</span><span class="sxs-lookup"><span data-stu-id="b61c7-103">Modifies a logic app in a resource group.</span></span>

## <span data-ttu-id="b61c7-104">句法</span><span class="sxs-lookup"><span data-stu-id="b61c7-104">SYNTAX</span></span>

### <span data-ttu-id="b61c7-105">預設)  (消耗量</span><span class="sxs-lookup"><span data-stu-id="b61c7-105">Consumption (Default)</span></span>
```
Set-AzLogicApp -ResourceGroupName <String> -Name <String> [-UseConsumptionModel] [-State <String>]
 [-Definition <Object>] [-DefinitionFilePath <String>] [-IntegrationAccountId <String>] [-Parameters <Object>]
 [-ParameterFilePath <String>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b61c7-106">HostingPlan</span><span class="sxs-lookup"><span data-stu-id="b61c7-106">HostingPlan</span></span>
```
Set-AzLogicApp -ResourceGroupName <String> -Name <String> [-AppServicePlan <String>] [-State <String>]
 [-Definition <Object>] [-DefinitionFilePath <String>] [-IntegrationAccountId <String>] [-Parameters <Object>]
 [-ParameterFilePath <String>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b61c7-107">說明</span><span class="sxs-lookup"><span data-stu-id="b61c7-107">DESCRIPTION</span></span>
<span data-ttu-id="b61c7-108">**AzLogicApp** Cmdlet 會使用邏輯應用程式功能來修改邏輯 app。</span><span class="sxs-lookup"><span data-stu-id="b61c7-108">The **Set-AzLogicApp** cmdlet modifies a logic app by using the Logic Apps feature.</span></span>
<span data-ttu-id="b61c7-109">邏輯 app 是在邏輯應用程式定義中定義的動作或觸發程式的集合。</span><span class="sxs-lookup"><span data-stu-id="b61c7-109">A logic app is a collection of actions or triggers defined in Logic App definition.</span></span>
<span data-ttu-id="b61c7-110">這個 Cmdlet 會傳回 **工作流程** 物件。</span><span class="sxs-lookup"><span data-stu-id="b61c7-110">This cmdlet returns a **Workflow** object.</span></span>
<span data-ttu-id="b61c7-111">您可以透過指定名稱、位置、邏輯應用程式定義、資源群組和規劃來修改邏輯 app。</span><span class="sxs-lookup"><span data-stu-id="b61c7-111">You can modify a logic app by specifying a name, location, Logic App definition, resource group, and plan.</span></span>
<span data-ttu-id="b61c7-112">邏輯應用程式定義和參數的格式設定為 JavaScript 物件符號 (JSON) 。</span><span class="sxs-lookup"><span data-stu-id="b61c7-112">A Logic App definition and parameters are formatted in JavaScript Object Notation (JSON).</span></span>
<span data-ttu-id="b61c7-113">您可以使用邏輯 app 做為定義與參數的範本。</span><span class="sxs-lookup"><span data-stu-id="b61c7-113">You can use a logic app as a template for definition and parameters.</span></span>
<span data-ttu-id="b61c7-114">此模組支援動態參數。</span><span class="sxs-lookup"><span data-stu-id="b61c7-114">This module supports dynamic parameters.</span></span>
<span data-ttu-id="b61c7-115">若要使用動態參數，請在命令中輸入。</span><span class="sxs-lookup"><span data-stu-id="b61c7-115">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="b61c7-116">若要探索動態參數的名稱，請在 Cmdlet 名稱後輸入連字號 ( ) ，然後重複按 Tab 鍵以迴圈顯示可用的參數。</span><span class="sxs-lookup"><span data-stu-id="b61c7-116">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="b61c7-117">如果您省略必要的範本參數，則 Cmdlet 會提示您輸入值。</span><span class="sxs-lookup"><span data-stu-id="b61c7-117">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>
<span data-ttu-id="b61c7-118">您在命令列中指定的範本參數檔值優先于 template 參數物件中的範本參數值。</span><span class="sxs-lookup"><span data-stu-id="b61c7-118">Template parameter file values that you specify at the command line take precedence over template parameter values in a template parameter object.</span></span>

## <span data-ttu-id="b61c7-119">示例</span><span class="sxs-lookup"><span data-stu-id="b61c7-119">EXAMPLES</span></span>

### <span data-ttu-id="b61c7-120">範例1：修改邏輯 app</span><span class="sxs-lookup"><span data-stu-id="b61c7-120">Example 1: Modify a logic app</span></span>
```
PS C:\>Set-AzLogicApp -ResourceGroupName "ResourceGroup11" -Name "LogicApp17" -State "Enabled" -AppServicePlan "ServicePlan01" -DefinitionFilePath "d:\workflows\Definition17.json" -ParameterFilePath "d:\workflows\Parameters17.json"
Id                           : /subscriptions/57b7034d-72d4-433d-ace2-a7460aed6a99/resourceGroups/LogicAppCmdletTest/providers/Microsoft.Logic/workflows/LogicApp1
Name                         : LogicApp17
Type                         : Microsoft.Logic/workflows
Location                     : westus
ChangedTime                  : 1/13/2016 2:41:39 PM
CreatedTime                  : 1/13/2016 2:41:39 PM
AccessEndpoint               : https://westus.logic.azure.com:443/subscriptions/57b7034d-72d4-433d-ace2-a7460aed6a99/resourcegroups/ResourceGroup11/providers/Microsoft.Logic/workflows/LogicApp17
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
PlanId                       : /subscriptions/57b7034d-72d4-433d-ace2-a7460aed6a99/resourceGroups/ResourceGroup11/providers/Microsoft.Web/serverfarms/ServicePlan17
Version                      : 08587489107859952120
```

<span data-ttu-id="b61c7-121">這個命令會修改邏輯 app。</span><span class="sxs-lookup"><span data-stu-id="b61c7-121">This command modifies a logic app.</span></span>

## <span data-ttu-id="b61c7-122">參數</span><span class="sxs-lookup"><span data-stu-id="b61c7-122">PARAMETERS</span></span>

### <span data-ttu-id="b61c7-123">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="b61c7-123">-AppServicePlan</span></span>
<span data-ttu-id="b61c7-124">指定方案的名稱。</span><span class="sxs-lookup"><span data-stu-id="b61c7-124">Specifies the name of a plan.</span></span>

```yaml
Type: System.String
Parameter Sets: HostingPlan
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b61c7-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b61c7-125">-DefaultProfile</span></span>
<span data-ttu-id="b61c7-126">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="b61c7-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b61c7-127">-定義</span><span class="sxs-lookup"><span data-stu-id="b61c7-127">-Definition</span></span>
<span data-ttu-id="b61c7-128">將邏輯 app 的定義指定為 JavaScript 物件符號 (JSON) 格式中的物件或字串。</span><span class="sxs-lookup"><span data-stu-id="b61c7-128">Specifies the definition of a logic app as an object or a string in JavaScript Object Notation (JSON) format.</span></span>

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

### <span data-ttu-id="b61c7-129">-DefinitionFilePath</span><span class="sxs-lookup"><span data-stu-id="b61c7-129">-DefinitionFilePath</span></span>
<span data-ttu-id="b61c7-130">將邏輯 app 的定義指定為 JSON 格式的定義檔路徑。</span><span class="sxs-lookup"><span data-stu-id="b61c7-130">Specifies the definition of a logic app as the path of a definition file in JSON format.</span></span>

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

### <span data-ttu-id="b61c7-131">-Force</span><span class="sxs-lookup"><span data-stu-id="b61c7-131">-Force</span></span>
<span data-ttu-id="b61c7-132">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="b61c7-132">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="b61c7-133">-IntegrationAccountId</span><span class="sxs-lookup"><span data-stu-id="b61c7-133">-IntegrationAccountId</span></span>
<span data-ttu-id="b61c7-134">指定邏輯 app 的整合帳戶識別碼。</span><span class="sxs-lookup"><span data-stu-id="b61c7-134">Specifies an integration account ID for the logic app.</span></span>

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

### <span data-ttu-id="b61c7-135">-名稱</span><span class="sxs-lookup"><span data-stu-id="b61c7-135">-Name</span></span>
<span data-ttu-id="b61c7-136">指定邏輯應用程式的名稱。</span><span class="sxs-lookup"><span data-stu-id="b61c7-136">Specifies the name of a logic app.</span></span>

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

### <span data-ttu-id="b61c7-137">-ParameterFilePath</span><span class="sxs-lookup"><span data-stu-id="b61c7-137">-ParameterFilePath</span></span>
<span data-ttu-id="b61c7-138">指定 JSON 格式化參數檔的路徑。</span><span class="sxs-lookup"><span data-stu-id="b61c7-138">Specifies the path of a JSON formatted parameter file.</span></span>

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

### <span data-ttu-id="b61c7-139">-參數</span><span class="sxs-lookup"><span data-stu-id="b61c7-139">-Parameters</span></span>
<span data-ttu-id="b61c7-140">指定邏輯 App 的參數集合物件。</span><span class="sxs-lookup"><span data-stu-id="b61c7-140">Specifies a parameters collection object for the Logic App.</span></span>
<span data-ttu-id="b61c7-141">指定雜湊資料表、字典 \< 字串 \> 或字典 \< 字串（WorkflowParameter） \> 。</span><span class="sxs-lookup"><span data-stu-id="b61c7-141">Specify a hash table, Dictionary\<string\>, or Dictionary\<string, WorkflowParameter\>.</span></span>

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

### <span data-ttu-id="b61c7-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b61c7-142">-ResourceGroupName</span></span>
<span data-ttu-id="b61c7-143">指定資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="b61c7-143">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="b61c7-144">-State</span><span class="sxs-lookup"><span data-stu-id="b61c7-144">-State</span></span>
<span data-ttu-id="b61c7-145">指定邏輯 app 的狀態。</span><span class="sxs-lookup"><span data-stu-id="b61c7-145">Specifies the state of the logic app.</span></span>
<span data-ttu-id="b61c7-146">此參數可接受的值為： [已啟用] 和 [已停用]。</span><span class="sxs-lookup"><span data-stu-id="b61c7-146">The acceptable values for this parameter are: Enabled and Disabled.</span></span>

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

### <span data-ttu-id="b61c7-147">-UseConsumptionModel</span><span class="sxs-lookup"><span data-stu-id="b61c7-147">-UseConsumptionModel</span></span>
<span data-ttu-id="b61c7-148">表示邏輯 app 帳單使用的是以消耗量為基礎的模型。</span><span class="sxs-lookup"><span data-stu-id="b61c7-148">Indicates that the logic app billing use the consumption based model.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Consumption
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b61c7-149">-確認</span><span class="sxs-lookup"><span data-stu-id="b61c7-149">-Confirm</span></span>
<span data-ttu-id="b61c7-150">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="b61c7-150">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b61c7-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b61c7-151">-WhatIf</span></span>
<span data-ttu-id="b61c7-152">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="b61c7-152">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b61c7-153">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="b61c7-153">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b61c7-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b61c7-154">CommonParameters</span></span>
<span data-ttu-id="b61c7-155">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="b61c7-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b61c7-156">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="b61c7-156">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b61c7-157">輸入</span><span class="sxs-lookup"><span data-stu-id="b61c7-157">INPUTS</span></span>

### <span data-ttu-id="b61c7-158">System.object</span><span class="sxs-lookup"><span data-stu-id="b61c7-158">System.String</span></span>

## <span data-ttu-id="b61c7-159">輸出</span><span class="sxs-lookup"><span data-stu-id="b61c7-159">OUTPUTS</span></span>

### <span data-ttu-id="b61c7-160">System.object</span><span class="sxs-lookup"><span data-stu-id="b61c7-160">System.Object</span></span>

## <span data-ttu-id="b61c7-161">筆記</span><span class="sxs-lookup"><span data-stu-id="b61c7-161">NOTES</span></span>

## <span data-ttu-id="b61c7-162">相關連結</span><span class="sxs-lookup"><span data-stu-id="b61c7-162">RELATED LINKS</span></span>

[<span data-ttu-id="b61c7-163">AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="b61c7-163">Get-AzLogicApp</span></span>](./Get-AzLogicApp.md)

[<span data-ttu-id="b61c7-164">新-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="b61c7-164">New-AzLogicApp</span></span>](./New-AzLogicApp.md)

[<span data-ttu-id="b61c7-165">移除-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="b61c7-165">Remove-AzLogicApp</span></span>](./Remove-AzLogicApp.md)

[<span data-ttu-id="b61c7-166">開始-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="b61c7-166">Start-AzLogicApp</span></span>](./Start-AzLogicApp.md)

