---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: 929F4593-2A71-49B9-87F8-F24FA9F6E314
online version: https://docs.microsoft.com/powershell/module/az.logicapp/test-azlogicapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Test-AzLogicApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Test-AzLogicApp.md
ms.openlocfilehash: 6639a397c97be35565d374279b2981fa2b1eabd8
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101902014"
---
# <span data-ttu-id="7e1b6-101">Test-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="7e1b6-101">Test-AzLogicApp</span></span>

## <span data-ttu-id="7e1b6-102">簡介</span><span class="sxs-lookup"><span data-stu-id="7e1b6-102">SYNOPSIS</span></span>
<span data-ttu-id="7e1b6-103">驗證邏輯應用程式定義。</span><span class="sxs-lookup"><span data-stu-id="7e1b6-103">Validates a logic app definition.</span></span>

## <span data-ttu-id="7e1b6-104">語法</span><span class="sxs-lookup"><span data-stu-id="7e1b6-104">SYNTAX</span></span>

### <span data-ttu-id="7e1b6-105">LogicAppWithDefinitionParameterSet</span><span class="sxs-lookup"><span data-stu-id="7e1b6-105">LogicAppWithDefinitionParameterSet</span></span>
```
Test-AzLogicApp -ResourceGroupName <String> -Name <String> -Location <String> [-State <String>]
 [-Definition <Object>] [-IntegrationAccountId <String>] [-Parameters <Object>] [-ParameterFilePath <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7e1b6-106">LogicAppWithDefinitionFileParameterSet</span><span class="sxs-lookup"><span data-stu-id="7e1b6-106">LogicAppWithDefinitionFileParameterSet</span></span>
```
Test-AzLogicApp -ResourceGroupName <String> -Name <String> -Location <String> [-State <String>]
 [-DefinitionFilePath <String>] [-IntegrationAccountId <String>] [-Parameters <Object>]
 [-ParameterFilePath <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7e1b6-107">描述</span><span class="sxs-lookup"><span data-stu-id="7e1b6-107">DESCRIPTION</span></span>
<span data-ttu-id="7e1b6-108">**Test-AzLogicApp** Cmdlet 會驗證資源群組中的邏輯應用程式定義。</span><span class="sxs-lookup"><span data-stu-id="7e1b6-108">The **Test-AzLogicApp** cmdlet validates a logic app definition in a resource group.</span></span>
<span data-ttu-id="7e1b6-109">指定邏輯應用程式名稱、資源組名、位置、狀態、整合帳戶識別碼或參數。</span><span class="sxs-lookup"><span data-stu-id="7e1b6-109">Specify the logic app name, resource group name, location, state, integration account ID, or parameters.</span></span>
<span data-ttu-id="7e1b6-110">此模組支援動態參數。</span><span class="sxs-lookup"><span data-stu-id="7e1b6-110">This module supports dynamic parameters.</span></span>
<span data-ttu-id="7e1b6-111">若要使用動態參數，請于命令中輸入。</span><span class="sxs-lookup"><span data-stu-id="7e1b6-111">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="7e1b6-112">若要探索動態參數的名稱，在 Cmdlet 名稱之後輸入連字號 (-) ，然後重複按 Tab 鍵以迴圈流覽可用的參數。</span><span class="sxs-lookup"><span data-stu-id="7e1b6-112">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="7e1b6-113">如果您省略必要的範本參數，Cmdlet 會提示您輸入值。</span><span class="sxs-lookup"><span data-stu-id="7e1b6-113">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="7e1b6-114">例子</span><span class="sxs-lookup"><span data-stu-id="7e1b6-114">EXAMPLES</span></span>

### <span data-ttu-id="7e1b6-115">範例 1：使用檔案路徑驗證邏輯應用程式</span><span class="sxs-lookup"><span data-stu-id="7e1b6-115">Example 1: Validate a logic app by using file paths</span></span>
```powershell
PS C:\>Test-AzLogicApp -ResourceGroupName "ResourceGroup11" -Name "LogicApp01" -Location "westus" -State "Enabled" -DefinitionFilePath "d:\workflows\Definition.json" -ParameterFilePath "d:\workflows\Parameters.json"
```

<span data-ttu-id="7e1b6-116">此命令會驗證指定資源群組中名為 LogicApp01 的邏輯應用程式。</span><span class="sxs-lookup"><span data-stu-id="7e1b6-116">This command validates a logic app named LogicApp01 in the specified resource group.</span></span>
<span data-ttu-id="7e1b6-117">命令會指定定義和參數檔案路徑。</span><span class="sxs-lookup"><span data-stu-id="7e1b6-117">The command specifies definition and parameter file paths.</span></span>

### <span data-ttu-id="7e1b6-118">範例 2：使用物件驗證邏輯應用程式</span><span class="sxs-lookup"><span data-stu-id="7e1b6-118">Example 2: Validate a logic app by using objects</span></span>
```powershell
PS C:\>Test-AzLogicApp -ResourceGroupName "ResourceGroup11" -Name "LogicApp01" -Location "westus" -State "Enabled" -Definition [IO.File]::ReadAllText("d:\Workflows\Definition.json") -Parameters @{name1="value1", name2="value2"}
```

<span data-ttu-id="7e1b6-119">此命令會驗證指定資源群組中名為 LogicApp01 的邏輯應用程式。</span><span class="sxs-lookup"><span data-stu-id="7e1b6-119">This command validates a logic app named LogicApp01 in the specified resource group.</span></span>
<span data-ttu-id="7e1b6-120">命令會指定定義和參數物件。</span><span class="sxs-lookup"><span data-stu-id="7e1b6-120">The command specifies definition and parameter objects.</span></span>

### <span data-ttu-id="7e1b6-121">範例 3</span><span class="sxs-lookup"><span data-stu-id="7e1b6-121">Example 3</span></span>

<span data-ttu-id="7e1b6-122">驗證邏輯應用程式定義。</span><span class="sxs-lookup"><span data-stu-id="7e1b6-122">Validates a logic app definition.</span></span> <span data-ttu-id="7e1b6-123"> (自動) </span><span class="sxs-lookup"><span data-stu-id="7e1b6-123">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
Test-AzLogicApp -DefinitionFilePath 'd:\workflows\Definition.json' -IntegrationAccountId <String> -Location 'westus' -Name 'LogicApp01' -ParameterFilePath 'd:\workflows\Parameters.json' -ResourceGroupName 'ResourceGroup11'
```

## <span data-ttu-id="7e1b6-124">參數</span><span class="sxs-lookup"><span data-stu-id="7e1b6-124">PARAMETERS</span></span>

### <span data-ttu-id="7e1b6-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7e1b6-125">-DefaultProfile</span></span>
<span data-ttu-id="7e1b6-126">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="7e1b6-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7e1b6-127">-定義</span><span class="sxs-lookup"><span data-stu-id="7e1b6-127">-Definition</span></span>
<span data-ttu-id="7e1b6-128">以 JSON 格式的 JavaScript 物件標記法指定邏輯應用程式 (定義) 字串。</span><span class="sxs-lookup"><span data-stu-id="7e1b6-128">Specifies the definition of a logic app as an object or a string in JavaScript Object Notation (JSON) format.</span></span>

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

### <span data-ttu-id="7e1b6-129">-DefinitionFilePath</span><span class="sxs-lookup"><span data-stu-id="7e1b6-129">-DefinitionFilePath</span></span>
<span data-ttu-id="7e1b6-130">以 JSON 格式指定邏輯應用程式的定義做為定義檔案的路徑。</span><span class="sxs-lookup"><span data-stu-id="7e1b6-130">Specifies the definition of your logic app as the path of a definition file in JSON format.</span></span>

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

### <span data-ttu-id="7e1b6-131">-IntegrationAccountId</span><span class="sxs-lookup"><span data-stu-id="7e1b6-131">-IntegrationAccountId</span></span>
<span data-ttu-id="7e1b6-132">指定邏輯應用程式的整合帳戶識別碼。</span><span class="sxs-lookup"><span data-stu-id="7e1b6-132">Specifies an integration account ID for the logic app.</span></span>

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

### <span data-ttu-id="7e1b6-133">-位置</span><span class="sxs-lookup"><span data-stu-id="7e1b6-133">-Location</span></span>
<span data-ttu-id="7e1b6-134">指定邏輯應用程式的位置。</span><span class="sxs-lookup"><span data-stu-id="7e1b6-134">Specifies the location of the logic app.</span></span>
<span data-ttu-id="7e1b6-135">輸入 Azure 資料中心位置，例如美國西部或東南亞。</span><span class="sxs-lookup"><span data-stu-id="7e1b6-135">Enter an Azure data center location, such as West US or Southeast Asia.</span></span>
<span data-ttu-id="7e1b6-136">您可以將邏輯應用程式放在任何位置。</span><span class="sxs-lookup"><span data-stu-id="7e1b6-136">You can place a logic app in any location.</span></span>

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

### <span data-ttu-id="7e1b6-137">-名稱</span><span class="sxs-lookup"><span data-stu-id="7e1b6-137">-Name</span></span>
<span data-ttu-id="7e1b6-138">指定邏輯應用程式的名稱。</span><span class="sxs-lookup"><span data-stu-id="7e1b6-138">Specifies the name of the logic app.</span></span>

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

### <span data-ttu-id="7e1b6-139">-ParameterFilePath</span><span class="sxs-lookup"><span data-stu-id="7e1b6-139">-ParameterFilePath</span></span>
<span data-ttu-id="7e1b6-140">指定 JSON 格式化參數檔案的路徑。</span><span class="sxs-lookup"><span data-stu-id="7e1b6-140">Specifies the path of a JSON formatted parameter file.</span></span>

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

### <span data-ttu-id="7e1b6-141">-參數</span><span class="sxs-lookup"><span data-stu-id="7e1b6-141">-Parameters</span></span>
<span data-ttu-id="7e1b6-142">指定邏輯應用程式的參數集合物件。</span><span class="sxs-lookup"><span data-stu-id="7e1b6-142">Specifies a parameters collection object of the logic app.</span></span>
<span data-ttu-id="7e1b6-143">指定雜湊表、字典 \<string\> 或字典 \<string, WorkflowParameter\> 。</span><span class="sxs-lookup"><span data-stu-id="7e1b6-143">Specify a hash table, Dictionary\<string\>, or Dictionary\<string, WorkflowParameter\>.</span></span>

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

### <span data-ttu-id="7e1b6-144">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7e1b6-144">-ResourceGroupName</span></span>
<span data-ttu-id="7e1b6-145">指定資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="7e1b6-145">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="7e1b6-146">-State</span><span class="sxs-lookup"><span data-stu-id="7e1b6-146">-State</span></span>
<span data-ttu-id="7e1b6-147">指定邏輯應用程式的狀態。</span><span class="sxs-lookup"><span data-stu-id="7e1b6-147">Specifies a state of the logic app.</span></span>
<span data-ttu-id="7e1b6-148">此參數可接受的值為：啟用和停用。</span><span class="sxs-lookup"><span data-stu-id="7e1b6-148">The acceptable values for this parameter are: Enabled and Disabled.</span></span>

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

### <span data-ttu-id="7e1b6-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7e1b6-149">CommonParameters</span></span>
<span data-ttu-id="7e1b6-150">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="7e1b6-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7e1b6-151">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="7e1b6-151">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7e1b6-152">輸入</span><span class="sxs-lookup"><span data-stu-id="7e1b6-152">INPUTS</span></span>

### <span data-ttu-id="7e1b6-153">System.String</span><span class="sxs-lookup"><span data-stu-id="7e1b6-153">System.String</span></span>

## <span data-ttu-id="7e1b6-154">輸出</span><span class="sxs-lookup"><span data-stu-id="7e1b6-154">OUTPUTS</span></span>

### <span data-ttu-id="7e1b6-155">System.Void</span><span class="sxs-lookup"><span data-stu-id="7e1b6-155">System.Void</span></span>

## <span data-ttu-id="7e1b6-156">筆記</span><span class="sxs-lookup"><span data-stu-id="7e1b6-156">NOTES</span></span>

## <span data-ttu-id="7e1b6-157">相關連結</span><span class="sxs-lookup"><span data-stu-id="7e1b6-157">RELATED LINKS</span></span>

[<span data-ttu-id="7e1b6-158">Get-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="7e1b6-158">Get-AzLogicApp</span></span>](./Get-AzLogicApp.md)

[<span data-ttu-id="7e1b6-159">New-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="7e1b6-159">New-AzLogicApp</span></span>](./New-AzLogicApp.md)

[<span data-ttu-id="7e1b6-160">Remove-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="7e1b6-160">Remove-AzLogicApp</span></span>](./Remove-AzLogicApp.md)

[<span data-ttu-id="7e1b6-161">Set-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="7e1b6-161">Set-AzLogicApp</span></span>](./Set-AzLogicApp.md)

[<span data-ttu-id="7e1b6-162">Start-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="7e1b6-162">Start-AzLogicApp</span></span>](./Start-AzLogicApp.md)


