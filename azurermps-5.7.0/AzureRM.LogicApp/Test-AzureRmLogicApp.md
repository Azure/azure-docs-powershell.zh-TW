---
external help file: Microsoft.Azure.Commands.LogicApp.dll-Help.xml
Module Name: AzureRM.LogicApp
ms.assetid: 929F4593-2A71-49B9-87F8-F24FA9F6E314
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.logicapp/test-azurermlogicapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Test-AzureRmLogicApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Test-AzureRmLogicApp.md
ms.openlocfilehash: c93cf0fdceebb3507a19c06ea5b6dda96fbc0656
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93625893"
---
# <span data-ttu-id="0398c-101">Test-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="0398c-101">Test-AzureRmLogicApp</span></span>

## <span data-ttu-id="0398c-102">摘要</span><span class="sxs-lookup"><span data-stu-id="0398c-102">SYNOPSIS</span></span>
<span data-ttu-id="0398c-103">驗證邏輯應用程式定義。</span><span class="sxs-lookup"><span data-stu-id="0398c-103">Validates a logic app definition.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0398c-104">句法</span><span class="sxs-lookup"><span data-stu-id="0398c-104">SYNTAX</span></span>

### <span data-ttu-id="0398c-105">LogicAppWithDefinitionParameterSet</span><span class="sxs-lookup"><span data-stu-id="0398c-105">LogicAppWithDefinitionParameterSet</span></span>
```
Test-AzureRmLogicApp -ResourceGroupName <String> -Name <String> -Location <String> [-State <String>]
 [-Definition <Object>] [-IntegrationAccountId <String>] [-Parameters <Object>] [-ParameterFilePath <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0398c-106">LogicAppWithDefinitionFileParameterSet</span><span class="sxs-lookup"><span data-stu-id="0398c-106">LogicAppWithDefinitionFileParameterSet</span></span>
```
Test-AzureRmLogicApp -ResourceGroupName <String> -Name <String> -Location <String> [-State <String>]
 [-DefinitionFilePath <String>] [-IntegrationAccountId <String>] [-Parameters <Object>]
 [-ParameterFilePath <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0398c-107">說明</span><span class="sxs-lookup"><span data-stu-id="0398c-107">DESCRIPTION</span></span>
<span data-ttu-id="0398c-108">**Test AzureRmLogicApp** Cmdlet 會驗證資源群組中的邏輯 app 定義。</span><span class="sxs-lookup"><span data-stu-id="0398c-108">The **Test-AzureRmLogicApp** cmdlet validates a logic app definition in a resource group.</span></span>
<span data-ttu-id="0398c-109">指定邏輯應用程式名稱、資源組名稱、位置、狀態、整合帳戶識別碼或參數。</span><span class="sxs-lookup"><span data-stu-id="0398c-109">Specify the logic app name, resource group name, location, state, integration account ID, or parameters.</span></span>

<span data-ttu-id="0398c-110">此模組支援動態參數。</span><span class="sxs-lookup"><span data-stu-id="0398c-110">This module supports dynamic parameters.</span></span>
<span data-ttu-id="0398c-111">若要使用動態參數，請在命令中輸入。</span><span class="sxs-lookup"><span data-stu-id="0398c-111">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="0398c-112">若要探索動態參數的名稱，請在 Cmdlet 名稱後輸入連字號 ( ) ，然後重複按 Tab 鍵以迴圈顯示可用的參數。</span><span class="sxs-lookup"><span data-stu-id="0398c-112">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="0398c-113">如果您省略必要的範本參數，則 Cmdlet 會提示您輸入值。</span><span class="sxs-lookup"><span data-stu-id="0398c-113">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="0398c-114">示例</span><span class="sxs-lookup"><span data-stu-id="0398c-114">EXAMPLES</span></span>

### <span data-ttu-id="0398c-115">範例1：使用檔路徑驗證邏輯 app</span><span class="sxs-lookup"><span data-stu-id="0398c-115">Example 1: Validate a logic app by using file paths</span></span>
```
PS C:\>Test-AzureRmLogicApp -ResourceGroupName "ResourceGroup11" -Name "LogicApp01" -Location "westus" -State "Enabled" -DefinitionFilePath "d:\workflows\Definition.json" -ParameterFilePath "d:\workflows\Parameters.json"
```

<span data-ttu-id="0398c-116">這個命令會驗證指定資源群組中名為 LogicApp01 的邏輯 app。</span><span class="sxs-lookup"><span data-stu-id="0398c-116">This command validates a logic app named LogicApp01 in the specified resource group.</span></span>
<span data-ttu-id="0398c-117">此命令指定定義和參數檔案路徑。</span><span class="sxs-lookup"><span data-stu-id="0398c-117">The command specifies definition and parameter file paths.</span></span>

### <span data-ttu-id="0398c-118">範例2：使用物件驗證邏輯 app</span><span class="sxs-lookup"><span data-stu-id="0398c-118">Example 2: Validate a logic app by using objects</span></span>
```
PS C:\>Test-AzureRmLogicApp -ResourceGroupName "ResourceGroup11" -Name "LogicApp01" -Location "westus" -State "Enabled" -Definition [IO.File]::ReadAllText("d:\Workflows\Definition.json") -Parameters @{name1="value1", name2="value2"}
```

<span data-ttu-id="0398c-119">這個命令會驗證指定資源群組中名為 LogicApp01 的邏輯 app。</span><span class="sxs-lookup"><span data-stu-id="0398c-119">This command validates a logic app named LogicApp01 in the specified resource group.</span></span>
<span data-ttu-id="0398c-120">此命令指定定義和參數物件。</span><span class="sxs-lookup"><span data-stu-id="0398c-120">The command specifies definition and parameter objects.</span></span>

## <span data-ttu-id="0398c-121">參數</span><span class="sxs-lookup"><span data-stu-id="0398c-121">PARAMETERS</span></span>

### <span data-ttu-id="0398c-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0398c-122">-DefaultProfile</span></span>
<span data-ttu-id="0398c-123">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="0398c-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0398c-124">-定義</span><span class="sxs-lookup"><span data-stu-id="0398c-124">-Definition</span></span>
<span data-ttu-id="0398c-125">將邏輯 app 的定義指定為 JavaScript 物件符號 (JSON) 格式中的物件或字串。</span><span class="sxs-lookup"><span data-stu-id="0398c-125">Specifies the definition of a logic app as an object or a string in JavaScript Object Notation (JSON) format.</span></span>

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

### <span data-ttu-id="0398c-126">-DefinitionFilePath</span><span class="sxs-lookup"><span data-stu-id="0398c-126">-DefinitionFilePath</span></span>
<span data-ttu-id="0398c-127">將您的邏輯 app 的定義指定為 JSON 格式之定義檔案的路徑。</span><span class="sxs-lookup"><span data-stu-id="0398c-127">Specifies the definition of your logic app as the path of a definition file in JSON format.</span></span>

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

### <span data-ttu-id="0398c-128">-IntegrationAccountId</span><span class="sxs-lookup"><span data-stu-id="0398c-128">-IntegrationAccountId</span></span>
<span data-ttu-id="0398c-129">指定邏輯 app 的整合帳戶識別碼。</span><span class="sxs-lookup"><span data-stu-id="0398c-129">Specifies an integration account ID for the logic app.</span></span>

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

### <span data-ttu-id="0398c-130">-位置</span><span class="sxs-lookup"><span data-stu-id="0398c-130">-Location</span></span>
<span data-ttu-id="0398c-131">指定邏輯 app 的位置。</span><span class="sxs-lookup"><span data-stu-id="0398c-131">Specifies the location of the logic app.</span></span>
<span data-ttu-id="0398c-132">輸入 Azure 資料中心的位置，例如 [西部] 或 [東南部]。</span><span class="sxs-lookup"><span data-stu-id="0398c-132">Enter an Azure data center location, such as West US or Southeast Asia.</span></span>
<span data-ttu-id="0398c-133">您可以將邏輯 app 放置在任何位置。</span><span class="sxs-lookup"><span data-stu-id="0398c-133">You can place a logic app in any location.</span></span>

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

### <span data-ttu-id="0398c-134">-名稱</span><span class="sxs-lookup"><span data-stu-id="0398c-134">-Name</span></span>
<span data-ttu-id="0398c-135">指定邏輯應用程式的名稱。</span><span class="sxs-lookup"><span data-stu-id="0398c-135">Specifies the name of the logic app.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0398c-136">-ParameterFilePath</span><span class="sxs-lookup"><span data-stu-id="0398c-136">-ParameterFilePath</span></span>
<span data-ttu-id="0398c-137">指定 JSON 格式化參數檔的路徑。</span><span class="sxs-lookup"><span data-stu-id="0398c-137">Specifies the path of a JSON formatted parameter file.</span></span>

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

### <span data-ttu-id="0398c-138">-參數</span><span class="sxs-lookup"><span data-stu-id="0398c-138">-Parameters</span></span>
<span data-ttu-id="0398c-139">指定邏輯 app 的參數集合物件。</span><span class="sxs-lookup"><span data-stu-id="0398c-139">Specifies a parameters collection object of the logic app.</span></span>
<span data-ttu-id="0398c-140">指定雜湊資料表、字典 \<string\> 或字典 \<string, WorkflowParameter\> 。</span><span class="sxs-lookup"><span data-stu-id="0398c-140">Specify a hash table, Dictionary\<string\>, or Dictionary\<string, WorkflowParameter\>.</span></span>

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

### <span data-ttu-id="0398c-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0398c-141">-ResourceGroupName</span></span>
<span data-ttu-id="0398c-142">指定資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="0398c-142">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="0398c-143">-State</span><span class="sxs-lookup"><span data-stu-id="0398c-143">-State</span></span>
<span data-ttu-id="0398c-144">指定邏輯 app 的狀態。</span><span class="sxs-lookup"><span data-stu-id="0398c-144">Specifies a state of the logic app.</span></span>
<span data-ttu-id="0398c-145">此參數可接受的值為： [已啟用] 和 [已停用]。</span><span class="sxs-lookup"><span data-stu-id="0398c-145">The acceptable values for this parameter are: Enabled and Disabled.</span></span>

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

### <span data-ttu-id="0398c-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0398c-146">CommonParameters</span></span>
<span data-ttu-id="0398c-147">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="0398c-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0398c-148">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="0398c-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0398c-149">輸入</span><span class="sxs-lookup"><span data-stu-id="0398c-149">INPUTS</span></span>

### <span data-ttu-id="0398c-150">所有</span><span class="sxs-lookup"><span data-stu-id="0398c-150">None</span></span>
<span data-ttu-id="0398c-151">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="0398c-151">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="0398c-152">輸出</span><span class="sxs-lookup"><span data-stu-id="0398c-152">OUTPUTS</span></span>

### <span data-ttu-id="0398c-153">System.object</span><span class="sxs-lookup"><span data-stu-id="0398c-153">System.Object</span></span>

## <span data-ttu-id="0398c-154">筆記</span><span class="sxs-lookup"><span data-stu-id="0398c-154">NOTES</span></span>

## <span data-ttu-id="0398c-155">相關連結</span><span class="sxs-lookup"><span data-stu-id="0398c-155">RELATED LINKS</span></span>

[<span data-ttu-id="0398c-156">AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="0398c-156">Get-AzureRmLogicApp</span></span>](./Get-AzureRmLogicApp.md)

[<span data-ttu-id="0398c-157">新-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="0398c-157">New-AzureRmLogicApp</span></span>](./New-AzureRmLogicApp.md)

[<span data-ttu-id="0398c-158">移除-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="0398c-158">Remove-AzureRmLogicApp</span></span>](./Remove-AzureRmLogicApp.md)

[<span data-ttu-id="0398c-159">Set-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="0398c-159">Set-AzureRmLogicApp</span></span>](./Set-AzureRmLogicApp.md)

[<span data-ttu-id="0398c-160">開始-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="0398c-160">Start-AzureRmLogicApp</span></span>](./Start-AzureRmLogicApp.md)


