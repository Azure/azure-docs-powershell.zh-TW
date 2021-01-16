---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: 929F4593-2A71-49B9-87F8-F24FA9F6E314
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/test-azlogicapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Test-AzLogicApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Test-AzLogicApp.md
ms.openlocfilehash: d38363d27253bea023e837e9b84076ccdcbf2b8d
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98281839"
---
# <span data-ttu-id="8fb8c-101">Test-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="8fb8c-101">Test-AzLogicApp</span></span>

## <span data-ttu-id="8fb8c-102">摘要</span><span class="sxs-lookup"><span data-stu-id="8fb8c-102">SYNOPSIS</span></span>
<span data-ttu-id="8fb8c-103">驗證邏輯應用程式定義。</span><span class="sxs-lookup"><span data-stu-id="8fb8c-103">Validates a logic app definition.</span></span>

## <span data-ttu-id="8fb8c-104">句法</span><span class="sxs-lookup"><span data-stu-id="8fb8c-104">SYNTAX</span></span>

### <span data-ttu-id="8fb8c-105">LogicAppWithDefinitionParameterSet</span><span class="sxs-lookup"><span data-stu-id="8fb8c-105">LogicAppWithDefinitionParameterSet</span></span>
```
Test-AzLogicApp -ResourceGroupName <String> -Name <String> -Location <String> [-State <String>]
 [-Definition <Object>] [-IntegrationAccountId <String>] [-Parameters <Object>] [-ParameterFilePath <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8fb8c-106">LogicAppWithDefinitionFileParameterSet</span><span class="sxs-lookup"><span data-stu-id="8fb8c-106">LogicAppWithDefinitionFileParameterSet</span></span>
```
Test-AzLogicApp -ResourceGroupName <String> -Name <String> -Location <String> [-State <String>]
 [-DefinitionFilePath <String>] [-IntegrationAccountId <String>] [-Parameters <Object>]
 [-ParameterFilePath <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8fb8c-107">說明</span><span class="sxs-lookup"><span data-stu-id="8fb8c-107">DESCRIPTION</span></span>
<span data-ttu-id="8fb8c-108">**Test AzLogicApp** Cmdlet 會驗證資源群組中的邏輯 app 定義。</span><span class="sxs-lookup"><span data-stu-id="8fb8c-108">The **Test-AzLogicApp** cmdlet validates a logic app definition in a resource group.</span></span>
<span data-ttu-id="8fb8c-109">指定邏輯應用程式名稱、資源組名稱、位置、狀態、整合帳戶識別碼或參數。</span><span class="sxs-lookup"><span data-stu-id="8fb8c-109">Specify the logic app name, resource group name, location, state, integration account ID, or parameters.</span></span>
<span data-ttu-id="8fb8c-110">此模組支援動態參數。</span><span class="sxs-lookup"><span data-stu-id="8fb8c-110">This module supports dynamic parameters.</span></span>
<span data-ttu-id="8fb8c-111">若要使用動態參數，請在命令中輸入。</span><span class="sxs-lookup"><span data-stu-id="8fb8c-111">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="8fb8c-112">若要探索動態參數的名稱，請在 Cmdlet 名稱後輸入連字號 ( ) ，然後重複按 Tab 鍵以迴圈顯示可用的參數。</span><span class="sxs-lookup"><span data-stu-id="8fb8c-112">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="8fb8c-113">如果您省略必要的範本參數，則 Cmdlet 會提示您輸入值。</span><span class="sxs-lookup"><span data-stu-id="8fb8c-113">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="8fb8c-114">示例</span><span class="sxs-lookup"><span data-stu-id="8fb8c-114">EXAMPLES</span></span>

### <span data-ttu-id="8fb8c-115">範例1：使用檔路徑驗證邏輯 app</span><span class="sxs-lookup"><span data-stu-id="8fb8c-115">Example 1: Validate a logic app by using file paths</span></span>
```powershell
PS C:\>Test-AzLogicApp -ResourceGroupName "ResourceGroup11" -Name "LogicApp01" -Location "westus" -State "Enabled" -DefinitionFilePath "d:\workflows\Definition.json" -ParameterFilePath "d:\workflows\Parameters.json"
```

<span data-ttu-id="8fb8c-116">這個命令會驗證指定資源群組中名為 LogicApp01 的邏輯 app。</span><span class="sxs-lookup"><span data-stu-id="8fb8c-116">This command validates a logic app named LogicApp01 in the specified resource group.</span></span>
<span data-ttu-id="8fb8c-117">此命令指定定義和參數檔案路徑。</span><span class="sxs-lookup"><span data-stu-id="8fb8c-117">The command specifies definition and parameter file paths.</span></span>

### <span data-ttu-id="8fb8c-118">範例2：使用物件驗證邏輯 app</span><span class="sxs-lookup"><span data-stu-id="8fb8c-118">Example 2: Validate a logic app by using objects</span></span>
```powershell
PS C:\>Test-AzLogicApp -ResourceGroupName "ResourceGroup11" -Name "LogicApp01" -Location "westus" -State "Enabled" -Definition [IO.File]::ReadAllText("d:\Workflows\Definition.json") -Parameters @{name1="value1", name2="value2"}
```

<span data-ttu-id="8fb8c-119">這個命令會驗證指定資源群組中名為 LogicApp01 的邏輯 app。</span><span class="sxs-lookup"><span data-stu-id="8fb8c-119">This command validates a logic app named LogicApp01 in the specified resource group.</span></span>
<span data-ttu-id="8fb8c-120">此命令指定定義和參數物件。</span><span class="sxs-lookup"><span data-stu-id="8fb8c-120">The command specifies definition and parameter objects.</span></span>

### <span data-ttu-id="8fb8c-121">範例3</span><span class="sxs-lookup"><span data-stu-id="8fb8c-121">Example 3</span></span>

<span data-ttu-id="8fb8c-122">驗證邏輯應用程式定義。</span><span class="sxs-lookup"><span data-stu-id="8fb8c-122">Validates a logic app definition.</span></span> <span data-ttu-id="8fb8c-123"> (自動生成) </span><span class="sxs-lookup"><span data-stu-id="8fb8c-123">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
Test-AzLogicApp -DefinitionFilePath 'd:\workflows\Definition.json' -IntegrationAccountId <String> -Location 'westus' -Name 'LogicApp01' -ParameterFilePath 'd:\workflows\Parameters.json' -ResourceGroupName 'ResourceGroup11'
```

## <span data-ttu-id="8fb8c-124">參數</span><span class="sxs-lookup"><span data-stu-id="8fb8c-124">PARAMETERS</span></span>

### <span data-ttu-id="8fb8c-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8fb8c-125">-DefaultProfile</span></span>
<span data-ttu-id="8fb8c-126">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="8fb8c-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8fb8c-127">-定義</span><span class="sxs-lookup"><span data-stu-id="8fb8c-127">-Definition</span></span>
<span data-ttu-id="8fb8c-128">將邏輯 app 的定義指定為 JavaScript 物件符號 (JSON) 格式中的物件或字串。</span><span class="sxs-lookup"><span data-stu-id="8fb8c-128">Specifies the definition of a logic app as an object or a string in JavaScript Object Notation (JSON) format.</span></span>

```yaml
Type: System.Object
Parameter Sets: LogicAppWithDefinitionParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8fb8c-129">-DefinitionFilePath</span><span class="sxs-lookup"><span data-stu-id="8fb8c-129">-DefinitionFilePath</span></span>
<span data-ttu-id="8fb8c-130">將您的邏輯 app 的定義指定為 JSON 格式之定義檔案的路徑。</span><span class="sxs-lookup"><span data-stu-id="8fb8c-130">Specifies the definition of your logic app as the path of a definition file in JSON format.</span></span>

```yaml
Type: System.String
Parameter Sets: LogicAppWithDefinitionFileParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8fb8c-131">-IntegrationAccountId</span><span class="sxs-lookup"><span data-stu-id="8fb8c-131">-IntegrationAccountId</span></span>
<span data-ttu-id="8fb8c-132">指定邏輯 app 的整合帳戶識別碼。</span><span class="sxs-lookup"><span data-stu-id="8fb8c-132">Specifies an integration account ID for the logic app.</span></span>

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

### <span data-ttu-id="8fb8c-133">-位置</span><span class="sxs-lookup"><span data-stu-id="8fb8c-133">-Location</span></span>
<span data-ttu-id="8fb8c-134">指定邏輯 app 的位置。</span><span class="sxs-lookup"><span data-stu-id="8fb8c-134">Specifies the location of the logic app.</span></span>
<span data-ttu-id="8fb8c-135">輸入 Azure 資料中心的位置，例如 [西部] 或 [東南部]。</span><span class="sxs-lookup"><span data-stu-id="8fb8c-135">Enter an Azure data center location, such as West US or Southeast Asia.</span></span>
<span data-ttu-id="8fb8c-136">您可以將邏輯 app 放置在任何位置。</span><span class="sxs-lookup"><span data-stu-id="8fb8c-136">You can place a logic app in any location.</span></span>

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

### <span data-ttu-id="8fb8c-137">-名稱</span><span class="sxs-lookup"><span data-stu-id="8fb8c-137">-Name</span></span>
<span data-ttu-id="8fb8c-138">指定邏輯應用程式的名稱。</span><span class="sxs-lookup"><span data-stu-id="8fb8c-138">Specifies the name of the logic app.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8fb8c-139">-ParameterFilePath</span><span class="sxs-lookup"><span data-stu-id="8fb8c-139">-ParameterFilePath</span></span>
<span data-ttu-id="8fb8c-140">指定 JSON 格式化參數檔的路徑。</span><span class="sxs-lookup"><span data-stu-id="8fb8c-140">Specifies the path of a JSON formatted parameter file.</span></span>

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

### <span data-ttu-id="8fb8c-141">-參數</span><span class="sxs-lookup"><span data-stu-id="8fb8c-141">-Parameters</span></span>
<span data-ttu-id="8fb8c-142">指定邏輯 app 的參數集合物件。</span><span class="sxs-lookup"><span data-stu-id="8fb8c-142">Specifies a parameters collection object of the logic app.</span></span>
<span data-ttu-id="8fb8c-143">指定雜湊資料表、字典 \<string\> 或字典 \<string, WorkflowParameter\> 。</span><span class="sxs-lookup"><span data-stu-id="8fb8c-143">Specify a hash table, Dictionary\<string\>, or Dictionary\<string, WorkflowParameter\>.</span></span>

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

### <span data-ttu-id="8fb8c-144">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8fb8c-144">-ResourceGroupName</span></span>
<span data-ttu-id="8fb8c-145">指定資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="8fb8c-145">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="8fb8c-146">-State</span><span class="sxs-lookup"><span data-stu-id="8fb8c-146">-State</span></span>
<span data-ttu-id="8fb8c-147">指定邏輯 app 的狀態。</span><span class="sxs-lookup"><span data-stu-id="8fb8c-147">Specifies a state of the logic app.</span></span>
<span data-ttu-id="8fb8c-148">此參數可接受的值為： [已啟用] 和 [已停用]。</span><span class="sxs-lookup"><span data-stu-id="8fb8c-148">The acceptable values for this parameter are: Enabled and Disabled.</span></span>

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

### <span data-ttu-id="8fb8c-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8fb8c-149">CommonParameters</span></span>
<span data-ttu-id="8fb8c-150">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="8fb8c-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8fb8c-151">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="8fb8c-151">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8fb8c-152">輸入</span><span class="sxs-lookup"><span data-stu-id="8fb8c-152">INPUTS</span></span>

### <span data-ttu-id="8fb8c-153">System.object</span><span class="sxs-lookup"><span data-stu-id="8fb8c-153">System.String</span></span>

## <span data-ttu-id="8fb8c-154">輸出</span><span class="sxs-lookup"><span data-stu-id="8fb8c-154">OUTPUTS</span></span>

### <span data-ttu-id="8fb8c-155">System.void</span><span class="sxs-lookup"><span data-stu-id="8fb8c-155">System.Void</span></span>

## <span data-ttu-id="8fb8c-156">筆記</span><span class="sxs-lookup"><span data-stu-id="8fb8c-156">NOTES</span></span>

## <span data-ttu-id="8fb8c-157">相關連結</span><span class="sxs-lookup"><span data-stu-id="8fb8c-157">RELATED LINKS</span></span>

[<span data-ttu-id="8fb8c-158">AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="8fb8c-158">Get-AzLogicApp</span></span>](./Get-AzLogicApp.md)

[<span data-ttu-id="8fb8c-159">新-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="8fb8c-159">New-AzLogicApp</span></span>](./New-AzLogicApp.md)

[<span data-ttu-id="8fb8c-160">移除-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="8fb8c-160">Remove-AzLogicApp</span></span>](./Remove-AzLogicApp.md)

[<span data-ttu-id="8fb8c-161">Set-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="8fb8c-161">Set-AzLogicApp</span></span>](./Set-AzLogicApp.md)

[<span data-ttu-id="8fb8c-162">開始-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="8fb8c-162">Start-AzLogicApp</span></span>](./Start-AzLogicApp.md)


